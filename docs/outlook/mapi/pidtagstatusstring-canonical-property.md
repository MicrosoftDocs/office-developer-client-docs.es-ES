---
title: Propiedad canónica PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8370a613162e3bc8d4395a18e9a7e177255b9b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567303"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propiedad canónica PidTagStatusString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mensaje que indica el estado actual de un recurso de la sesión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificador:  <br/> |0x3E08  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades proporcionan proveedores de servicios y la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicio en particular de MAPI. Esta propiedad se explica y proporciona información adicional acerca de un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Considerando que es necesario para todos los objetos de estado **PR_STATUS_CODE** , **PR_STATUS_STRING** y las propiedades asociadas son opcionales. Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado. 
  
La cadena se genera en el mismo lado de la llamada a procedimiento remoto como la cola MAPI; viajan a través de la memoria compartida en lugar de que se puede ordenar a través de un límite de proceso.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

