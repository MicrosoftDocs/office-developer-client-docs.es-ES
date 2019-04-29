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
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439425"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Propiedad canónica PidTagDeliveryPoint

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la naturaleza de la entidad funcional a través de la cual un mensaje se ha entregado o se habría entregado al destinatario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DELIVERY_POINT  <br/> |
|Identificador:  <br/> |0x0C07  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores: 
  
MAPI_MH_DP_ML 
  
> Entregada a una lista de distribución, un punto de entrega que, a su vez, puede distribuir el mensaje a muchos destinatarios.
    
MAPI_MH_DP_MS 
  
> Se entrega a un almacén de mensajes en lugar de a un destinatario directamente.
    
MAPI_MH_DP_OTHER_AU 
  
> Entregarse a una unidad de acceso (AU) que no sea una unidad de acceso de entrega física (PDAU), como un sistema de FAX.
    
MAPI_MH_DP_PDAU 
  
> Entregarse a una unidad de acceso de entrega física, como una compañía de correos humanos.
    
MAPI_MH_DP_PDS_PATRON 
  
> Entregarse a un sistema de entrega físico, como un buzón postal convencional.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Se entrega a un agente de usuario privado (UA), como un cliente en un sistema de mensajería interno.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Entrega a un agente de usuario público o a un proveedor de servicios públicos.
    
El valor predeterminado es MAPI_MH_DP_PRIVATE_UA, es decir, un cliente MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

