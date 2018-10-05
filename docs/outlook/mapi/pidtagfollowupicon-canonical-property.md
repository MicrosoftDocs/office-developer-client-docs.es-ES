---
title: Propiedad canónica PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383523"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propiedad canónica PidTagFollowupIcon

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica el color del indicador del objeto de mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificador:  <br/> |0x1095  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Cambiar el nombre de la carpeta de mensajes  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no debe existir a menos que el valor de la propiedad **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) se establece en "followupFlagged", o el objeto de mensaje es un objeto relacionado con la reunión. Esta propiedad no debe existir en un objeto task. Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los valores siguientes.
  
|**Valor numérico**|**Nombre**|**Descripción**|
|:-----|:-----|:-----|
|No está presente  <br/> |N/D  <br/> |Sin color  <br/> |
|1  <br/> |followupIcon1  <br/> |Marca púrpura  <br/> |
|2  <br/> |followupIcon2  <br/> |Marca naranja  <br/> |
|3  <br/> |followupIcon3  <br/> |Marca verde  <br/> |
|4  <br/> |followupIcon4  <br/> |Marca amarilla  <br/> |
|5  <br/> |followupIcon5  <br/> |Marca azul  <br/> |
|6  <br/> |followupIcon6  <br/> |Marca roja  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
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

