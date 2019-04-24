---
title: Propiedad canónica PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345762"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Propiedad canónica PidLidResponseStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de respuesta de un asistente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidResponseStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008218  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentarios

El estado de respuesta debe ser uno de los valores de la tabla siguiente.
  
|**Estado de respuesta**|**Value**|**Descripción**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |No se requiere respuesta para este objeto. Este es el caso de objetos de cita y objetos de respuesta a la reunión.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Esta reunión pertenece al organizador.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Este valor en la reunión del asistente indica que el asistente aceptó provisionalmente la convocatoria de reunión.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Este valor en la reunión del asistente t indica que el asistente ha aceptado la convocatoria de reunión.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Este valor en la reunión del asistente indica que el asistente ha rechazado la convocatoria de reunión.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Este valor en la reunión del asistente indica que el asistente todavía no ha respondido. Este valor se encuentra en la convocatoria de reunión, la actualización de la reunión y la cancelación de la reunión.  <br/> |
   
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

