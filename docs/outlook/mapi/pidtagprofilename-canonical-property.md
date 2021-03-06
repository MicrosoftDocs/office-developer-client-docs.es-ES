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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435652"
---
# <a name="pidtagprofilename-canonical-property"></a>Propiedad canónica PidTagProfileName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre del perfil.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D12  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Configuración de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estos proveedores de servicios calculan estas propiedades. La implementación de la función **ServiceEntry** de un proveedor puede usar estas propiedades para detectar el nombre del perfil. 
  
Las aplicaciones cliente pueden usar estas propiedades como una alternativa conveniente para obtener el nombre del perfil examinando la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la fila de tabla de estado del subsistema MAPI.
  
Es posible que estas propiedades no sean únicas a lo largo del tiempo, por ejemplo, cuando se elimina un perfil y posteriormente se vuelve a crear con el mismo nombre. MAPI proporciona una propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente única en una sección de perfil codificado de forma **MUID_PROFILE_INSTANCE.**
  
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

