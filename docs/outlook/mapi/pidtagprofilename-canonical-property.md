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
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341653"
---
# <a name="pidtagprofilename-canonical-property"></a>Propiedad canónica PidTagProfileName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre del perfil.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D12  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Configuración del perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades son calculadas por proveedores de servicios. La implementación de un proveedor de la función **ServiceEntry** puede usar estas propiedades para descubrir el nombre del perfil. 
  
Las aplicaciones cliente pueden usar estas propiedades como una alternativa cómoda para obtener el nombre del perfil mediante el examen de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la fila de la tabla de estado del subsistema MAPI.
  
Es posible que estas propiedades no sean únicas a lo largo del tiempo, por ejemplo, cuando se elimina un perfil y posteriormente se vuelve a crear con el mismo nombre. MAPI facilita una propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente única en una sección de perfil codificada de forma rígida denominada **MUID_PROFILE_INSTANCE.**
  
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

