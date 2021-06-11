---
title: Escritura de texto con formato sin comprimir
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426327"
---
# <a name="writing-uncompressed-formatted-text"></a>Escritura de texto con formato sin comprimir

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al prepararse para enviar un mensaje con texto con formato, establezca la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje en texto comprimido o sin comprimir. Escribir texto comprimido en la **propiedad PR_RTF_COMPRESSED** es una operación muy intensiva en la CPU y puede afectar considerablemente al rendimiento. 
  
Para mejorar el rendimiento del envío de mensajes con formato, haga lo siguiente:
  
- Actualice la CPU, una solución que no siempre es plausible.
    
    - O -
    
- Escriba texto sin comprimir en la **PR_RTF_COMPRESSED** propiedad. 
    
El procedimiento para establecer **PR_RTF_COMPRESSED** texto sin comprimir es el mismo que para establecerlo con texto comprimido, con una excepción. Al llamar [a WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca la marca STORE_UNCOMPRESSED_RTF en el _parámetro ulFlags._ Establecer texto sin comprimir tiene la desventaja de que aumenta el tamaño de los mensajes. 
  

