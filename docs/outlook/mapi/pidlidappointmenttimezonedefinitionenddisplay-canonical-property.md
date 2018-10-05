---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382753"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de finalización de una instancia única cita o convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x0000825F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Office Outlook 2003 o anterior y las soluciones que se basan en Collaboration Data Objects (CDO) 1.2.1 y que no se ejecuta la herramienta de actualización de calendario de Outlook o Microsoft Exchange Server, almacenan la hora de inicio y hora de finalización de instancia única las citas y las convocatorias de reunión en hora Universal coordinada (UTC). Estos clientes no almacene ninguna información para la zona horaria donde se crea la solicitud de reunión o cita.
  
Versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y soluciones basadas en CDO 1.2.1 que se han ejecutado el calendario de Outlook o Exchange Server la actualización de uso de herramienta **dispidApptTZDefEndDisplay** para almacenar la zona horaria para la hora de finalización. **dispidApptTZDefEndDisplay** muestra la cita o reunión en la zona horaria original que se ha programado y que determina si se debe ajustar la hora de finalización si cambian las reglas de la zona horaria. Si falta esta propiedad, se usa la zona horaria especificada por la propiedad **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)). Si **dispidApptTZDefStartDisplay** es falta o no es válida, se supone la zona horaria local actual. **dispidApptTZDefEndDisplay** se utiliza únicamente con fines de presentación y no se usa en la expansión de periodicidad. 
  
Un analizador de debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefEndDisplay**, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefEndDisplay**. Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** especifica la información de zona horaria de la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). El formato y las restricciones de cálculo de **dispidApptTZDefEndDisplay** son los mismos tal como se especifica en la propiedad **dispidApptTZDefStartDisplay** . 
  
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

