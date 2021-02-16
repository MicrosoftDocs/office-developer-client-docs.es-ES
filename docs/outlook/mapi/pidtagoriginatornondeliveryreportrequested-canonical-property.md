---
title: Propiedad canónica PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341961"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a>Propiedad canónica PidTagOriginatorNonDeliveryReportRequested

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un remitente de mensaje solicita un informe de no entrega para un destinatario determinado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificador:  <br/> |0x0C08  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para dirigir al sistema de mensajería en el control de mensajes no entregados. En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) establecida en FALSE.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

