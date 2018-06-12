---
title: Propiedad canónico PidTagStatusCode
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820338"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propiedad canónico PidTagStatusCode

  
  
**Se aplica a**: Outlook 
  
Contiene una máscara de bits de marcadores que indican el estado actual de un recurso de la sesión. Todos los proveedores de servicios establecen códigos de estado de MAPI para informar sobre el estado de la libreta de direcciones integrada, la cola MAPI y el subsistema de igual.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS_CODE  <br/> |
|Identificador:  <br/> |0x3E04  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Notas

El código de estado debe aparecer en el archivo Mapisvc.inf para todos los proveedores. 
  
Objetos de estado se implementan por MAPI y por todos los proveedores de servicio. Hay dos conjuntos de valores válidos para los códigos de estado, un conjunto de todos los objetos de estado y otra para sólo los proveedores de transporte. Todos los objetos de estado pueden establecer esta propiedad en los siguientes valores:
  
STATUS_AVAILABLE 
  
> Indica que el recurso está operativo.
    
STATUS_FAILURE 
  
> Indica que el recurso está experimentando un problema. Para proveedores de servicios, STATUS_FAILURE indica que el proveedor es posible que pronto se apague para finalizar la sesión actual.
    
STATUS_OFFLINE 
  
> Indica que los datos locales sólo o servicios están disponibles.
    
Los proveedores de transporte también pueden establecer su estado de las propiedades de los objetos **PR_STATUS_CODE** a los siguientes valores: 
  
STATUS_INBOUND_ACTIVE 
  
> Indica que el proveedor de transporte recibe un mensaje entrante. 
    
STATUS_INBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede recibir los mensajes entrantes.
    
STATUS_INBOUND_FLUSH 
  
> Indica que el proveedor de transporte está descargando los mensajes de la cola de entrada.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indica que el proveedor de transporte recibe un mensaje de salida. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indica que el proveedor de transporte puede controlar los mensajes salientes.
    
STATUS_OUTBOUND_FLUSH 
  
> Indica que el proveedor de transporte carga de los mensajes de su cola de salida.
    
STATUS_REMOTE_ACCESS 
  
> Indica que el proveedor de transporte admite el acceso remoto.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

