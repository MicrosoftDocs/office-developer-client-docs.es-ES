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
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325756"
---
# <a name="writing-uncompressed-formatted-text"></a>Escribir texto con formato sin comprimir

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se prepara para enviar un mensaje con texto con formato, establezca la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje en texto comprimido o descomprimido. Escribir texto comprimido en la propiedad **PR_RTF_COMPRESSED** es una operación que conSUME mucha CPU y puede afectar considerablemente al rendimiento. 
  
Para mejorar el rendimiento del envío de mensajes con formato, puede hacer lo siguiente:
  
- Actualizar la CPU, una solución que no siempre es plausible.
    
    - O
    
- Escribir texto sin comprimir en la propiedad **PR_RTF_COMPRESSED** 
    
El procedimiento para establecer **PR_RTF_COMPRESSED** con texto sin comprimir es el mismo que para configurarlo con texto comprimido, con una excepción. Al llamar a [WrapCompressedRTFStream](wrapcompressedrtfstream.md), establezca la marca STORE_UNCOMPRESSED_RTF en el parámetro _ulFlags_ . La configuración del texto sin comprimir tiene el inconveniente de que aumenta el tamaño de los mensajes. 
  

