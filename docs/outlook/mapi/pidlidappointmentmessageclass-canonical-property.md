---
title: Propiedad canónica PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358103"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a>Propiedad canónica PidLidAppointmentMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de la reunión que se va a generar a partir de la solicitud de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptMessageClass  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000024  <br/> |
|Tipo de datos:  <br/> |PT_TSTRING  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser "IPM. Cita" o tener el prefijo "IPM. Cita.". Esta propiedad no es necesaria.
  
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

