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
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405166"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="1c12f-105">Celda IndLeft (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="1c12f-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="1c12f-p102">Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.</span><span class="sxs-lookup"><span data-stu-id="1c12f-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c12f-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c12f-109">Remarks</span></span>

<span data-ttu-id="1c12f-110">Para obtener una referencia a la celda IndLeft por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1c12f-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c12f-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1c12f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1c12f-112">Para.IndLeft[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1c12f-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1c12f-113">Para obtener una referencia desde un programa a la celda IndLeft por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1c12f-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c12f-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1c12f-114">Section index:</span></span>  <br/> |<span data-ttu-id="1c12f-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="1c12f-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="1c12f-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1c12f-116">Row index:</span></span>  <br/> |<span data-ttu-id="1c12f-117">**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1c12f-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1c12f-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1c12f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1c12f-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="1c12f-119">**visIndentLeft**</span></span> <br/> |
   

