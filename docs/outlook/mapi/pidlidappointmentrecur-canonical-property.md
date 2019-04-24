---
title: Propiedad canónica PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331783"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propiedad canónica PidLidAppointmentRecur

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la fecha y la hora en que tiene lugar una serie periódica mediante uno de los intervalos y patrones de periodicidad especificados en [[ms-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptRecur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008216  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica la fecha y la hora en que tiene lugar una serie periódica mediante uno de los intervalos y patrones de periodicidad descritos en [[ms-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como fechas, asunto, ubicación y otras propiedades de las excepciones. Los datos binarios de esta propiedad para los elementos de calendario periódicos se almacenan como la estructura **AppointmentRecurrencePattern** . Esta propiedad no debe existir en elementos de calendario de instancia única. 
  
Hay algunas limitaciones en la periodicidad:
  
- No se deben iniciar varias instancias en el mismo día.
    
- Las rePeticiones no deben superponerse. Concretamente, una excepción que modifica la fecha de inicio de una instancia de la serie periódica debe producirse en una fecha posterior al final de la instancia anterior y el inicio de la siguiente repetición de la serie periódica. Lo mismo sucede si las instancias anteriores o siguientes de la serie periódica son excepciones.
    
La programación de una serie periódica viene determinada por su patrón y intervalo de periodicidad.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para el correo electrónico y otros recordatorios de objetos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

