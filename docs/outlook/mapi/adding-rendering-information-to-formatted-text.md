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
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594561"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Agregar información de representación de texto con formato

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para indicar la ubicación en el texto con formato donde se representa un archivo adjunto, se debe insertar una secuencia de caracteres de marcador de posición en la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La secuencia de marcador de posición se compone de los siguientes caracteres: `\objattph`.
  
 **Para agregar información de representación para el texto del mensaje con formato**
  
- Al escribir la secuencia de texto en la propiedad del mensaje **PR_RTF_COMPRESSED** , inserte la secuencia de marcador de posición y un carácter de espacio en la posición donde se deben representar los datos adjuntos. 
    
- Establezca la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico. El valor más bajo debe asignarse a la propiedad **PR_RENDERING_POSITION** de los primeros datos adjuntos que aparezca en el texto con formato; el valor más alto para el último archivo adjunto. 
    

