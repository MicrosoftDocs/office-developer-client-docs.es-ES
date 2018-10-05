---
title: Propiedad canónica PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386946"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a>Propiedad canónica PidLidNonSendableBccTrackStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor para cada asistente que aparece en la propiedad **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidNonSendBccTrackStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008545  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableBCC** . El número de valores de esta propiedad debe ser igual que el número de valores en el **dispidNonSendableBCC**. Cada valor de esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableBCC** en el mismo índice. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

