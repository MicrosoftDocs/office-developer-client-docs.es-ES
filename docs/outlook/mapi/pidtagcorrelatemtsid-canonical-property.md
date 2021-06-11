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
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426838"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propiedad canónica PidTagCorrelateMtsid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador del sistema de transferencia de mensajes (MTS) usado para correlacionar informes con mensajes enviados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificador:  <br/> |0x0E0D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando un proveedor de transporte encuentra un mensaje enviado con esta propiedad establecida en TRUE, establece esta propiedad en el identificador MTS de ese mensaje. Después de la transmisión, esta propiedad se almacena con el mensaje en la carpeta Elementos enviados del mensaje interpersonal (IPM).
  
Los sistemas de mensajería que admiten la correlación por el identificador MTS, como X.400, conservan el identificador como parte del sobre de transporte del mensaje original y también de los informes generados en respuesta a él. Cuando un informe se entrega desde un sistema de mensajería de este tipo, el proveedor de transporte establece esta propiedad en el identificador MTS original del sobre de transporte del informe. A continuación, esta propiedad se almacena con el informe.
  
Una aplicación cliente puede mantener una carpeta de resultados de búsqueda de todos los mensajes que tienen esta propiedad. Cuando un informe llega para un mensaje de este tipo, el cliente puede aplicar restricciones a la carpeta de resultados de búsqueda, buscar la versión original del mensaje y correlacionar la información del mensaje original con la nueva información.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

