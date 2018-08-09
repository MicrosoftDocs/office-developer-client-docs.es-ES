---
title: Propiedad canónica PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818793"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propiedad canónica PidLidMeetingType

  
  
**Hace referencia a**: Outlook 
  
Indica el tipo de convocatoria de reunión o una actualización de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidMeetingType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00000026  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe establecerse en uno de estos procedimientos:
  
|**Propiedad**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |No se especifica.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Convocatoria de reunión inicial.  <br/> |
|mtgFull  <br/> |0 x 00010000  <br/> |Actualización completa.  <br/> |
|mtgInfo  <br/> |0 x 00020000  <br/> |Información de la actualización.  <br/> |
|mtgOutOfDate  <br/> |0 x 00080000  <br/> |Una convocatoria de reunión más reciente o la actualización de la reunión se recibió después de éste.  <br/> |
|mtgDelegatorCopy  <br/> |0 x 00100000  <br/> |Esto se establece en la copia de la persona que delega cuando un objetos relacionados con la reunión de identificadores de delegado.  <br/> |
   
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

