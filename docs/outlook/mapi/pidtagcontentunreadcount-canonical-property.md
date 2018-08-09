---
title: Propiedad canónica PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819378"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propiedad canónica PidTagContentUnreadCount

  
  
**Hace referencia a**: Outlook 
  
Contiene el número de mensajes no leídos en una carpeta, como se calcula mediante el almacén de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificador:  <br/> |0x3603  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad calculada por el almacén de mensajes se usa para dos diferentes, aunque relacionados con fines. En un objeto de carpeta MAPI, que contiene el número de mensajes en una carpeta. En una fila de encabezado en tablas MAPI organizados por categorías, que contiene el número de mensajes no leídos no asociados en la categoría correspondiente a esa fila de encabezado.
  
Esta propiedad contiene el número de mensajes en la tabla de contenido de carpeta para la que no se establece la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). La propiedad **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contiene el número total de mensajes de la carpeta. El **PR_CONTENT_COUNT** y esta propiedad son de solo lectura a los clientes. 
  
Algunas aplicaciones cliente mostrar la fila de encabezado de una categoría de forma diferente según el valor de esta propiedad. Por ejemplo, un cliente puede mostrar una categoría que incluye los mensajes no leídos en negrita. Esta propiedad no se puede usar como una categoría y un intento para ello, los resultados en el valor MAPI_E_INVALID_PARAMETER que se devuelve el método [SortTable](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye las operaciones permitidas para los objetos de la tabla principal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

