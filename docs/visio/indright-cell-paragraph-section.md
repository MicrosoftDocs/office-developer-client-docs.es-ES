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
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408869"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="dbadc-105">Celda IndRight (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="dbadc-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="dbadc-p102">Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.</span><span class="sxs-lookup"><span data-stu-id="dbadc-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbadc-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbadc-109">Remarks</span></span>

<span data-ttu-id="dbadc-110">Para obtener una referencia a la celda IndRight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="dbadc-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbadc-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dbadc-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dbadc-112">Para.IndRight[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dbadc-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dbadc-113">Para obtener una referencia desde un programa a la celda IndRight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dbadc-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbadc-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dbadc-114">Section index:</span></span>  <br/> |<span data-ttu-id="dbadc-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="dbadc-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="dbadc-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dbadc-116">Row index:</span></span>  <br/> |<span data-ttu-id="dbadc-117">**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dbadc-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dbadc-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dbadc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dbadc-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="dbadc-119">**visIndentRight**</span></span> <br/> |
   

