---
title: Propiedad canónica PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385539"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Propiedad canónica PidTagUserX509Certificate

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene los certificados de seguridad X.509 versión 3 para un usuario de mensajería. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x3A70  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Usuario de correo MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa en aplicaciones que utilizan la seguridad de clave pública. Contiene una representación binaria uno o más X.509 versión 3 de certificados de seguridad. 
  
Diversas aplicaciones y los clientes pueden utilizar esta propiedad para sus propios certificados de seguridad. El formato binario de los datos X.509 puede variar entre los distintos proveedores. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
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

