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
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421567"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propiedad canónica PidTagStatusString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mensaje que indica el estado actual de un recurso de sesión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificador:  <br/> |0x3E08  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades ofrecen a los proveedores de servicios y MAPI la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicios en particular. Esta propiedad explica y proporciona información adicional sobre un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Mientras que **PR_STATUS_CODE** es necesario para todos los objetos de **estado,** PR_STATUS_STRING y las propiedades asociadas son opcionales. Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado. 
  
La cadena se genera en el mismo lado de la llamada de procedimiento remoto que la cola MAPI; viaja a través de la memoria compartida en lugar de ser serializada a través de un límite de proceso.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

