---
title: Propiedad canónica PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321325"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propiedad canónica PidTagScheduleInfoAppointmentTombstone

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de bloques de datos que representan las reuniones que se han rechazado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificador:  <br/> |0x686A  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Disponibilidad  <br/> |
   
## <a name="remarks"></a>Comentarios

Los bloques de datos comienzan con un encabezado de valores de 32 bits definidos como:
  
|**Value**|**Descripción**|
|:-----|:-----|
|Identificador  <br/> |Este campo debe ser el valor 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Este campo debe tener el valor 0x00000014.  <br/> |
|Versión  <br/> |Este campo debe tener el valor 3.  <br/> |
|RecordsCount  <br/> |El número de registros que siguen.  <br/> |
|RecordsSize  <br/> |Este campo debe tener el valor 0x00000014.  <br/> |
   
El encabezado va seguido de **RecordsCount** entradas de valores de bit 32 definidos como: 
  
|**Value**|**Descripción**|
|:-----|:-----|
|StartTime  <br/> |La hora de inicio del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.  <br/> |
|EndTime  <br/> |La hora de finalización del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |El tamaño, en bytes, del campo GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |El valor de la propiedad **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la reunión que representa este registro.  <br/> |
|UserName  <br/> |Los primeros dos bytes son la longitud de la cadena PT_STRING8 que sigue.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

