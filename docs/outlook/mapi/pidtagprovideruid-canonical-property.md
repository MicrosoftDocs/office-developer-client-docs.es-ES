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
  
Contiene una **estructura MAPIUID** del proveedor de servicios que administra un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_UID  <br/> |
|Identificador:  <br/> |0x300C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI común  <br/> |
   
## <a name="remarks"></a>Comentarios

Todos los proveedores de servicios calculan esta propiedad. Contiene una estructura [MAPIUID](mapiuid.md) asociada al proveedor y, por lo general, codificada de forma hard. Normalmente lo usa una aplicación cliente que está interesada en solo los contenedores de libreta de direcciones proporcionados por un proveedor determinado. 
  
Esta propiedad solo aparece como una entrada de columna en la tabla del proveedor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

