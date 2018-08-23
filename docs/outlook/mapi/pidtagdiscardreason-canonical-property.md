---
title: Propiedad canónica PidTagDiscardReason
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8835b7234a209d5cb80a19593632380f6d83826
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593161"
---
# <a name="pidtagdiscardreason-canonical-property"></a>Propiedad canónica PidTagDiscardReason

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un motivo por qué un agente de transferencia de mensajes (MTA) ha descartado un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISCARD_REASON  <br/> |
|Identificador:  <br/> |0x0011  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Sobres MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

La razón contenida en esta propiedad se usa en un informe de no entrega para el mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

