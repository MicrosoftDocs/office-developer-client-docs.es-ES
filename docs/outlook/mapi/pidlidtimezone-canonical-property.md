---
title: Propiedad canónica PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389928"
---
# <a name="pidlidtimezone-canonical-property"></a>Propiedad canónica PidLidTimeZone

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica información acerca de la zona horaria de una reunión periódica.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |LID_TIME_ZONE  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x0000000C  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es de sólo lectura si no se establece la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)), pero si la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) es TRUE y la **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) la propiedad es FALSE. La palabra inferior especifica un índice en una tabla que contiene la información de zona horaria. Desde la palabra superior, es de lectura sólo el bit más alto. Si ese bit está establecido, a continuación, la zona horaria que hace referencia no observará se seguirá el horario de verano (DST), en caso contrario, las fechas de horario de verano se detallan en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) . 
  
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

