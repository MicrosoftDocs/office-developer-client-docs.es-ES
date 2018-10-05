---
title: Propiedad canónica PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388060"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>Propiedad canónica PidTagRecipientProposed

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Indica si ha respondido o asistente a una reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Identificador:  <br/> |0x5FE1  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Destinatario del transporte  <br/> |
   
## <a name="remarks"></a>Comentarios

Un valor de TRUE para esta propiedad indica que el Asistente propuesto una nueva fecha u hora. Un valor de FALSE, o la ausencia de esta propiedad, significa que el asistente no ha respondido todavía o la respuesta más reciente del asistente no incluye una nueva fecha / hora propuesta. Este valor no debe ser TRUE para los asistentes de una serie periódica.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
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

