---
title: Propiedad canónica PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418517"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propiedad canónica PidTagStatusCode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que indican el estado actual de un recurso de sesión. Todos los proveedores de servicios establecen códigos de estado al igual que MAPI para informar sobre el estado del subsistema, la cola MAPI y la libreta de direcciones integrada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_CODE  <br/> |
|Identificador:  <br/> |0x3E04  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El código de estado debe aparecer en el archivo Mapisvc.inf para todos los proveedores. 
  
Mapi y todos los proveedores de servicios implementan objetos de estado. Hay dos conjuntos de valores válidos para códigos de estado, uno establecido para todos los objetos de estado y otro conjunto solo para proveedores de transporte. Todos los objetos de estado pueden establecer esta propiedad en los siguientes valores:
  
STATUS_AVAILABLE 
  
> Indica que el recurso está operativo.
    
STATUS_FAILURE 
  
> Indica que el recurso está experimentando un problema. Para los proveedores de servicios, STATUS_FAILURE indica que el proveedor podría cerrarse pronto para finalizar la sesión actual.
    
STATUS_OFFLINE 
  
> Indica que solo están disponibles los datos o servicios locales.
    
Los proveedores de transporte también pueden establecer las propiedades **de** PR_STATUS_CODE de sus objetos de estado en los siguientes valores: 
  
STATUS_INBOUND_ACTIVE 
  
> Indica que el proveedor de transporte recibe un mensaje entrante. 
    
STATUS_INBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede recibir mensajes entrantes.
    
STATUS_INBOUND_FLUSH 
  
> Indica que el proveedor de transporte está descargando mensajes de la cola entrante.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indica que el proveedor de transporte recibe un mensaje saliente. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede controlar los mensajes salientes.
    
STATUS_OUTBOUND_FLUSH 
  
> Indica que el proveedor de transporte está cargando mensajes desde su cola de salida.
    
STATUS_REMOTE_ACCESS 
  
> Indica que el proveedor de transporte admite el acceso remoto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

