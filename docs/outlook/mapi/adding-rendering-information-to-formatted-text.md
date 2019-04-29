---
title: Agregar información de representación a texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420615"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Agregar información de representación a texto con formato

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para indicar la ubicación del texto con formato donde se representan los datos adjuntos, debe insertar una secuencia de caracteres de marcador de posición en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje. La secuencia del marcador de posición está formada por los siguientes `\objattph`caracteres:.
  
 **Para agregar información de representación al texto del mensaje con formato**
  
- Al escribir la secuencia de texto en la propiedad **PR_RTF_COMPRESSED** del mensaje, inserte la secuencia del marcador de posición y un carácter de espacio en la posición en la que se deben representar los datos adjuntos. 
    
- Establezca la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico. El valor mínimo debe asignarse a la propiedad **PR_RENDERING_POSITION** del primer dato adjunto para que aparezca en el texto con formato; el valor más alto para los últimos datos adjuntos. 
    

