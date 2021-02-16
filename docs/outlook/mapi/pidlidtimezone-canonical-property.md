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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319274"
---
# <a name="pidlidtimezone-canonical-property"></a>Propiedad canónica PidLidTimeZone

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica información sobre la zona horaria de una reunión periódica.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |LID_TIME_ZONE  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x0000000C  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad solo se lee si la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) no está establecida, pero si la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) es TRUE y la propiedad **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) es FALSE. Word inferior especifica un índice en una tabla que contiene información de zona horaria. Desde la parte superior de WORD, solo se lee el bit más alto. Si se establece ese bit, la zona horaria a la que se hace referencia no observará el horario de verano (DST), de lo contrario se seguirán las fechas de horario de verano detalladas en [[MS-OLICOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

