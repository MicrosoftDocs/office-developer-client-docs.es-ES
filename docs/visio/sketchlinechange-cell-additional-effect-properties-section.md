---
title: Celda SketchLineChange (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina la cantidad de selección aleatoria de línea de la forma en la geometría de la forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchLineChange se establece en 0%, la geometría de la línea de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de la línea de la forma no siguen la geometría de la forma.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823259"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="146fb-105">Celda SketchLineChange (sección Propiedades del efecto adicional)</span><span class="sxs-lookup"><span data-stu-id="146fb-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="146fb-106">Determina la cantidad de selección aleatoria de línea de la forma en la geometría de la forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección.</span><span class="sxs-lookup"><span data-stu-id="146fb-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="146fb-107">Si el valor de la celda **SketchLineChange** se establece en 0%, la geometría de la línea de la forma coincide con la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="146fb-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="146fb-108">Si el valor es 100%, la geometría de la línea de la forma no siguen la geometría de la forma.</span><span class="sxs-lookup"><span data-stu-id="146fb-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="146fb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="146fb-109">Remarks</span></span>

<span data-ttu-id="146fb-110">Para obtener mejores resultados, el intervalo de valores de la celda **SketchLineChange** ideal está entre el 15% y un 50%.</span><span class="sxs-lookup"><span data-stu-id="146fb-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="146fb-111">Un valor inferior al 15% es casi imperceptible; un valor mayor que el 50% pudo randomize demasiado la línea.</span><span class="sxs-lookup"><span data-stu-id="146fb-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="146fb-112">Para obtener una referencia a la celda **SketchLineChange** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="146fb-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="146fb-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="146fb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="146fb-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="146fb-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="146fb-115">Para obtener una referencia a la celda **SketchLineChange** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="146fb-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="146fb-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="146fb-116">Section index:</span></span>  <br/> |<span data-ttu-id="146fb-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="146fb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="146fb-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="146fb-118">Row index:</span></span>  <br/> |<span data-ttu-id="146fb-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="146fb-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="146fb-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="146fb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="146fb-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="146fb-121">**visSketchLineChange**</span></span> <br/> |
   

