---
title: Propiedad canónica PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818908"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propiedad canónica PidLidSharingFlavor

  
  
**Hace referencia a**: Outlook 
  
Designa como una propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingFlavor  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008A18  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Uso compartido  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser una de las siguientes opciones:
  
|**Valor**|**Tipo de objeto de mensaje de uso compartido**|
|:-----|:-----|
|0x00020310  <br/> |Una invitación para compartir de una carpeta especial.  <br/> |
|0x00000310  <br/> |Una invitación para compartir de una carpeta que no es una carpeta especial.  <br/> |
|0x00020500  <br/> |Una solicitud para compartir.  <br/> |
|0x00020710  <br/> |Ambos una invitación para compartir una carpeta especial y una solicitud para compartir para la carpeta del destinatario equivalente especiales.  <br/> |
|0x00025100  <br/> |Una respuesta para compartir la denegación de una solicitud.  <br/> |
|0x00023310  <br/> |Una respuesta para compartir aceptación de una solicitud (también un tipo de invitación de uso compartido).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte las carpetas de buzón de correo entre los clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

