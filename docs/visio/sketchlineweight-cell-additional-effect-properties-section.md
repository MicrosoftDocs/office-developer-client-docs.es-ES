---
title: Celda SketchLineWeight (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Determina el grosor adicional que se agrega al grosor de línea como resultado de un efecto de boceto, en puntos entre 0 y 50. El grosor de la línea de una forma aumenta conforme aumenta el valor de la celda SketchLineWeight.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315123"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="52038-104">Celda SketchLineWeight (sección Propiedades del efecto adicional)</span><span class="sxs-lookup"><span data-stu-id="52038-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="52038-105">Determina el grosor adicional que se agrega al grosor de línea como resultado de un efecto de boceto, en puntos entre 0 y 50.</span><span class="sxs-lookup"><span data-stu-id="52038-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="52038-106">El grosor de la línea de una forma aumenta conforme aumenta el valor de la celda **SketchLineWeight** .</span><span class="sxs-lookup"><span data-stu-id="52038-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="52038-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52038-107">Remarks</span></span>

<span data-ttu-id="52038-108">Para obtener una referencia a la celda **SketchLineWeight** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="52038-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52038-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="52038-109">Cell name:</span></span>  <br/> | <span data-ttu-id="52038-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="52038-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="52038-111">Para obtener una referencia desde un programa a la celda **SketchLineWeight** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="52038-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52038-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="52038-112">Section index:</span></span>  <br/> |<span data-ttu-id="52038-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52038-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52038-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="52038-114">Row index:</span></span>  <br/> |<span data-ttu-id="52038-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="52038-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="52038-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="52038-116">Cell index:</span></span>  <br/> |<span data-ttu-id="52038-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="52038-117">**visSketchLineWeight**</span></span> <br/> |
   

