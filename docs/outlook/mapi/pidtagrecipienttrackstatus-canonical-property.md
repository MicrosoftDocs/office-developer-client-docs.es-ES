---
title: Propiedad canónica PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820061"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Propiedad canónica PidTagRecipientTrackStatus

  
  
**Hace referencia a**: Outlook 
  
Indica el estado de respuesta devuelto por el asistente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Identificador:  <br/> |0x5FFF  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario del transporte  <br/> |
   
## <a name="remarks"></a>Comentarios

Si no se establece este valor, debe ser supone que ésta respNone. De lo contrario, debe ser uno de estos procedimientos:
  
|**Estado de la respuesta**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |No hay respuesta es necesaria para este objeto. Este es el caso de objetos de citas y objetos de respuesta de la reunión.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado provisionalmente la reunión objeto de solicitud.  <br/> |
|respAccepted  <br/> |0 x 00000003  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado la reunión objeto de solicitud.  <br/> |
|respDeclined  <br/> |0 x 00000004  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado la reunión objeto de solicitud.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

