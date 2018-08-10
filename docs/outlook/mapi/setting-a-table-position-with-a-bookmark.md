---
title: Establecer una posición de tabla con un marcador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820641"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Establecer una posición de tabla con un marcador

  
  
**Hace referencia a**: Outlook 
  
Un marcador es un recurso que indica una ubicación determinada en una tabla. Establecer un marcador hace posible volver a una posición en un momento posterior, una característica que puede mejorar significativamente el rendimiento de las operaciones de la tabla. MAPI define tres marcadores estándares: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Puntos a la fila actual de una tabla.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Puntos a la primera fila de una tabla.  <br/> |
|BOOKMARK_END  <br/> |Apunta a la última fila de una tabla.  <br/> |
   
Los implementadores de tabla son necesarios para admitir estos marcadores estándares y también pueden admitir otros usuarios. Sin embargo, debido a que los marcadores son recursos y los recursos se limitan, los usuarios de marcador deben liberarlos tan pronto como sea posible. 
  
 **Para establecer un marcador en la posición actual de la tabla**
  
- Llame a [IMAPITable::CreateBookmark](imapitable-createbookmark.md). En ocasiones será suficiente memoria disponible para asignar el nuevo marcador, lo que provoca que **CreateBookmark** devolver el valor de error MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Para liberar un marcador**
  
- Llame a [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover el cursor a una posición con marcador**
  
- Llame a [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** establece un nuevo valor para la posición de BOOKMARK_CURRENT. **SeekRow** puede utilizarse, por ejemplo, para colocar un filas de tabla diez desde la posición actual o para empezar de nuevo al principio. Los clientes o proveedores de servicios pueden buscar a la actual, a partir de, o finalizar de una tabla o cualquier otra posición en la que está asociada con un marcador predefinido. En una dirección hacia delante o hacia atrás y el límite de la operación puede mover a un número especificado de filas. Como regla general, deben tratar de los autores de llamadas a través de no más de 50 filas con **SeekRow**; Debe usarse [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) con un gran número de filas. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

