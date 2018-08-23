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
ms.openlocfilehash: 4b26266e58a201b13aa178534039c9e07c900de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569501"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a>Propiedad canónica PidLidAppointmentMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de la reunión que va a generar a partir de la convocatoria de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptMessageClass  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Identificador de tipo Long (LID):  <br/> |0 x 00000024  <br/> |
|Tipo de datos:  <br/> |PT_TSTRING  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe ser "IPM. Cita"o el prefijo"IPM. Cita. ". Esta propiedad no es necesaria.
  
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

