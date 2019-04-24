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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278761"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propiedad canónica PidTagStatusCode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de máscara de marcas que indican el estado actual de un recurso de sesión. Todos los proveedores de servicios establecen los códigos de estado como hace MAPI para informar sobre el estado del subsistema, la cola MAPI y la libreta de direcciones integrada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_CODE  <br/> |
|Identificador:  <br/> |0x3E04  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El código de Estado debe aparecer en el archivo MAPISVC. inf para todos los proveedores. 
  
Los objetos de estado son implementados por MAPI y por todos los proveedores de servicios. Hay dos conjuntos de valores válidos para los códigos de estado: un conjunto para todos los objetos status y otro conjunto solo para los proveedores de transporte. Todos los objetos status pueden establecer esta propiedad en los siguientes valores:
  
STATUS_AVAILABLE 
  
> Indica que el recurso está operativo.
    
STATUS_FAILURE 
  
> Indica que el recurso está experimentando un problema. Para los proveedores de servicios, STATUS_FAILURE indica que el proveedor puede cerrarse pronto para finalizar la sesión actual.
    
STATUS_OFFLINE 
  
> Indica que solo están disponibles los datos locales o los servicios.
    
Los proveedores de transporte también pueden establecer sus propiedades **PR_STATUS_CODE** de objetos de estado en los siguientes valores: 
  
STATUS_INBOUND_ACTIVE 
  
> Indica que el proveedor de transporte está recibiendo un mensaje entrante. 
    
STATUS_INBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede recibir mensajes entrantes.
    
STATUS_INBOUND_FLUSH 
  
> Indica que el proveedor de transporte está descargando mensajes de la cola de entrada.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indica que el proveedor de transporte está recibiendo un mensaje saliente. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede controlar los mensajes salientes.
    
STATUS_OUTBOUND_FLUSH 
  
> Indica que el proveedor de transporte está cargando mensajes desde su cola de salida.
    
STATUS_REMOTE_ACCESS 
  
> Indica que el proveedor de transporte admite el acceso remoto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

