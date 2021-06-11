---
title: Propiedad canónica PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339259"
---
# <a name="pidtagsubject-canonical-property"></a>Propiedad canónica PidTagSubject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el asunto completo de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0037  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se recomiendan en todos los objetos de mensaje. 
  
Estas propiedades son siempre el texto completo del asunto, es decir, la concatenación del prefijo y el asunto normalizado. Si no hay ningún prefijo, el asunto normalizado debe ser el mismo que el asunto. Un proveedor de transporte o almacén de mensajes usa estas propiedades y las propiedades **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) para calcular el asunto normalizado mediante la regla descrita **en PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
Las propiedades del asunto suelen ser pequeñas cadenas de menos de 256 caracteres y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **IStream** en ellas. El cliente siempre debe intentar el acceso a través de la interfaz **IMAPIProp** primero y recurrir a **IStream** solo si **MAPI_E_NOT_ENOUGH_MEMORY** se devuelve. 
  
Para un informe, esta propiedad contiene el asunto del mensaje original precedido por una cadena que indica lo que ha ocurrido con el mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
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

