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
ms.openlocfilehash: a315f1564f2980ad16ce2ba3da2308960f7d4b88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578895"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propiedad canónica PidTagDefaultProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un perfil de usuario de mensajería es el perfil predeterminado MAPI.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificador:  <br/> |0x3D04  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no aparece como una propiedad de cualquier objeto, pero sólo como una columna de una tabla de perfil. Una aplicación cliente puede usar el método [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) para designar el perfil predeterminado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

