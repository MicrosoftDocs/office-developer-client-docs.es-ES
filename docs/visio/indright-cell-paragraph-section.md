---
title: Celda IndRight (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822334"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="964f1-105">Celda IndRight (sección Párrafo)</span><span class="sxs-lookup"><span data-stu-id="964f1-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="964f1-p102">Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.</span><span class="sxs-lookup"><span data-stu-id="964f1-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="964f1-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="964f1-109">Remarks</span></span>

<span data-ttu-id="964f1-110">Para obtener una referencia a la celda IndRight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="964f1-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="964f1-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="964f1-111">Cell name:</span></span>  <br/> | <span data-ttu-id="964f1-112">Para.IndRight [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="964f1-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="964f1-113">Para obtener una referencia desde un programa a la celda IndRight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="964f1-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="964f1-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="964f1-114">Section index:</span></span>  <br/> |<span data-ttu-id="964f1-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="964f1-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="964f1-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="964f1-116">Row index:</span></span>  <br/> |<span data-ttu-id="964f1-117">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="964f1-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="964f1-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="964f1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="964f1-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="964f1-119">**visIndentRight**</span></span> <br/> |
   

