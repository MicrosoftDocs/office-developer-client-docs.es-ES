---
title: Propiedad canónica PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818559"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>Propiedad canónica PidLidAppointmentStateFlags

  
  
**Hace referencia a**: Outlook 
  
Especifica un campo de bits que describe el estado del objeto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptStateFlags  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008217  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no es necesaria. A continuación se muestran los indicadores individuales que se pueden establecer.
  
M (asfMeeting, 0 x 00000001)
  
> Esta marca indica que el objeto es un objeto de la reunión o un objeto relacionado con la reunión.
    
R (asfReceived, 0 x 00000002)
  
> Esta marca indica que se ha recibido el objeto representado de otra persona.
    
C (asfCanceled, 0 x 00000004)
  
> Esta marca indica que se ha cancelado el objeto de reunión representado por el objeto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

