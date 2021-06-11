---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408827"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un marcador en la posición actual de la tabla.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parameters

 _lpbkPosition_
  
> [salida] Puntero al valor devuelto de marcador de 32 bits. Este marcador se puede pasar más adelante en una llamada al método [IMAPITable::SeekRow.](imapitable-seekrow.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> No se pudo completar la operación solicitada.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::CreateBookmark** marca una posición de tabla creando un valor denominado marcador. Se puede usar un marcador para volver a la posición identificada por el marcador. La posición marcada está asociada con el objeto en esa fila de la tabla. 
  
Los marcadores no se admiten en las tablas de datos adjuntos y las implementaciones de tablas de datos adjuntos de **CreateBookmark** devuelven MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Debido al gasto de memoria de mantener las posiciones del cursor con marcadores, limite el número de marcadores que puede crear. Cuando llegue a ese número, devuelva MAPI_E_UNABLE_TO_COMPLETE de todas las llamadas posteriores a **CreateBookmark**.
  
A veces, un marcador apunta a una fila que ya no está en la vista de tabla. Si un autor de la llamada usa un marcador de este tipo, mueva el cursor a la siguiente fila visible y deténlo allí. 
  
Cuando el autor de la llamada intente usar un marcador que apunte a una fila no invisible porque se ha contraído, MAPI_W_POSITION_CHANGED después de mover el marcador. Puede cambiar la posición del marcador a la siguiente fila visible en este momento o cuando se produzca la contación en el **método SetCollapseState.** Si mueve el marcador en el momento en que se contrae la fila, debe conservar un poco en el marcador que indica exactamente cuándo se movió el marcador: desde su último uso o si nunca se ha usado desde su creación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CreateBookmark** asigna memoria al marcador que crea. Libere los recursos del marcador llamando al [método IMAPITable::FreeBookmark.](imapitable-freebookmark.md) 
  
## <a name="see-also"></a>Vea también



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

