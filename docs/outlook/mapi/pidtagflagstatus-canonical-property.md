---
title: Propiedad canónica PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390558"
---
# <a name="pidtagflagstatus-canonical-property"></a>Propiedad canónica PidTagFlagStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de marca del objeto de mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FLAG_STATUS  <br/> |
|Identificador:  <br/> |0x1090  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no debe existir en un objeto relacionado con la reunión y no debe existir en un objeto task. Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores:
  
|**Valor numérico**|**Nombre**|**Descripción**|
|:-----|:-----|:-----|
|No está presente  <br/> |N/D  <br/> |Sin marca  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Marcar como completado  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Marca  <br/> |
   
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

