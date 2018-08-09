---
title: Celda IndFirst (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Representa la distancia de separación que existe entre la primera línea de cada párrafo en el bloque de texto y la sangría izquierda del párrafo. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría de la primera línea permanece igual.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822323"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="c2e2e-105">Celda IndFirst (sección Párrafo)</span><span class="sxs-lookup"><span data-stu-id="c2e2e-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="c2e2e-p102">Representa la distancia de separación que existe entre la primera línea de cada párrafo en el bloque de texto y la sangría izquierda del párrafo. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría de la primera línea permanece igual.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2e2e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2e2e-109">Remarks</span></span>

<span data-ttu-id="c2e2e-110">Para obtener una referencia a la celda IndFirst por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2e2e-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c2e2e-112">Para.IndFirst [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c2e2e-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c2e2e-113">Para obtener una referencia desde un programa a la celda IndFirst por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2e2e-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-114">Section index:</span></span>  <br/> |<span data-ttu-id="c2e2e-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c2e2e-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c2e2e-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-116">Row index:</span></span>  <br/> |<span data-ttu-id="c2e2e-117">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c2e2e-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c2e2e-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c2e2e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c2e2e-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="c2e2e-119">**visIndentFirst**</span></span> <br/> |
   

