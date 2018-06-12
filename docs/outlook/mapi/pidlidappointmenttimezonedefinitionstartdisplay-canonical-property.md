---
title: Propiedad canónico PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818580"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propiedad canónico PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Se aplica a**: Outlook 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de inicio de una instancia única cita o convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x0000825E  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Notas

Microsoft Office Outlook 2003 o anterior y las soluciones que se basan en Collaboration Data Objects (CDO) 1.2.1 y que no se ejecuta la herramienta de actualización de calendario de Outlook o Microsoft Exchange Server, almacenan la hora de inicio y hora de finalización de instancia única las citas y las convocatorias de reunión en hora Universal coordinada (UTC). Estos clientes no almacene ninguna información para la zona horaria en la que se creó la convocatoria de reunión o cita.
  
Las versiones de Outlook con respecto a Microsoft Office Outlook 2007 y soluciones basadas en CDO 1.2.1 que han ejecutado la herramienta de actualización de calendario de Outlook o Exchange Server usan esta propiedad para almacenar la zona horaria de la hora de inicio. La propiedad **dispidApptTZDefStartDisplay** muestra la cita o reunión en la zona horaria original que se encontraba programado. Determina si se debe ajustar la hora de inicio si cambian las reglas de la zona horaria. Si falta esta propiedad, se supone la zona horaria local actual. Esta propiedad se utiliza únicamente con fines de presentación y no se usa en la expansión de periodicidad. 
  
Un analizador de debe tener cuidado cuando lee una secuencia obtenida de esta propiedad, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefStartDisplay**. Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Esta propiedad especifica la información de zona horaria de la propiedad **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). El valor de **dispidApptTZDefStartDisplay** se usa para convertir la fecha de inicio y la hora de la hora UTC a la zona horaria local para fines de presentación. Para cada **TZRULE** especificado por esta propiedad, no se debe establecer la marca TZRULE_FLAG_RECUR_CURRENT_TZREG. Por ejemplo, si la **TZRULE** es la regla eficaz, el valor del campo, **TZRULE** debe ser "0 x 0002"; de lo contrario, debe ser "0 x 0000". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones de protocolo relacionadas de Exchange Server..
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

