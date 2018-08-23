---
title: Propiedad canónica PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 78749a61bcbac64ded2c4791d9e239a12c38ce81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579049"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Propiedad canónica PidLidAppointmentSubType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si está o no el evento todo el día.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptSubType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008215  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica si el evento es un evento de día completo, tal como se especifica por el usuario. Un valor de TRUE indica que el evento es un evento de día completo, en cuyo caso la hora de inicio y hora de finalización deben ser medianoche para que la duración es un múltiplo de 24 horas y es de al menos 24 horas. Un valor de FALSE o la ausencia de esta propiedad indica que el evento no es un evento de día completo. El cliente o el servidor no debe inferir el valor como TRUE cuando ocurre un usuario crear un evento que es de 24 horas, incluso si el evento se inicia y termina en la medianoche.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

