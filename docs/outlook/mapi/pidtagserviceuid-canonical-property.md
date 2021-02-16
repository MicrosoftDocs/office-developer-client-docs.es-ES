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
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426530"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propiedad canónica PidTagServiceUid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la [estructura MAPIUID](mapiuid.md) de un servicio de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_UID  <br/> |
|Identificador:  <br/> |0x3D0C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI calcula esta propiedad en objetos de sección de perfil. MAPI lo usa para agrupar todos los proveedores que pertenecen al mismo servicio de mensajes. Esta propiedad se proporciona como un parámetro para la mayoría de los [métodos IMsgServiceAdmin.](imsgserviceadminiunknown.md) No debe aparecer en Mapisvc.inf. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

