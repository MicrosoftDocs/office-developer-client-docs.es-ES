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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393372"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propiedad canónica PidLidAppointmentRecur

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica las fechas y horas cuando se produce una serie periódica mediante uno de los patrones de periodicidad y los intervalos que se especifican en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptRecur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008216  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica las fechas y horas cuando una serie periódica se produce mediante uno de los patrones de periodicidad y rangos detalla en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como las fechas, asunto, ubicación y otras propiedades de excepciones. Los datos binarios en esta propiedad para los elementos de calendario periódicos se almacenan como la estructura de **AppointmentRecurrencePattern** . Esta propiedad no debe existir en los elementos de calendario de una sola instancia. 
  
Existen algunas limitaciones para las repeticiones:
  
- No deben iniciar varias instancias en el mismo día.
    
- No deben superponerse repeticiones. En concreto, debe producir una excepción que modifica la fecha de inicio de una instancia de la serie periódica en una fecha que se encuentra después del final de la instancia anterior y el inicio de la siguiente aparición de la serie periódica. El mismo es true si las instancias anteriores o siguiente de la serie periódica son excepciones.
    
La programación de una serie periódica está determinada por su patrón de periodicidad y el intervalo.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

