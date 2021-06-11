---
title: Adición de información de representación al texto con formato
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
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="31a66-103">Adición de información de representación al texto con formato</span><span class="sxs-lookup"><span data-stu-id="31a66-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="31a66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31a66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31a66-105">Para indicar la ubicación en el texto con formato donde se representa un dato adjunto, debe insertar una secuencia de caracteres de marcador de posición en la propiedad PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="31a66-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="31a66-106">La secuencia de marcador de posición está hecha de los siguientes caracteres:  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="31a66-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="31a66-107">**Para agregar información de representación al texto de mensaje con formato**</span><span class="sxs-lookup"><span data-stu-id="31a66-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="31a66-108">Al escribir la secuencia de texto  en la propiedad PR_RTF_COMPRESSED del mensaje, inserte la secuencia de marcador de posición y un carácter de espacio en la posición donde se deben representar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="31a66-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="31a66-109">Establezca la **propiedad PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada dato adjunto en un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="31a66-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="31a66-110">El valor más bajo debe asignarse a la **PR_RENDERING_POSITION** de los primeros datos adjuntos que aparecen en el texto con formato; el valor más alto de los últimos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="31a66-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

