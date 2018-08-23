---
title: Propiedad canónica PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581058"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propiedad canónica PidTagProviderUid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una estructura **MAPIUID** del proveedor de servicios que se encarga de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_UID  <br/> |
|Identificador:  <br/> |0x300C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se calcula por todos los proveedores de servicio. Contiene una estructura [MAPIUID](mapiuid.md) asociada y normalmente codificado de forma rígida por el proveedor. Normalmente se usa por una aplicación cliente que está interesada en sólo los contenedores de la libreta de direcciones proporcionados por un proveedor concreto. 
  
Esta propiedad aparece sólo como una entrada de la columna en la tabla proveedor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

