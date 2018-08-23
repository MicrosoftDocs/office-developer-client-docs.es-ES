---
title: Propiedad canónica PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582255"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propiedad canónica PidTagServiceUid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la estructura [MAPIUID](mapiuid.md) para un servicio de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_UID  <br/> |
|Identificador:  <br/> |0x3D0C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se calcula mediante MAPI en los objetos de sección de perfil. MAPI utiliza para todos los proveedores que pertenecen al mismo servicio de mensajes de grupo. Esta propiedad se proporciona como un parámetro a la mayoría de los métodos de [IMsgServiceAdmin](imsgserviceadminiunknown.md) . No debe aparecer en Mapisvc.inf. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

