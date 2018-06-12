---
title: Propiedad canónico PidTagStatusString
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820331"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propiedad canónico PidTagStatusString

  
  
**Se aplica a**: Outlook 
  
Contiene un mensaje que indica el estado actual de un recurso de la sesión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificador:  <br/> |0x3E08  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Estas propiedades proporcionan proveedores de servicios y la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicio en particular de MAPI. Esta propiedad se explica y proporciona información adicional acerca de un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Considerando que es necesario para todos los objetos de estado **PR_STATUS_CODE** , **PR_STATUS_STRING** y las propiedades asociadas son opcionales. Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado. 
  
La cadena se genera en el mismo lado de la llamada a procedimiento remoto como la cola MAPI; viajan a través de la memoria compartida en lugar de que se puede ordenar a través de un límite de proceso.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

