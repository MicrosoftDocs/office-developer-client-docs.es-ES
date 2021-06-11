---
title: Propiedad canónica PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355177"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Propiedad canónica PidTagReplyRecipientNames

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de nombres para mostrar para los destinatarios que van a obtener una respuesta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Identificador:  <br/> |0x0050  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Sobre MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades contienen los nombres para mostrar separados por punto y coma.
  
Cuando esta propiedad no está presente, solo se envía una respuesta al usuario identificado por la propiedad **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Cuando **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) y estas propiedades se definen, la respuesta se envía a todos los destinatarios identificados por estas dos propiedades. Un proveedor de transporte usa estas propiedades para invalidar la lógica de respuesta habitual.
  
Si se **PR_REPLY_RECIPIENT_ENTRIES** o estas propiedades están establecidas, también se debe establecer la otra propiedad. Estas propiedades deben contener el mismo número de destinatarios y deben contenerlas en el mismo orden. Si no se cumplen estos requisitos, se pueden producir resultados impredecibles. 
  
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

