---
title: Agregar información de representación de texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816396"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Agregar información de representación de texto con formato

  
  
**Hace referencia a**: Outlook 
  
Para indicar la ubicación en el texto con formato donde se representa un archivo adjunto, se debe insertar una secuencia de caracteres de marcador de posición en la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La secuencia de marcador de posición se compone de los siguientes caracteres: `\objattph`.
  
 **Para agregar información de representación para el texto del mensaje con formato**
  
- Al escribir la secuencia de texto en la propiedad del mensaje **PR_RTF_COMPRESSED** , inserte la secuencia de marcador de posición y un carácter de espacio en la posición donde se deben representar los datos adjuntos. 
    
- Establezca la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico. El valor más bajo debe asignarse a la propiedad **PR_RENDERING_POSITION** de los primeros datos adjuntos que aparezca en el texto con formato; el valor más alto para el último archivo adjunto. 
    

