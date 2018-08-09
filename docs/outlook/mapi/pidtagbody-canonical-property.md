---
title: Propiedad canónica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819265"
---
# <a name="pidtagbody-canonical-property"></a>Propiedad canónica PidTagBody

  
  
**Hace referencia a**: Outlook 
  
Contiene el texto del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificador:  <br/> |0 x 1000  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se suelen usar sólo en un mensaje interpersonal (IPM). 
  
Almacenes de mensaje que admiten el formato de texto enriquecido (RTF) omitir los cambios realizados en el espacio en blanco en el texto del mensaje. Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la versión RTF del texto del mensaje. Si posteriormente se llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y **PR_BODY** se ha modificado, el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión RTF. Si sólo se ha cambiado el espacio en blanco, las propiedades se dejan sin cambios. Esto significa que mantiene cualquier RTF no trivial formato cuando el mensaje se transmite a través de clientes ajenos a RTF y sistemas de mensajería. 
  
El valor de esta propiedad debe expresarse en la página de códigos del sistema operativo que se está ejecutando MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

