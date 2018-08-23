---
title: Propiedad canónica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588576"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propiedad canónica PidTagSpoolerStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el estado del mensaje según la información que está disponible para la cola de MAPI.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificador:  <br/> |0x0E10  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se calcula mediante MAPI en objetos de mensaje.
  
Esta propiedad aparece en los mensajes entrantes sólo y está reservada en todos los demás casos. Indica si un mensaje se ha entregado a su ubicación final o si un proveedor de enlace de mensajería potencialmente elimina el mensaje mientras se reenrutamiento.
  
Aplicaciones de cliente nunca deben establecer esta propiedad. Para un mensaje entrante, un proveedor de servicio o cliente puede llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) en esta propiedad para determinar el estado del mensaje. El valor S_OK indica que el mensaje se entregó correctamente al almacén de mensajes. El valor MAPI_E_OBJECT_DELETED indica que el mensaje se eliminó y nunca se ha confirmado en el almacén. 
  
Los proveedores de almacén de mensajes deben admitir esta propiedad en los mensajes, tablas de destinatarios y la tabla de cola saliente. Los clientes y proveedores deben ser capaces de establecer columnas en la tabla cola saliente y restringir en función de esta propiedad.
  
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

