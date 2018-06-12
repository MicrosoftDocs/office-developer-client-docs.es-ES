---
title: Celda IndLeft (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822332"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="bcff1-105">Celda IndLeft (sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="bcff1-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="bcff1-p102">Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.</span><span class="sxs-lookup"><span data-stu-id="bcff1-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bcff1-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcff1-109">Remarks</span></span>

<span data-ttu-id="bcff1-110">Para obtener una referencia a la celda IndLeft por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="bcff1-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcff1-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bcff1-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bcff1-112">Para.IndLeft [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bcff1-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bcff1-113">Para obtener una referencia a la celda IndLeft por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bcff1-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcff1-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bcff1-114">Section index:</span></span>  <br/> |<span data-ttu-id="bcff1-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="bcff1-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="bcff1-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bcff1-116">Row index:</span></span>  <br/> |<span data-ttu-id="bcff1-117">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bcff1-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bcff1-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bcff1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bcff1-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="bcff1-119">**visIndentLeft**</span></span> <br/> |
   

