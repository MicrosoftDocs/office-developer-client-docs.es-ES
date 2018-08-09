---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816660"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Hace referencia a**: Outlook 
  
Define los datos de marcadores de recordar una posición en una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Métodos relacionados:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Comentarios

MAPI define tres marcadores, como se indica a continuación:
  
BOOKMARK_BEGINNING 
  
> Recuerda la posición inicial de la tabla. 
    
BOOKMARK_CURRENT 
  
> Recuerda la posición actual de la tabla.
    
BOOKMARK_END 
  
> Recuerda la posición final de la tabla.
    
Los clientes pueden crear otros marcadores para recordar otras posiciones de tabla. Marcadores son válidos sólo cuando la tabla está abierta. Los clientes deben liberar todos los marcadores que se hayan creado antes de cerrar la tabla asociada. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Tipos de datos MAPI](mapi-data-types.md)

