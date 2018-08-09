---
title: Propiedad canónica PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819687"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>Propiedad canónica PidTagLatestDeliveryTime

  
  
**Hace referencia a**: Outlook 
  
Contiene la última fecha y hora cuando un agente de transferencia de mensajes (MTA) debe entregar un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LATEST_DELIVERY_TIME  <br/> |
|Identificador:  <br/> |0x0019  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Si un MTA no puede entregar un mensaje por el tiempo que especifica esta propiedad, cancela el mensaje sin entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

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

