---
title: Propiedad canónica PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578874"
---
# <a name="pidtagformhostmap-canonical-property"></a>Propiedad canónica PidTagFormHostMap

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mapa de host de formularios disponibles. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FORM_HOST_MAP  <br/> |
|Identificador:  <br/> |0x3306  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Una aplicación de cliente debe actualizar esta propiedad, junto con la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), cuando se cambia la estructura subyacente en la interfaz de **IMAPIFormProp** . 
  
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

