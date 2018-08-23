---
title: Propiedad canónica PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e05144beeac8318b8c28153461742a491698996
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576634"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Propiedad canónica PidLidAppointmentAuxiliaryFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un campo de bits que describe el estado del objeto auxiliar.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptAuxFlags  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008207  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no es necesaria. A continuación se muestran los indicadores individuales que se pueden establecer.
  
C (auxApptFlagCopied, 0 x 00000001)
  
> Esta marca indica que el objeto de calendario se copió desde otra carpeta de calendario.
    
R (auxApptFlagForceMtgResponse, 0 x 00000002)
  
> Esta marca en una convocatoria de reunión indica que el cliente o el servidor debe enviar una respuesta de reunión al organizador cuando se elige una respuesta.
    
F (auxApptFlagForwarded, 0 x 00000004)
  
> Esta marca en una convocatoria de reunión indica que se reenvió (incluidos se reenvíen por el organizador), en lugar de ser una invitación del organizador.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

