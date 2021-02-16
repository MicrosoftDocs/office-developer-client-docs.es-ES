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
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339231"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propiedad canónica PidTagSubjectPrefix

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un prefijo de asunto que normalmente indica alguna acción en un mensaje, como "FW: " para el reenvío. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificador:  <br/> |0x003D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se recomiendan en todos los objetos de mensaje. 
  
El prefijo de asunto consta de uno o más caracteres alfanuméricos, seguidos de dos puntos y un espacio (que forman parte del prefijo). No debe contener caracteres no alfanuméricos delante de los dos puntos. La ausencia de un prefijo se puede representar con una cadena vacía o con esta propiedad que no se establece. 
  
Si estas propiedades se establecen explícitamente, la cadena puede tener cualquier longitud y usar cualquier carácter alfanumérico, pero debe coincidir con una subcadena al principio de la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Si el remitente no establece estas propiedades y deben calcularse, su contenido está más restringido. La regla para calcular el prefijo es que **PR_SUBJECT** debe comenzar con una, dos o tres letras (solo alfabética) seguidas de dos puntos y un espacio. Si dicha subcadena se encuentra al principio de **PR_SUBJECT**, se convierte en la cadena de estas propiedades (y también permanece al principio de **PR_SUBJECT**). De lo contrario, estas propiedades permanecen sin conjunto. 
  
Estas propiedades **y PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) deben calcularse como parte de la [implementación de IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Un cliente no debe solicitar a [IMAPIProp::GetProps](imapiprop-getprops.md) sus valores hasta que se hayan confirmado mediante una llamada **IMAPIProp::SaveChanges.** 
  
Las propiedades de asunto suelen ser cadenas pequeñas de menos de 256 caracteres y un proveedor de almacenamiento de mensajes no está obligado a admitir la interfaz **OLE IStream** en ellas. Un cliente siempre debe intentar obtener acceso a través de la interfaz **IMAPIProp** en primer lugar y recurrir a **IStream** solo si MAPI_E_NOT_ENOUGH_MEMORY **se** devuelve. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

