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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345384"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de finalización de una cita de instancia única o una solicitud de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Id. largo (LID):  <br/> |0x0000825F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Office Outlook 2003 o versiones anteriores y soluciones basadas en objetos de datos de colaboración (CDO) 1.2.1 y que no han ejecutado la herramienta de actualización de calendario para Outlook o Microsoft Exchange Server, almacene la hora de inicio y la hora de finalización de las citas de instancia única y las solicitudes de reunión en la hora universal coordinada (UTC). Estos clientes no almacenan información sobre la zona horaria donde se crea la cita o la solicitud de reunión.
  
Las versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en CDO 1.2.1 que han ejecutado la herramienta de actualización de calendario Outlook o Exchange Server usan **dispidApptTZDefEndDisplay** para almacenar la zona horaria para la hora de finalización. **dispidApptTZDefEndDisplay** muestra la cita o reunión en la zona horaria original que se programó y determina si se debe ajustar la hora de finalización si cambian las reglas de la zona horaria. Si falta esta propiedad, se usa la zona horaria especificada por la **propiedad dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)). Si **falta dispidApptTZDefStartDisplay** o no es válido, se supone que la zona horaria local actual. **dispidApptTZDefEndDisplay** solo se usa con fines de presentación y no se usa en la expansión de periodicidad. 
  
Un analizador debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefEndDisplay**, o cuando persiste **TZDEFINITION** en una secuencia para el compromiso con una propiedad binaria como **dispidApptTZDefEndDisplay**. Para obtener más información, vea [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** especifica la información de zona horaria para la **propiedad dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). El formato, las restricciones y el cálculo de **dispidApptTZDefEndDisplay** son los mismos que se especifican en la **propiedad dispidApptTZDefStartDisplay.** 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

