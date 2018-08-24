---
title: Propiedad canónica PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589780"
---
# <a name="pidtagminiicon-canonical-property"></a>Propiedad canónica PidTagMiniIcon

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un mapa de bits de un icono de tamaño para un formulario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MINI_ICON  <br/> |
|Identificador:  <br/> |0x0FFC  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene una imagen de 32 x 32 píxeles de un icono, el mismo que el contenido de una. Archivo ICO, pero sólo los píxeles de la parte superior izquierda de 16 x 16 se consideran importantes. Esta propiedad normalmente se copia desde el. Archivo ICO especificado en la línea de iconos de la sección [descripción] adecuada del archivo de configuración de formulario.
  
 **Nota** Algunas plataformas hacer no los iconos de compatibilidad de 16 x 16 píxeles. El formato de 32 x 32 de esta propiedad es utilizable en tal caso, pero las aplicaciones cliente deben tener en cuenta las incoherencias de presentación. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagIcon](pidtagicon-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

