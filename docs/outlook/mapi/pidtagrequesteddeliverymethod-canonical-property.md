---
title: Propiedad canónica PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820114"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Propiedad canónica PidTagRequestedDeliveryMethod

  
  
**Hace referencia a**: Outlook 
  
Esta propiedad contiene una matriz binaria de métodos de entrega (proveedores de servicios), en orden de preferencia del remitente de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Identificador:  <br/> |0x0C18  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

La matriz contenida en esta propiedad consta de ASN.1 identificadores para cada uno de los proveedores de servicios.
  
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

