---
title: Propiedad canónica PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315025"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propiedad canónica PidNameRightsManagementLicense

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Almacena en caché la licencia de uso para el mensaje de correo electrónico administrado con derechos.
  
|||
|:-----|:-----|
|Nombres descriptivos:  <br/> |Ninguno  <br/> |
|Conjunto de propiedades:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nombre de la propiedad:  <br/> |DRMLicense  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Mensajería segura  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la propiedad está presente en un mensaje de correo electrónico administrado con derechos, el primer valor de esta propiedad binaria múltiple debe contener la licencia de uso comprimido ZLIB (como se especifica en [RFC1950]) para el mensaje de correo electrónico administrado con derechos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de los mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

