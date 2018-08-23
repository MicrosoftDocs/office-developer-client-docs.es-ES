---
title: Propiedad canónica PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30c8f31c104be52da2900eb81c7b7c29dfa55015
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586532"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>Propiedad canónica PidTagFormDesignerGuid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador único para el objeto que se utiliza para diseñar un formulario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|Identificador:  <br/> |0x3309  <br/> |
|Tipo de datos:  <br/> |PT_GUID  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Normalmente, esta propiedad contiene el identificador único global (GUID) del programa de diseño que se usa para crear el formulario. Esta propiedad puede estar vacía. 
  
La estructura [MAPIUID](mapiuid.md) contiene la definición del identificador único. 
  
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

