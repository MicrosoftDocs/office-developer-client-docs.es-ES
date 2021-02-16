---
title: Propiedad canónica PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405222"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propiedad canónica PidTagCorrelate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el remitente de un mensaje solicita la característica de correlación del sistema de mensajería.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CORRELATE  <br/> |
|Identificador:  <br/> |0x0E0C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para solicitar la correlación de los informes entrantes con el mensaje original enviado. Cuando un proveedor de transporte encuentra un mensaje enviado con **PR_CORRELATE** establecido en TRUE, establece la propiedad **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) en el identificador del sistema de transferencia de mensajes (MTS) para ese mensaje.
  
 **PR_CORRELATE** debe usarse con sistemas de mensajería compatibles con la correlación del identificador MTS, como X.400. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

