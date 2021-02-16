---
title: Celda ReplaceCopyCells (Sección de comportamiento de cambio de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica una lista de celdas de ShapeSheet que se copian de una forma antigua a la forma de reemplazo durante una operación de reemplazo de forma.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409345"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="889b4-103">Celda ReplaceCopyCells (Sección de comportamiento de cambio de forma)</span><span class="sxs-lookup"><span data-stu-id="889b4-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="889b4-104">Indica una lista de celdas de ShapeSheet que se copian de una forma antigua a la forma de reemplazo durante una operación de reemplazo de forma.</span><span class="sxs-lookup"><span data-stu-id="889b4-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="889b4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="889b4-105">Remarks</span></span>

<span data-ttu-id="889b4-106">La forma maestra del reemplazo debe contener una llamada de función **DEPENDSON** en la celda **ReplaceCopyCells,** donde cada argumento de la función es una referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="889b4-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="889b4-107">Dichas celdas se copian de la forma antigua a la forma resultante de una operación de reemplazo de forma, independientemente de dónde se encuentran en shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="889b4-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="889b4-108">Los valores o fórmulas que hacen referencia a otras celdas se copian en la forma resultante.</span><span class="sxs-lookup"><span data-stu-id="889b4-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="889b4-109">Si la forma resultante no tiene la celda a la que se hace referencia, la celda copiada sólo contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="889b4-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="889b4-110">Las referencias de la celda **ReplaceCopyCells** invalidan  la protección establecida en las celdas según se define en la sección Protección y las celdas **ReplaceLockFormat**, **ReplaceLockShapeData** y **ReplaceLockText.**</span><span class="sxs-lookup"><span data-stu-id="889b4-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="889b4-111">Para obtener una referencia a la celda **ReplaceCopyCells** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="889b4-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="889b4-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="889b4-112">Cell name:</span></span>  <br/> | <span data-ttu-id="889b4-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="889b4-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="889b4-114">Para obtener una referencia desde un programa a la celda **ReplaceCopyCells** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="889b4-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="889b4-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="889b4-115">Section index:</span></span>  <br/> |<span data-ttu-id="889b4-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="889b4-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="889b4-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="889b4-117">Row index:</span></span>  <br/> |<span data-ttu-id="889b4-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="889b4-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="889b4-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="889b4-119">Cell index:</span></span>  <br/> |<span data-ttu-id="889b4-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="889b4-120">**visReplaceCopyCells**</span></span> <br/> |
   

