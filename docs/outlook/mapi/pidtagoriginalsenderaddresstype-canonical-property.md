---
title: Propiedad canónica PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342682"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a>Propiedad canónica PidTagOriginalSenderAddressType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de dirección del remitente de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W  <br/> |
|Identificador:  <br/> |0x0066  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son ejemplos de las propiedades de dirección del remitente original de un mensaje. En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor **de PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)). Nunca se cambia cuando el mensaje se reenvía o se responde.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
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

