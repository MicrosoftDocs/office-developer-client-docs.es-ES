---
title: Propiedad canónica PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819407"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propiedad canónica PidTagCorrelateMtsid

  
  
**Hace referencia a**: Outlook 
  
Contiene el identificador del sistema (MTS) de transferencia de mensaje usado en la correlación de informes con los mensajes enviados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificador:  <br/> |0x0E0D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando un proveedor de transporte encuentra un mensaje enviado con esta propiedad establecida en TRUE, se establece esta propiedad para el identificador MTS para ese mensaje. Después de transmisión, esta propiedad se almacena con el mensaje en la carpeta Elementos enviados de mensajes interpersonales (IPM).
  
Los sistemas de mensajería que admiten la correlación por identificador de MTS, como X.400, conservan el identificador como parte de los sobres de transporte del mensaje original y también de los informes generados en respuesta a ella. Cuando un informe se entrega desde como un sistema de mensajería, el proveedor de transporte establece esta propiedad en el identificador MTS original desde sobre de transporte del informe. Esta propiedad se almacena con el informe.
  
Una aplicación cliente puede mantener una carpeta de resultados de búsqueda de todos los mensajes de esta propiedad. Cuando se recibe un informe para este tipo de mensaje, el cliente puede aplicar restricciones a la carpeta de resultados de búsqueda, buscar la versión original del mensaje y correlacionar la información del mensaje original con la nueva información.
  
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

