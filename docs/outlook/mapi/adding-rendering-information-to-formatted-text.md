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
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="c8288-103">Agregar información de representación de texto con formato</span><span class="sxs-lookup"><span data-stu-id="c8288-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="c8288-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8288-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8288-105">Para indicar la ubicación en el texto con formato donde se representa un archivo adjunto, se debe insertar una secuencia de caracteres de marcador de posición en la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8288-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="c8288-106">La secuencia de marcador de posición se compone de los siguientes caracteres: `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="c8288-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="c8288-107">**Para agregar información de representación para el texto del mensaje con formato**</span><span class="sxs-lookup"><span data-stu-id="c8288-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="c8288-108">Al escribir la secuencia de texto en la propiedad del mensaje **PR_RTF_COMPRESSED** , inserte la secuencia de marcador de posición y un carácter de espacio en la posición donde se deben representar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c8288-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="c8288-109">Establezca la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c8288-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="c8288-110">El valor más bajo debe asignarse a la propiedad **PR_RENDERING_POSITION** de los primeros datos adjuntos que aparezca en el texto con formato; el valor más alto para el último archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="c8288-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

