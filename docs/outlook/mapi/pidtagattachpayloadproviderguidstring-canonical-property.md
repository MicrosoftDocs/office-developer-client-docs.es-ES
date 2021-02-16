---
title: Propiedad canónica PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361106"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>Propiedad canónica PidTagAttachPayloadProviderGuidString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor de un campo de encabezado MIME X-Payload-Provider-Guid.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|Identificador:  <br/> |0x3719  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el valor de estas propiedades, los clientes MIME deben escribir un campo de encabezado X-Payload-Provider-Guid en una entidad MIME que se analizará como datos adjuntos.
  
Los lectores MIME deben copiar este valor de campo de encabezado en el valor de la propiedad correspondiente. Los lectores MIME deben omitir este campo de encabezado cuando aparece en una entidad MIME que se analiza como un mensaje o cuerpo del mensaje, en lugar de como datos adjuntos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
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

