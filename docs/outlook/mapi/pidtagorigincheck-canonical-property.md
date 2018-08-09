---
title: Propiedad canónica PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819876"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propiedad canónica PidTagOriginCheck

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor binario de comprobación que permite a un destinatario de informe de entrega comprobar el origen del mensaje original.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificador:  <br/> |0x0027  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona un medio para un tercero, como un agente de transferencia de mensajes (MTA) o un usuario de mensajería recibir un informe de entrega, para comprobar el origen del mensaje enviado. Si está presente en un mensaje recibido, esta propiedad debe copiarse en cualquier informe de entrega generado en respuesta al mensaje.
  
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

