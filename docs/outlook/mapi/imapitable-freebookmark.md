---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409457"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Libera la memoria asociada a un marcador.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameters

 _bkPosition_
  
> [in] El marcador que se va a liberar, creado mediante una llamada al [método IMAPITable::CreateBookmark.](imapitable-createbookmark.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El marcador se ha liberando correctamente.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador especificado no existe.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::FreeBookmark** libera un marcador que ya no es necesario. El marcador ya no es válido después de esta llamada. Cada vez que se libera una tabla de la memoria, también se liberan todos los marcadores asociados. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si el autor de la llamada pasa uno de los tres marcadores predefinidos en el parámetro  _bkPosition,_ ignore la solicitud y devuelva S_OK. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

