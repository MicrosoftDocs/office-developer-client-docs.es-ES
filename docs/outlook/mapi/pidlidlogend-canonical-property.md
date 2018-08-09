---
title: Propiedad canónica PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818789"
---
# <a name="pidlidlogend-canonical-property"></a>Propiedad canónica PidLidLogEnd

  
  
**Hace referencia a**: Outlook 
  
Representa la fecha de finalización y la hora para el mensaje de diario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidLogEnd  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Log  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008708  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Comentarios

La hora en que la actividad finalizó en hora Universal coordinada el (UTC), que debe ser igual a la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) y mayor o igual que la propiedad **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para diarios.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

