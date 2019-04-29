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
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405418"
---
# <a name="pidtagminiicon-canonical-property"></a>Propiedad canónica PidTagMiniIcon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mapa de bits de un icono de tamaño medio de un formulario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MINI_ICON  <br/> |
|Identificador:  <br/> |0x0FFC  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene una imagen de 32 × 32 píxeles de un icono, que es la misma que el contenido de un. ICO, pero solo el extremo superior izquierdo de 16 x 16 píxeles se considera significativo. Normalmente, esta propiedad se copia desde el. Archivo ICO especificado en la línea SmallIcon de la sección [deScription] correspondiente del archivo de configuración de formulario.
  
 **Nota:** Algunas plataformas no admiten iconos de 16 x 16 píxeles. El formato 32 × 32 de esta propiedad se puede usar en este caso, pero las aplicaciones cliente deben tener en cuenta las incoherencias de la pantalla. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónica PidTagIcon](pidtagicon-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

