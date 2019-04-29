---
title: Ordenación y categorización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418487"
---
# <a name="sorting-and-categorization"></a>Ordenación y categorización

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Ordenar una tabla coloca las filas en un orden que tiene sentido para su visor. Por ejemplo, un visor puede preferir ver la tabla de contenido de una carpeta ordenada por asunto del mensaje, de modo que todos los subprocesos de una conversación estén juntos, mientras que otro usuario desea ordenar los mensajes por el nombre del remitente. Una tabla recién creada no está necesariamente ordenada en un orden determinado. 
  
Hay dos tipos de ordenación:
  
- Ordenación estándar
    
- Ordenación por categorías 
    
Con la ordenación estándar, todas las filas se muestran en una lista plana con una o más columnas como criterio de ordenación. Con la ordenación por categorías, las filas se muestran jerárquicamente con una o más columnas como clave de ordenación. Dentro de cada categoría hay una fila de encabezado especial que contiene las columnas siguientes.
  
- La columna o columnas que componen el criterio de ordenación
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
La sangría situada debajo de la fila de encabezado son todas las filas de la tabla que contienen columnas con valores que coinciden con la clave de ordenación. Estas filas se denominan filas de hoja. Las filas hoja contienen todas las columnas del conjunto de columnas menos las columnas clave de ordenación. 
  
Las tablas de contenido de las carpetas a menudo admiten la ordenación por categorías además de la ordenación estándar. Las tablas de contenido de los contenedores de la libreta de direcciones normalmente solo admiten la ordenación estándar. 
  
Una categoría puede tener dos Estados: contraído y expandido. Cuando una categoría está contraída, sólo la fila de título se devuelve desde [IMAPITable:: QueryRows](imapitable-queryrows.md). Cuando una categoría está en estado expandido, se devuelven todas las filas relacionadas con la categoría. Esto incluye la fila de encabezado y las filas de hoja. 
  
Cada categoría de una vista de tabla se puede expandir o contraer independientemente. Es decir, no todas las categorías deben estar en el mismo estado al mismo tiempo; algunas categorías pueden estar contraídas mientras que otras se expanden. 
  
El usuario de una tabla clasificada decide cómo se muestra. Una opción común es usar un control proporcionado en el SDK de Windows denominado el control TreeView. Los controles TreeView son cuadros de lista que admiten información en una estructura de tipo árbol. Las filas de título de las categorías con el estado expandido se marcan con un signo menos mientras que las filas de título de las categorías del estado contraído se marcan con un signo más. Las categorías expandidas se muestran con las filas hoja con sangría debajo de las filas de título. 
  
Para contraer y expandir una categoría, una aplicación cliente o un proveedor de servicios utiliza los siguientes métodos [IMAPITable: IUnknown](imapitableiunknown.md) : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Para obtener más información acerca de la ordenación de los subprocesos de una conversación, vea los siguientes temas:
  
- [SSortOrder](ssortorder.md)
    
- [Propiedad canónica PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propiedad canónica PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propiedad canónica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propiedad canónica PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Ordenar tablas después de establecer las columnas y restricciones](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

