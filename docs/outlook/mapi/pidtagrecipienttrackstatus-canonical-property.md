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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355289"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Propiedad canónica PidTagRecipientTrackStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el estado de respuesta devuelto por el asistente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Identificador:  <br/> |0x5FFF  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario de transporte  <br/> |
   
## <a name="remarks"></a>Comentarios

Si no se establece este valor, debe considerarse respNone. De lo contrario, debe ser uno de los siguientes:
  
|**Estado de respuesta**|**Value**|**Descripción**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |No se requiere respuesta para este objeto. Este es el caso de objetos de cita y objetos de respuesta a la reunión.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente aceptó provisionalmente el objeto convocatoria de reunión.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado el objeto convocatoria de reunión.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado el objeto de convocatoria de reunión.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

