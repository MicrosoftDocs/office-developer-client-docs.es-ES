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
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817592"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Hace referencia a**: Outlook 
  
Libera la memoria asociada con un marcador.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parámetros

 _bkPosition_
  
> [entrada] El marcador que se va a liberar, creado al llamar al método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El marcador correctamente se libera.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador especificado no existe.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::FreeBookmark** libera un marcador que ya no sea necesaria. El marcador ya no es válido después de esta llamada. Siempre que se publique una tabla de la memoria, todos sus marcadores asociados también se liberan. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si el autor de la llamada pasa a uno de los tres marcadores predefinidos en el parámetro _bkPosition_ , omitir la solicitud y devolver S_OK. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

