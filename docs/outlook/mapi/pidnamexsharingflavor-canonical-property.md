---
title: Propiedad canónica PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360889"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Propiedad canónica PidNameXSharingFlavor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa el valor de la **propiedad dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|||
|:-----|:-----|
|Nombres descriptivos:  <br/> |Ninguno  <br/> |
|Conjunto de propiedades:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nombre de la propiedad:  <br/> |X-Sharing-Flavor  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

La **propiedad dispidSharingFlavor** debe ser uno de los siguientes valores. 
  
|**Valor**|**Tipo de mensaje de uso compartido**|
|:-----|:-----|
|0x00020310  <br/> |Una invitación para compartir para una carpeta especial.  <br/> |
|0x00000310  <br/> |Una invitación para compartir para una carpeta que no es una carpeta especial.  <br/> |
|0x00020500  <br/> |Una solicitud de uso compartido.  <br/> |
|0x00020710  <br/> |Tanto una invitación para compartir para una carpeta especial como una solicitud de uso compartido para la carpeta especial equivalente del destinatario.  <br/> |
|0x00025100  <br/> |Respuesta de uso compartido que niega una solicitud.  <br/> |
|0x00023310  <br/> |Respuesta de uso compartido que acepta una solicitud (también un tipo de invitación para compartir).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte carpetas de buzones entre clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

