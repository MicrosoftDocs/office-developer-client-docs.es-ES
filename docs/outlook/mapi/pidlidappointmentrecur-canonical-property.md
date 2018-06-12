---
title: Propiedad canónico PidLidAppointmentRecur
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818520"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propiedad canónico PidLidAppointmentRecur

  
  
**Se aplica a**: Outlook 
  
Especifica las fechas y horas cuando se produce una serie periódica mediante uno de los patrones de periodicidad y los intervalos que se especifican en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptRecur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008216  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad especifica las fechas y horas cuando una serie periódica se produce mediante uno de los patrones de periodicidad y rangos detalla en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como las fechas, asunto, ubicación y otras propiedades de excepciones. Los datos binarios en esta propiedad para los elementos de calendario periódicos se almacenan como la estructura de **AppointmentRecurrencePattern** . Esta propiedad no debe existir en los elementos de calendario de una sola instancia. 
  
Existen algunas limitaciones para las repeticiones:
  
- No deben iniciar varias instancias en el mismo día.
    
- No deben superponerse repeticiones. En concreto, debe producir una excepción que modifica la fecha de inicio de una instancia de la serie periódica en una fecha que se encuentra después del final de la instancia anterior y el inicio de la siguiente aparición de la serie periódica. El mismo es true si las instancias anteriores o siguiente de la serie periódica son excepciones.
    
La programación de una serie periódica está determinada por su patrón de periodicidad y el intervalo.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

