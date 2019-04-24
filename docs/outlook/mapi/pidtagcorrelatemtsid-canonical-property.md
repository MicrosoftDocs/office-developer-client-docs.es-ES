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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359937"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propiedad canónica PidTagCorrelateMtsid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador del sistema de transferencia de mensajes (MTS) que se usa en la correlación de informes con los mensajes enviados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificador:  <br/> |0x0E0D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando un proveedor de transporte encuentra un mensaje enviado con esta propiedad establecida en TRUE, establece esta propiedad en el identificador de MTS para ese mensaje. Después de la transmisión, esta propiedad se almacena con el mensaje en la carpeta elementos enviados del mensaje interpersonal (IPM).
  
Los sistemas de mensajería que admiten la correlación mediante el identificador de MTS, como X. 400, conservan el identificador como parte del sobre de transporte del mensaje original y también de los informes generados en respuesta al mismo. Cuando un informe se entrega desde un sistema de mensajería de ese tipo, el proveedor de transporte establece esta propiedad en el identificador de MTS original desde el sobre de transporte del informe. A continuación, esta propiedad se almacena con el informe.
  
Una aplicación cliente puede mantener una carpeta de resultados de búsqueda de todos los mensajes que tienen esta propiedad. Cuando se entrega un informe para este tipo de mensajes, el cliente puede aplicar restricciones a la carpeta de resultados de búsqueda, buscar la versión original del mensaje y correlacionar la información del mensaje original con la nueva información.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

