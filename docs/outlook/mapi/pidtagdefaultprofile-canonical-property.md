---
title: Propiedad canónica PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428777"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propiedad canónica PidTagDefaultProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un perfil de usuario de mensajería es el perfil predeterminado de MAPI.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificador:  <br/> |0x3D04  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no aparece como una propiedad de ningún objeto, sino solo como una columna de una tabla de perfil. Una aplicación cliente puede usar el [método IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) para designar el perfil predeterminado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

