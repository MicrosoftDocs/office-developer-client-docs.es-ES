---
title: Propiedad canónica PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355058"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Propiedad canónica PidTagReplyRecipientEntries

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de tamaño de identificadores de entrada para los destinatarios que van a obtener una respuesta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Identificador:  <br/> |0x004F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Sobre MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene una [estructura FLATENTRYLIST](flatentrylist.md) y no es una propiedad multivalor. 
  
Cuando esta propiedad no está presente, solo se envía una respuesta al usuario identificado por la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Cuando se definen esta y **las propiedades PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)), la respuesta se envía a todos los destinatarios identificados por estas dos propiedades. Un proveedor de transporte usa estas propiedades para invalidar la lógica de respuesta habitual.
  
Si esta propiedad o la **PR_REPLY_RECIPIENT_NAMES** está establecida, también se debe establecer la otra propiedad. Estas propiedades deben contener el mismo número de destinatarios y deben contenerlas en el mismo orden. Si no se cumplen estos requisitos, se pueden producir resultados impredecibles. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
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

