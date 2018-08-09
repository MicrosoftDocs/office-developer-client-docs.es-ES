---
title: Propiedad canónica PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819951"
---
# <a name="pidtagprofilename-canonical-property"></a>Propiedad canónica PidTagProfileName

  
  
**Hace referencia a**: Outlook 
  
Contiene el nombre del perfil.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D12  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Configuración de perfiles de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se calculan por los proveedores de servicio. Implementación de un proveedor de la función de **entrada de servicio** puede usar estas propiedades para descubrir el nombre del perfil. 
  
Aplicaciones cliente pueden utilizar estas propiedades como una alternativa cómoda a obtener el nombre del perfil mediante el examen de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la fila de tabla de estado del subsistema MAPI.
  
Estas propiedades no pueden ser únicas a través del tiempo, por ejemplo donde se elimina y más adelante vuelve a crear con el mismo nombre de un perfil. MAPI proporciona una propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente única en una sección de perfil codificado de forma rígida denominada **MUID_PROFILE_INSTANCE.**
  
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

