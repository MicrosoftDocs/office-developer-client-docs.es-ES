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
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327485"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propiedad canónica PidLidSharingFlavor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Designa como propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingFlavor  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A18  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser uno de los siguientes:
  
|**Valor**|**Tipo de objeto de mensaje de uso compartido**|
|:-----|:-----|
|0x00020310  <br/> |Una invitación para compartir para una carpeta especial.  <br/> |
|0x00000310  <br/> |Una invitación para compartir para una carpeta que no es una carpeta especial.  <br/> |
|0x00020500  <br/> |Una solicitud de uso compartido.  <br/> |
|0x00020710  <br/> |Tanto una invitación para compartir para una carpeta especial como una solicitud de uso compartido para la carpeta especial equivalente del destinatario.  <br/> |
|0x00025100  <br/> |Una respuesta para compartir que deniega una solicitud.  <br/> |
|0x00023310  <br/> |Una respuesta para compartir que acepta una solicitud (también un tipo de invitación para compartir).  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte carpetas de buzones entre clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

