---
title: Propiedad canónica PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819880"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Propiedad canónica PidTagOriginatorDeliveryReportRequested

  
  
**Hace referencia a**: Outlook 
  
Contiene TRUE si el remitente del mensaje solicita un informe de entrega para un destinatario concreto desde el sistema de mensajería antes de que el mensaje se coloca en el almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificador:  <br/> |0x0023  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se utiliza para dirigir el sistema de mensajería en el control de los mensajes entregados. En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) que se establece en FALSE.
  
Establecimiento de la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** en un mensaje es una forma para solicitar informes de estado de entrega para todos los destinatarios. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

