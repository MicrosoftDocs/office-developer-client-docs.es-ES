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
  
> contempla Puntero al valor de marcador de 32 bits devuelto. Este marcador se puede pasar más adelante en una llamada al método [IMAPITable:: SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> No se pudo completar la operación solicitada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: CreateBookmark** marca una posición de tabla mediante la creación de un valor denominado Bookmark. Se puede usar un marcador para volver a la posición identificada por el marcador. La posición marcada se asocia con el objeto de esa fila en la tabla. 
  
Los marcadores no se admiten en tablas adjuntas y las implementaciones de tabla de datos adjuntos de **CreateBookmark** devuelven MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Debido al gasto en la memoria que supone mantener las posiciones del cursor con marcadores, limite el número de marcadores que puede crear. Cuando llegue a ese número, devuelva MAPI_E_UNABLE_TO_COMPLETE de todas las llamadas posteriores a **CreateBookmark**.
  
A veces, un marcador apunta a una fila que ya no está en la vista de tabla. Si el autor de la llamada utiliza un marcador de ese tipo, mueva el cursor a la siguiente fila visible y deténgalo. 
  
Cuando el autor de la llamada intenta usar un marcador que señala a una fila no visible porque se ha contraído, devuelve MAPI_W_POSITION_CHANGED después de mover el marcador. Puede cambiar la posición del marcador a la siguiente fila visible en este momento o cuando la contracción se produzca en el método **SetCollapseState** . Si mueve el marcador en el momento en que se contrae la fila, debe conservar un bit en el marcador que indique exactamente cuándo se movió el marcador: desde su último uso o si nunca se ha usado desde su creación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CreateBookmark** asigna memoria para el marcador que crea. Para liberar los recursos del marcador, llame al método [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Ver también



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

