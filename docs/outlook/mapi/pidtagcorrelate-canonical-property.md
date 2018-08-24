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
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575458"
---
# <a name="pidtagcorrelate-canonical-property"></a>Propiedad canónica PidTagCorrelate

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el remitente de un mensaje solicita la característica de correlación del sistema de mensajería.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CORRELATE  <br/> |
|Identificador:  <br/> |0x0E0C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para solicitar la correlación de informes entrantes con el mensaje original enviado. Cuando un proveedor de transporte encuentra un mensaje enviado con **PR_CORRELATE** establecido en TRUE, se establece la propiedad **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) para el identificador de sistema (MTS) de transferencia de mensaje para ese mensaje.
  
 **PR_CORRELATE** debe utilizarse con sistemas de mensajería que admiten correlación por identificador de MTS, como X.400. 
  
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

