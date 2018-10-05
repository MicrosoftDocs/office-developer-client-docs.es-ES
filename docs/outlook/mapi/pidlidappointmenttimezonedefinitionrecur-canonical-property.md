---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389305"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se crea una cita periódica o una convocatoria de reunión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptTZDefRecur  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008260  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 que se han ejecutado el calendario de Outlook o Exchange Server actualización de uso de la herramienta el **dispidApptTZDefRecur** y ** dispidTimeZoneStruct** propiedades ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar si se debe ajustar la reunión periódica si cambian las reglas de la zona horaria. Estas propiedades se deben sincronizarse, debido a que los clientes más antiguos aún pueden manipular la propiedad **dispidTimeZoneStruct** . Para detectar si se sincronizan las dos propiedades, el miembro **wFlags** para la regla que coincide con **dispidTimeZoneStruct** debe tener el indicador TZRULE_FLAG_RECUR_CURRENT_TZREG establecido. Si no se establece este marcador, o se establece y la regla en la propiedad **dispidTimeZoneStruct** no coincide con la regla de marcado, la propiedad **dispidApptTZDefRecur** debe descartarse y **dispidTimeZoneStruct** debe usarse en su lugar. 
  
Al escribir las propiedades de la **dispidApptTZDefRecur** y la **dispidTimeZoneStruct** a una nueva reunión periódica o, cuando se realiza una opción para usar la propiedad **dispidTimeZoneStruct** , la definición actual para la zona horaria (arbitraria debe usarse según el registro de Windows). 
  
Un analizador de debe tener cuidado cuando lee una secuencia que se obtiene de **dispidApptTZDefRecur**, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefRecur**. Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** especifica la información de zona horaria que se describe el procedimiento para convertir la fecha de la reunión y la hora en una serie periódica y de la hora Universal coordinada (UTC). Si se establece esta propiedad, pero tiene datos que no es coherentes con los datos representados por **dispidTimeZoneStruct**, el cliente debe utilizar **dispidTimeZoneStruct** en lugar de **dispidApptTZDefRecur**. Si **dispidApptTZDefRecur** no está establecida, la propiedad **PidLidTimeZoneStruct** se usará en su lugar. Los campos de este BLOB se codifican en orden de bytes little-endian. 
  
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

