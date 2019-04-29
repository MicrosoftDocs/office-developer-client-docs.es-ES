---
title: Celda SpBefore (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425760"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="ad7e2-103">Celda SpBefore (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="ad7e2-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="ad7e2-104">Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.</span><span class="sxs-lookup"><span data-stu-id="ad7e2-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad7e2-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad7e2-105">Remarks</span></span>

<span data-ttu-id="ad7e2-p101">Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio delante del párrafo permanece igual.</span><span class="sxs-lookup"><span data-stu-id="ad7e2-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="ad7e2-108">Para obtener una referencia a la celda SpBefore por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad7e2-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ad7e2-110">Para. SpBefore [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ad7e2-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ad7e2-111">Para obtener una referencia desde un programa a la celda SpBefore por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad7e2-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-112">Section index:</span></span>  <br/> |<span data-ttu-id="ad7e2-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ad7e2-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="ad7e2-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-114">Row index:</span></span>  <br/> |<span data-ttu-id="ad7e2-115">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ad7e2-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ad7e2-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ad7e2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ad7e2-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="ad7e2-117">**visSpaceBefore**</span></span> <br/> |
   

