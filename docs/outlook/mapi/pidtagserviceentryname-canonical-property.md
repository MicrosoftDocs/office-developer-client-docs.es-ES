---
title: Propiedad canónica PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820281"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propiedad canónica PidTagServiceEntryName

  
  
**Hace referencia a**: Outlook 
  
Contiene el nombre de la función de punto de entrada para la configuración de un servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificador:  <br/> |0x3D0B  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los implementadores de servicio de mensaje proporcionar un punto de entrada del servicio de mensaje, pero el punto de entrada no es necesario. Sin embargo, se debe proporcionar el punto de entrada sólo si existen las propiedades de configuración relacionados. Si no existen estas propiedades, MAPI se da por supuesto que no se proporciona ningún punto de entrada.
  
La biblioteca de vínculos dinámicos (DLL) en el que aparece la función de punto de entrada denominada por la propiedad **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Para obtener más información sobre puntos de entrada del servicio de mensajes, vea [implementar una función de punto de entrada de proveedor de servicio](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Recursos relacionados

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

