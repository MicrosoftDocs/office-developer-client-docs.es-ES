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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316285"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Propiedad canónica PidTagFollowupIcon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el color de marca del objeto de mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Identificador:  <br/> |0x1095  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Cambiar el nombre de la carpeta del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no debe existir a menos que el valor de la propiedad **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) esté establecido en "followupFlagged" o el objeto de mensaje sea un objeto relacionado con la reunión. Esta propiedad no debe existir en un objeto de tarea. Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores.
  
|**Valor numérico**|**Nombre**|**Descripción**|
|:-----|:-----|:-----|
|No presente  <br/> |N/D  <br/> |Sin color  <br/> |
|1   <br/> |followupIcon1  <br/> |Marca púrpura  <br/> |
|2   <br/> |followupIcon2  <br/> |Marca naranja  <br/> |
|3   <br/> |followupIcon3  <br/> |Marca verde  <br/> |
|4   <br/> |followupIcon4  <br/> |Marca amarilla  <br/> |
|5   <br/> |followupIcon5  <br/> |Marca azul  <br/> |
|6   <br/> |followupIcon6  <br/> |Marca roja  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

