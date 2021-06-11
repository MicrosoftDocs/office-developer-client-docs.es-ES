---
title: Ordenación y categorización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418487"
---
# <a name="sorting-and-categorization"></a>Ordenación y categorización

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Ordenar una tabla coloca las filas en un orden que tiene sentido para su visor. Por ejemplo, un visor puede preferir ver la tabla de contenido de una carpeta ordenada por asunto de mensaje para que todos los subprocesos de una conversación estén juntos, mientras que otro visor podría querer que los mensajes se ordenen por el nombre del remitente. Una tabla recién creada con instancias no se ordena necesariamente en ningún orden en particular. 
  
Hay dos tipos de ordenación:
  
- Ordenación estándar
    
- Ordenación categorizada 
    
Con la ordenación estándar, todas las filas se muestran en una lista plana con una o más columnas como clave de ordenación. Con la ordenación categorizada, las filas se muestran jerárquicamente con una o más columnas como clave de ordenación. Dentro de cada categoría, hay una fila de título especial que contiene las siguientes columnas.
  
- La columna o columnas que forma la clave de ordenación
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Sangría debajo de la fila de encabezado son todas las filas de la tabla que contienen columnas con valores que coinciden con la clave de ordenación. Estas filas se denominan filas de hoja. Las filas de hoja contienen todas las columnas del conjunto de columnas menos las columnas de clave de ordenación. 
  
Las tablas de contenido de las carpetas a menudo admiten la ordenación categorizada además de la ordenación estándar. Las tablas de contenido de los contenedores de libreta de direcciones normalmente solo admiten la ordenación estándar. 
  
Una categoría puede tener dos estados: contraído y expandido. Cuando una categoría está en estado contraído, solo se devuelve la fila de encabezado de [IMAPITable::QueryRows](imapitable-queryrows.md). Cuando una categoría está en estado expandido, se devuelven todas las filas relacionadas con la categoría. Esto incluye la fila de encabezado y las filas de hoja. 
  
Cada categoría de una vista de tabla puede expandirse o contraerse de forma independiente. Es decir, no todas las categorías deben estar en el mismo estado al mismo tiempo; algunas categorías se pueden contraer mientras que otras se expanden. 
  
El usuario de una tabla categorizada decide cómo se muestra. Una opción común es usar un control proporcionado en el SDK de Windows denominado control treeview. Los controles Treeview son cuadros de lista que admiten información en una estructura similar a un árbol. Las filas de encabezado de las categorías en el estado expandido se marcan con un signo menos mientras que las filas de encabezado para las categorías en estado contraído se marcan con un signo más. Las categorías expandida se muestran con las filas de hoja sangría debajo de las filas de encabezado. 
  
Para contraer y expandir una categoría, una aplicación cliente o un proveedor de servicios usa los siguientes [métodos IMAPITable : IUnknown:](imapitableiunknown.md) 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Para obtener más información sobre cómo ordenar los subprocesos de una conversación, consulte los siguientes temas:
  
- [SSortOrder](ssortorder.md)
    
- [Propiedad canónica PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propiedad canónica PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propiedad canónica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propiedad canónica PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Ordenar tablas después de establecer columnas y restricciones](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

