---
title: Escribir sin comprimir texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821000"
---
# <a name="writing-uncompressed-formatted-text"></a>Escribir sin comprimir texto con formato

  
  
**Se aplica a**: Outlook 
  
Cuando se prepare para enviar un mensaje con texto con formato, establezca la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) al texto comprimido o sin comprimir. Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación de un uso intensivo de CPU muy y considerablemente puede afectar al rendimiento. 
  
Para mejorar el rendimiento de envío de mensajes con formato, ya sea:
  
- Actualización de la CPU, una solución que no siempre pueda suceder.
    
    - O bien -
    
- Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED** . 
    
El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que si se establece con texto comprimido, con una excepción. Cuando se llama a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca el indicador STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags indicado_ . Establecer el texto sin comprimir tiene la desventaja en que aumenta el tamaño de los mensajes. 
  

