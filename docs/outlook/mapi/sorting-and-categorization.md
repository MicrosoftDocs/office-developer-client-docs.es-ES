---
title: Ordenar y categorización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820717"
---
# <a name="sorting-and-categorization"></a>Ordenar y categorización

 
  
**Hace referencia a**: Outlook 
  
Ordenar una tabla, coloca las filas en un orden que tenga sentido para su visor. Por ejemplo, podría preferir un visor ver la tabla de contenido de una carpeta ordenada por asunto del mensaje de modo que todos los subprocesos de una conversación estén juntas mientras otro visor es posible que desea que los mensajes ordenados por el nombre del remitente. Una tabla de la instancia recién creada no se ordena necesariamente en un orden determinado. 
  
Hay dos tipos de ordenación:
  
- Ordenación estándar
    
- Clasificar la ordenación 
    
Con la ordenación estándar, todas las filas se muestran en una lista plana con una o varias columnas como un criterio de ordenación. Con la ordenación por categorías, las filas se muestran jerárquicamente con una o varias columnas como el criterio de ordenación. Dentro de cada categoría, hay una fila de encabezado especial que contiene las siguientes columnas.
  
- La columna o columnas que componen la clave de ordenación
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
En la fila de encabezado de sangría son todas las filas de la tabla que contienen columnas con valores que coinciden con el criterio de ordenación. Estas filas se denominan las filas de la hoja. Las filas de la hoja contienen todas las columnas en el conjunto menos las columnas de clave de ordenación de columnas. 
  
Las tablas de contenido de carpetas a menudo admiten la ordenación por categorías además de ordenación estándar. Normalmente, en las tablas de contenido de los contenedores de la libreta de direcciones se admiten la ordenación sólo estándar. 
  
Una categoría puede tener dos estados: contraído y expandido. Cuando una categoría se encuentra en el estado contraído, [IMAPITable:: QueryRows](imapitable-queryrows.md)devuelve sólo la fila de encabezado. Cuando una categoría se encuentra en estado expandido, se devuelven todas las filas relacionadas con la categoría. Esto incluye la fila de encabezado y las filas de la hoja. 
  
Cada categoría en una vista de tabla se puede expandir o contraer de forma independiente. Es decir, deben ser no todas las categorías en el mismo estado al mismo tiempo; Algunas categorías se pueden contraer mientras que otras personas se expanden. 
  
El usuario de una tabla con categorías decide cómo se muestra. Una opción común consiste en usar un control proporcionado en el SDK de Windows denominado el control treeview. Controles TreeView son cuadros de lista que admiten la información en una estructura de árbol. Filas de encabezado para las categorías en el estado expandido se marcan con un signo menos mientras se marcan las filas de encabezado para las categorías en el estado contraído con un signo más. Categorías expandidas se muestran con las filas de la hoja con sangría bajo las filas de encabezado. 
  
Para contraer y expandir una categoría, una aplicación de cliente o un proveedor de servicios usa las siguientes [IMAPITable: IUnknown](imapitableiunknown.md) métodos: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Para obtener más información acerca de la ordenación los subprocesos de una conversación vea los siguientes temas:
  
- [SSortOrder](ssortorder.md)
    
- [Propiedad canónica PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propiedad canónica PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propiedad canónica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propiedad canónica PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Ordenar tablas después de establecer restricciones y columnas](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

