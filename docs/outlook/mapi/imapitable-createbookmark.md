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
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817576"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Hace referencia a**: Outlook 
  
Crea un marcador en la posición actual de la tabla.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parámetros

 _lpbkPosition_
  
> [out] Puntero al valor devuelto de 32 bits de marcador. Más adelante se puede pasar este marcador en una llamada al método [IMAPITable::SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> No se pudo completar la operación solicitada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::CreateBookmark** marca una posición de tabla mediante la creación de un valor de un marcador. Un marcador se puede utilizar para volver a la posición identificada por el marcador. El marcador de posición está asociada con el objeto en esa fila en la tabla. 
  
En las tablas de datos adjuntos no se admiten los marcadores y las implementaciones de la tabla de datos adjuntos de **CreateBookmark** devuelven MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Debido a los gastos de memoria del mantenimiento de las posiciones de cursor con marcadores, limitar el número de marcadores que se pueden crear. Cuando llegue a ese número, devolver MAPI_E_UNABLE_TO_COMPLETE de todas las llamadas subsiguientes a **CreateBookmark**.
  
En ocasiones, un marcador apunta a una fila que ya no está en la vista de tabla. Si un autor de la llamada usa como un marcador, mueva el cursor a la siguiente fila visible y detenga no existe. 
  
Cuando el autor de la llamada intenta utilizar un marcador que señala a una fila no visible debido a que se ha contraído, devolver MAPI_W_POSITION_CHANGED después de mover el marcador. Puede cambiar la posición del marcador en la siguiente fila visible en este momento, o cuando la contracción se produce en el método **SetCollapseState** . Si mueve el marcador en el momento de la fila está contraída, debe conservar un poco en el marcador que indica exactamente cuándo se ha movido el marcador: debido a que su última utilizar o si nunca se ha usado desde su creación. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CreateBookmark** asigna memoria para el marcador que se creen. Liberar los recursos para el marcador llamando al método [IMAPITable::FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Vea también



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

