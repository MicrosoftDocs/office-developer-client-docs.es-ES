---
title: Escribir texto con formato sin comprimir
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577047"
---
# <a name="writing-uncompressed-formatted-text"></a>Escribir texto con formato sin comprimir

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se prepare para enviar un mensaje con texto con formato, establezca la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) al texto comprimido o sin comprimir. Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación de un uso intensivo de CPU muy y considerablemente puede afectar al rendimiento. 
  
Para mejorar el rendimiento de envío de mensajes con formato, ya sea:
  
- Actualización de la CPU, una solución que no siempre pueda suceder.
    
    - O bien -
    
- Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED** . 
    
El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que si se establece con texto comprimido, con una excepción. Cuando se llama a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca el indicador STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags indicado_ . Establecer el texto sin comprimir tiene la desventaja en que aumenta el tamaño de los mensajes. 
  

