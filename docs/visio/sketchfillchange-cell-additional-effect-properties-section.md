---
title: Celda SketchFillChange (sección de propiedades de efecto adicionales)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina la cantidad de selección aleatoria de relleno de la forma de la geometría de forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchFillChange se establece en 0%, la geometría del límite de relleno de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría del límite del relleno de la forma no siguen la geometría de la forma.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823264"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="20ff8-105">Celda SketchFillChange (sección de propiedades de efecto adicionales)</span><span class="sxs-lookup"><span data-stu-id="20ff8-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="20ff8-106">Determina la cantidad de selección aleatoria de relleno de la forma de la geometría de forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección.</span><span class="sxs-lookup"><span data-stu-id="20ff8-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="20ff8-107">Si el valor de la celda **SketchFillChange** se establece en 0%, la geometría del límite de relleno de la forma coincide con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="20ff8-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="20ff8-108">Si el valor es 100%, la geometría del límite del relleno de la forma no siguen la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="20ff8-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20ff8-109">Notas</span><span class="sxs-lookup"><span data-stu-id="20ff8-109">Remarks</span></span>

<span data-ttu-id="20ff8-110">Para obtener mejores resultados, el intervalo de valores de la celda **SketchFillChange** ideal está entre el 15% y un 50%.</span><span class="sxs-lookup"><span data-stu-id="20ff8-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="20ff8-111">Un valor inferior al 15% es casi imperceptible; un valor mayor que 50% cada vez más es más aleatorio.</span><span class="sxs-lookup"><span data-stu-id="20ff8-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="20ff8-112">Para obtener una referencia a la celda **SketchFillChange** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="20ff8-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20ff8-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="20ff8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="20ff8-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="20ff8-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="20ff8-115">Para obtener una referencia a la celda **SketchFillChange** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="20ff8-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20ff8-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="20ff8-116">Section index:</span></span>  <br/> |<span data-ttu-id="20ff8-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20ff8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20ff8-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="20ff8-118">Row index:</span></span>  <br/> |<span data-ttu-id="20ff8-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="20ff8-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="20ff8-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="20ff8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="20ff8-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="20ff8-121">**visSketchFillChange**</span></span> <br/> |
   

