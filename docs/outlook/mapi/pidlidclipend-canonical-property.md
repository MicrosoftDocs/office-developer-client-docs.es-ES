---
title: Propiedad canónica PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386071"
---
# <a name="pidlidclipend-canonical-property"></a>Propiedad canónica PidLidClipEnd

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica la fecha de finalización y la hora del evento en hora Universal coordinada (UTC) para los objetos de calendario de una sola instancia. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidClipEnd  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008236  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Para los objetos de calendario de una sola instancia, especifica la fecha de finalización y la hora del evento en UTC. Para una serie periódica, esta propiedad especifica medianoche en la fecha de la última instancia de la serie periódica en UTC, a menos que la serie periódica no tiene fin, en el que caso el valor debe ser el 31 de agosto 4500, 11:59 p.m.
  
El valor de esta propiedad debe establecerse en el valor de la **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).
  
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

