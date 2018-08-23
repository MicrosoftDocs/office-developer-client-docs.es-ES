---
title: Propiedad canónica PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ffc47eca3457eef876d88a4be43888f24c403b10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575346"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propiedad canónica PidTagSubjectPrefix

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un prefijo de asunto que indica normalmente alguna acción en un mensaje, como "Rv:" para el reenvío. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificador:  <br/> |0x003D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda utilizar estas propiedades en todos los objetos de mensaje. 
  
El prefijo del asunto consta de uno o más caracteres alfanuméricos, seguidos de un punto y coma y un espacio (que forman parte del prefijo). No debe contener todos los caracteres no alfanuméricos antes de los dos puntos. Ausencia de un prefijo puede estar representada por una cadena vacía o por esta propiedad no está establecido. 
  
Si estas propiedades se establecen de forma explícita, la cadena puede ser de cualquier longitud y usar caracteres alfanuméricos, pero debe coincidir con una subcadena al principio de la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Si estas propiedades no se han establecido por el remitente y deben calcularse, su contenido es más restringido. La regla de la informática el prefijo es que **PR_SUBJECT** debe comenzar con uno, dos o tres letras (alfabéticos sólo) seguido de un punto y coma y un espacio. Si se encuentra dicha una subcadena al principio del **PR_SUBJECT**, a continuación, se convierte en la cadena para estas propiedades (y también permanece al principio del **PR_SUBJECT**). De lo contrario, estas propiedades permanecen sin establecer. 
  
Estas propiedades y **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) se deben calcular como parte de la implementación de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Un cliente no debe solicitar [IMAPIProp::GetProps](imapiprop-getprops.md) para sus valores hasta que se hayan confirmado por una llamada **IMAPIProp::SaveChanges** . 
  
Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **IStream** OLE en ellos. Un cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve **MAPI_E_NOT_ENOUGH_MEMORY** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

