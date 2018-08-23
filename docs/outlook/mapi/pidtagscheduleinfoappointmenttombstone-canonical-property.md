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
ms.openlocfilehash: e554a496dd1869dd7c07b315d92a136676e05006
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590046"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propiedad canónica PidTagScheduleInfoAppointmentTombstone

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de bloques de datos que representan las reuniones que se hayan rechazado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificador:  <br/> |0x686A  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libre/ocupado  <br/> |
   
## <a name="remarks"></a>Comentarios

Los bloques de datos comienzan con un encabezado de valores de 32 bits definido como:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Identificador  <br/> |Este campo debe ser el valor 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Este campo debe tener el valor 0x00000014.  <br/> |
|Versión  <br/> |Este campo debe tener el valor 3.  <br/> |
|RecordsCount  <br/> |El número de registros que le siguen.  <br/> |
|RecordsSize  <br/> |Este campo debe tener el valor 0x00000014.  <br/> |
   
El encabezado es seguido por **RecordsCount** entradas de valores de 32 bits definidos como: 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|StartTime  <br/> |Hora de comienzo del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.  <br/> |
|EndTime  <br/> |Hora de finalización del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |El tamaño, en bytes, del campo GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |Representa el valor de la propiedad **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la reunión este registro.  <br/> |
|UserName  <br/> |Los dos primeros bytes son la longitud de la cadena de PT_STRING8 que sigue.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

