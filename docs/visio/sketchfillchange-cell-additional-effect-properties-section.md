---
title: Celda SketchFillChange (Sección de propiedades de efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina la cantidad de aleatorización del relleno de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchFillChange se establece en 0%, la geometría de límite del relleno de una forma coincide con la geometría de la forma. Si el valor es 100%, la geometría delimitadora del relleno de la forma no sigue la geometría de la forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408078"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="15e7c-105">Celda SketchFillChange (Sección de propiedades de efecto adicional)</span><span class="sxs-lookup"><span data-stu-id="15e7c-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="15e7c-106">Determina la cantidad de aleatorización del relleno de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección.</span><span class="sxs-lookup"><span data-stu-id="15e7c-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="15e7c-107">Si el valor de la celda **SketchFillChange** se establece en 0%, la geometría de límite del relleno de una forma coincide con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="15e7c-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="15e7c-108">Si el valor es 100%, la geometría delimitadora del relleno de la forma no sigue la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="15e7c-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="15e7c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15e7c-109">Remarks</span></span>

<span data-ttu-id="15e7c-110">Para obtener mejores resultados, el rango ideal de valores para la celda **SketchFillChange** está entre el 15 % y el 50 %.</span><span class="sxs-lookup"><span data-stu-id="15e7c-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="15e7c-111">Un valor inferior al 15 % es apenas perceptible; un valor mayor que el 50 % se aleatoriza cada vez más.</span><span class="sxs-lookup"><span data-stu-id="15e7c-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="15e7c-112">Para obtener una referencia a la celda **SketchFillChange** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="15e7c-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15e7c-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="15e7c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="15e7c-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="15e7c-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="15e7c-115">Para obtener una referencia desde un programa a la celda **SketchFillChange** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="15e7c-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15e7c-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="15e7c-116">Section index:</span></span>  <br/> |<span data-ttu-id="15e7c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15e7c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="15e7c-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="15e7c-118">Row index:</span></span>  <br/> |<span data-ttu-id="15e7c-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="15e7c-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="15e7c-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="15e7c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="15e7c-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="15e7c-121">**visSketchFillChange**</span></span> <br/> |
   

