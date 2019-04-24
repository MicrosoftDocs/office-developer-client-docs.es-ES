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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331125"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="a6797-103">Agregar información de representación a texto con formato</span><span class="sxs-lookup"><span data-stu-id="a6797-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="a6797-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6797-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6797-105">Para indicar la ubicación del texto con formato donde se representan los datos adjuntos, debe insertar una secuencia de caracteres de marcador de posición en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6797-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="a6797-106">La secuencia del marcador de posición está formada por los siguientes `\objattph`caracteres:.</span><span class="sxs-lookup"><span data-stu-id="a6797-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="a6797-107">**Para agregar información de representación al texto del mensaje con formato**</span><span class="sxs-lookup"><span data-stu-id="a6797-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="a6797-108">Al escribir la secuencia de texto en la propiedad **PR_RTF_COMPRESSED** del mensaje, inserte la secuencia del marcador de posición y un carácter de espacio en la posición en la que se deben representar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a6797-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="a6797-109">Establezca la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="a6797-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="a6797-110">El valor mínimo debe asignarse a la propiedad **PR_RENDERING_POSITION** del primer dato adjunto para que aparezca en el texto con formato; el valor más alto para los últimos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a6797-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

