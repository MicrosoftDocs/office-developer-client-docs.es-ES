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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392126"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Propiedad canónica PidNameXSharingFlavor

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Representa el valor de la propiedad **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|||
|:-----|:-----|
|Nombres descriptivos:  <br/> |Ninguno  <br/> |
|Conjunto de propiedades:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nombre de la propiedad:  <br/> |Tipo de uso compartido de X  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Uso compartido  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad **dispidSharingFlavor** debe ser uno de los valores siguientes. 
  
|**Valor**|**Tipo de mensaje para compartir**|
|:-----|:-----|
|0x00020310  <br/> |Una invitación para compartir de una carpeta especial.  <br/> |
|0x00000310  <br/> |Una invitación para compartir de una carpeta que no es una carpeta especial.  <br/> |
|0x00020500  <br/> |Una solicitud para compartir.  <br/> |
|0x00020710  <br/> |Ambos una invitación para compartir una carpeta especial y una solicitud para compartir para la carpeta del destinatario equivalente especiales.  <br/> |
|0x00025100  <br/> |Una respuesta para compartir que se deniega una solicitud.  <br/> |
|0x00023310  <br/> |Una respuesta para compartir que acepta una solicitud (también un tipo de invitación de uso compartido).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte las carpetas de buzón de correo entre los clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

