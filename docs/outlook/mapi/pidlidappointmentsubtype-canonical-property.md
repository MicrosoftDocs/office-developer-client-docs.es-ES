---
title: Propiedad canónica PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345419"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Propiedad canónica PidLidAppointmentSubType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si el evento es todo el día.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptSubType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Id. largo (LID):  <br/> |0x00008215  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica si el evento es un evento de todo el día, según lo especificado por el usuario. Un valor de TRUE indica que el evento es un evento de todo el día, en cuyo caso la hora de inicio y la hora de finalización deben ser medianoche, de modo que la duración sea de un múltiplo de 24 horas y de al menos 24 horas. Un valor de FALSE o la ausencia de esta propiedad indica que el evento no es un evento de todo el día. El cliente o el servidor no deben inferir el valor como TRUE cuando un usuario crea un evento de 24 horas, incluso si el evento se inicia y finaliza a medianoche.
  
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

