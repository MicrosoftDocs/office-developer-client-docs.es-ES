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
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318042"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define los datos de los marcadores para recordar una posición en una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Métodos relacionados:  <br/> |[IMAPITable:: CreateBookmark](imapitable-createbookmark.md) [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Comentarios

MAPI define tres marcadores, enumerados como sigue:
  
BOOKMARK_BEGINNING 
  
> Recuerda la posición inicial de la tabla. 
    
BOOKMARK_CURRENT 
  
> Recuerda la posición actual de la tabla.
    
BOOKMARK_END 
  
> Recuerda la posición final de la tabla.
    
Los clientes pueden crear otros marcadores para recordar otras posiciones de tabla. Los marcadores solo son válidos cuando la tabla está abierta. Los clientes deben liberar los marcadores que hayan creado antes de cerrar la tabla asociada. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Tipos de datos MAPI](mapi-data-types.md)

