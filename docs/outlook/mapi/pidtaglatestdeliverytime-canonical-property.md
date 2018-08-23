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
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590928"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>Propiedad canónica PidTagLatestDeliveryTime

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

