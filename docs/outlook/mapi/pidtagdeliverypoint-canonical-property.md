---
title: Propiedad canónica PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819441"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Propiedad canónica PidTagDeliveryPoint

  
  
**Hace referencia a**: Outlook 
  
Especifica la naturaleza de la entidad funcional por medio de que un mensaje se ha o habría se ha entregado al destinatario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DELIVERY_POINT  <br/> |
|Identificador:  <br/> |0x0C07  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores: 
  
MAPI_MH_DP_ML 
  
> Entrega a una lista de distribución, una entrega punto que a su vez puede distribuir el mensaje a muchos destinatarios.
    
MAPI_MH_DP_MS 
  
> Entrega a un almacén de mensajes en lugar de hacerlo directamente a un destinatario.
    
MAPI_MH_DP_OTHER_AU 
  
> Entrega a una unidad de acceso (AU) que no sea una unidad de acceso de entrega física (PDAU), como un sistema de FAX.
    
MAPI_MH_DP_PDAU 
  
> Entrega a una unidad de acceso de entrega física, como un operador postal humana.
    
MAPI_MH_DP_PDS_PATRON 
  
> Entrega a un usuario del sistema físico de entrega, como un buzón de correo postal convencional.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Entrega a un agente de usuario privada (UA), como un cliente en un sistema de mensajería interno.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Entregar a un agente de usuario público o proveedor de servicios públicos.
    
El valor predeterminado es MAPI_MH_DP_PRIVATE_UA, es decir, un cliente MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

