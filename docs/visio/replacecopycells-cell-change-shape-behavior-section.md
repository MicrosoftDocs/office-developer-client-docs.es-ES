---
title: Celda ReplaceCopyCells (sección de comportamiento de cambio forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica una lista de las celdas de ShapeSheet que se copian desde una forma antigua a la forma de reemplazo durante una operación de reemplazo de la forma.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822943"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="97a7a-103">Celda ReplaceCopyCells (sección de comportamiento de cambio forma)</span><span class="sxs-lookup"><span data-stu-id="97a7a-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="97a7a-104">Indica una lista de las celdas de ShapeSheet que se copian desde una forma antigua a la forma de reemplazo durante una operación de reemplazo de la forma.</span><span class="sxs-lookup"><span data-stu-id="97a7a-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97a7a-105">Notas</span><span class="sxs-lookup"><span data-stu-id="97a7a-105">Remarks</span></span>

<span data-ttu-id="97a7a-106">La forma de patrón de la sustitución debe contener una llamada de función **DEPENDSON** en la celda **ReplaceCopyCells** , donde cada argumento de la función es una referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="97a7a-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="97a7a-107">Esas celdas se copian de la antigua forma a la forma que dan como resultado de una operación de reemplazo de la forma, independientemente de dónde se encuentran en la ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="97a7a-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="97a7a-108">Los valores y las fórmulas que hacen referencia otras celdas se copian a la forma resultante.</span><span class="sxs-lookup"><span data-stu-id="97a7a-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="97a7a-109">Si la forma resultante no tiene la celda que se hace referencia, la celda copiada contiene sólo el valor.</span><span class="sxs-lookup"><span data-stu-id="97a7a-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="97a7a-110">Referencias de la celda **ReplaceCopyCells** reemplazar el conjunto de protección en las celdas como se define en la sección de **protección** y la **ReplaceLockFormat**, **ReplaceLockShapeData**y **ReplaceLockText** celdas.</span><span class="sxs-lookup"><span data-stu-id="97a7a-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="97a7a-111">Para obtener una referencia a la celda **ReplaceCopyCells** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="97a7a-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97a7a-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="97a7a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="97a7a-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="97a7a-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="97a7a-114">Para obtener una referencia a la celda **ReplaceCopyCells** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="97a7a-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97a7a-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="97a7a-115">Section index:</span></span>  <br/> |<span data-ttu-id="97a7a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97a7a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97a7a-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="97a7a-117">Row index:</span></span>  <br/> |<span data-ttu-id="97a7a-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="97a7a-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="97a7a-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="97a7a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="97a7a-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="97a7a-120">**visReplaceCopyCells**</span></span> <br/> |
   

