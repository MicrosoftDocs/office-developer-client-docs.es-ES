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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351075"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propiedad canónica PidTagServiceEntryName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de la función de punto de entrada para la configuración de un servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificador:  <br/> |0x3D0B  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los implementadores del servicio de mensajes proporcionen un punto de entrada al servicio de mensajes, pero el punto de entrada no es necesario. Sin embargo, el punto de entrada solo debe proporcionarse si existen las propiedades de configuración relacionadas. Si no existen estas propiedades, MAPI supone que no se proporciona ningún punto de entrada.
  
La biblioteca de vínculos dinámicos (DLL) en la que aparece la función de punto de entrada se nombra mediante la propiedad **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Para obtener más información acerca de los puntos de entrada del servicio de mensajes, consulte [implementar una función de punto de entrada de proveedor de servicios](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

