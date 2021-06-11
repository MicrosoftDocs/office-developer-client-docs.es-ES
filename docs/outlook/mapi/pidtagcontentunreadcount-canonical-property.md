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
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331874"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propiedad canónica PidTagContentUnreadCount

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el número de mensajes no leídos de una carpeta, tal como lo calcula el almacén de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificador:  <br/> |0x3603  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Carpeta  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad calculada por el almacén de mensajes se usa para dos propósitos diferentes, aunque relacionados. En un objeto de carpeta MAPI, contiene el número de mensajes de una carpeta. En una fila de encabezado en tablas MAPI categorizadas, contiene el número de mensajes no leídos no asociados en la categoría correspondiente a esa fila de título.
  
Esta propiedad contiene el número de mensajes de la tabla de contenido de carpeta para los que no se establece la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). La **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contiene el recuento total de mensajes de la carpeta. El **PR_CONTENT_COUNT** y esta propiedad son de solo lectura para los clientes. 
  
Algunas aplicaciones cliente muestran la fila de encabezado de una categoría de forma diferente en función del valor de esta propiedad. Por ejemplo, un cliente puede mostrar una categoría que incluye mensajes no leídos en negrita. Esta propiedad no se puede usar como categoría y un intento de hacerlo da como resultado que se devuelva el valor MAPI_E_INVALID_PARAMETER del método [IMAPITable::SortTable.](imapitable-sorttable.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye operaciones permitidas para los objetos de tabla principal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

