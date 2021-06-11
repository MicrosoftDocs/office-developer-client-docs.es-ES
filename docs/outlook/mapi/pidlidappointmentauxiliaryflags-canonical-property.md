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
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345433"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Propiedad canónica PidLidAppointmentAuxiliaryFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un campo de bits que describe el estado auxiliar del objeto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptAuxFlags  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Id. largo (LID):  <br/> |0x00008207  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no es necesaria. A continuación se muestran las marcas individuales que se pueden establecer.
  
C (auxApptFlagCopied, 0x00000001)
  
> Esta marca indica que el objeto calendar se copió de otra carpeta de calendario.
    
R (auxApptFlagForceMtgResponse, 0x00000002)
  
> Esta marca en una solicitud de reunión indica que el cliente o servidor debe enviar una respuesta de reunión al organizador cuando se elige una respuesta.
    
F (auxApptFlagForwarded, 0x00000004)
  
> Esta marca en una solicitud de reunión indica que se reenvía (incluida la reenviada por el organizador), en lugar de ser una invitación del organizador.
    
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

