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
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422778"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propiedad canónica PidTagProviderUid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una estructura **MAPIUID** del proveedor de servicios que controla un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_UID  <br/> |
|Identificador:  <br/> |0x300C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Common MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad la calculan todos los proveedores de servicios. Contiene una estructura [MAPIUID](mapiuid.md) asociada y, normalmente, codificada de forma rígida por el proveedor. Lo suele usar una aplicación cliente que está interesada en solo los contenedores de la libreta de direcciones suministrados por un proveedor en particular. 
  
Esta propiedad aparece sólo como una entrada de columna en la tabla del proveedor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

