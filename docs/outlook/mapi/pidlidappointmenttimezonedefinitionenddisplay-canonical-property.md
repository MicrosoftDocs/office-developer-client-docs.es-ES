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
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de finalización de una cita o convocatoria de reunión de una sola instancia. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x0000825F  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Microsoft Office Outlook 2003 o anterior, y soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 y que no han ejecutado la herramienta de actualización de calendarios para Outlook o Microsoft Exchange Server, almacenan la hora de inicio y la hora de finalización de una sola instancia citas y convocatorias de reunión en la hora universal coordinada (UTC). Estos clientes no almacenan ninguna información para la zona horaria en la que se crea la cita o la convocatoria de reunión.
  
Las versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en CDO 1.2.1 que ejecutaban la herramienta de actualización de calendario de Outlook o Exchange Server usan **dispidApptTZDefEndDisplay** para almacenar la zona horaria para la hora de finalización. **dispidApptTZDefEndDisplay** muestra la cita o la reunión en la zona horaria original en la que se programó y determina si la hora de finalización debe ajustarse si las reglas de la zona horaria cambian. Si falta esta propiedad, se utiliza la zona horaria especificada por la propiedad **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)). Si **dispidApptTZDefStartDisplay** falta o no es válido, se supone que se trata de la zona horaria local actual. **dispidApptTZDefEndDisplay** se usa solo con fines de presentación y no se usa en la expansión de periodicidad. 
  
Un analizador debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefEndDisplay**o cuando continúa **TZDEFINITION** en una secuencia para que se comprometa a una propiedad binaria como **dispidApptTZDefEndDisplay**. Para obtener más información, vea [acerca de la persistencia de TZDEFINITION en una secuencia para confirmar una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** especifica la información de zona horaria para la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). El formato, las restricciones y el cálculo de **dispidApptTZDefEndDisplay** son los mismos que los especificados en la propiedad **dispidApptTZDefStartDisplay** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

