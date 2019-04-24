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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278896"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propiedad canónica PidTagStatusString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mensaje que indica el estado actual de un recurso de sesión. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificador:  <br/> |0x3E08  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades proporcionan a los proveedores de servicios y a MAPI la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicios determinado. Esta propiedad explica y proporciona información adicional sobre un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Mientras que **PR_STATUS_CODE** es necesario para todos los objetos status, **PR_STATUS_STRING** y las propiedades asociadas son opcionales. Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado. 
  
La cadena se genera en el mismo lado de la llamada a procedimiento remoto que la cola MAPI; viaja a través de la memoria compartida en lugar de calcular las referencias a lo largo de un límite de proceso.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

