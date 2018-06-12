---
title: Fila SplineStart (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contiene x - e y-coordenadas para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823313"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="fdd3e-103">Fila SplineStart (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="fdd3e-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="fdd3e-104">Contiene *x* - e *y* -coordenadas para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="fdd3e-105">Las filas SplineStart contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="fdd3e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fdd3e-106">**Cell**</span></span>|<span data-ttu-id="fdd3e-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdd3e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdd3e-108">X</span><span class="sxs-lookup"><span data-stu-id="fdd3e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-109">La *x* -coordenadas del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="fdd3e-110">Y</span><span class="sxs-lookup"><span data-stu-id="fdd3e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-111">La *y* -coordenadas del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="fdd3e-112">A</span><span class="sxs-lookup"><span data-stu-id="fdd3e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-113">Segundo nodo de la spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="fdd3e-114">B</span><span class="sxs-lookup"><span data-stu-id="fdd3e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-115">Primer nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="fdd3e-116">C</span><span class="sxs-lookup"><span data-stu-id="fdd3e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-117">Último nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="fdd3e-118">D</span><span class="sxs-lookup"><span data-stu-id="fdd3e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="fdd3e-119">Grado de la spline (un número entero entre 1 y 25).</span><span class="sxs-lookup"><span data-stu-id="fdd3e-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdd3e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdd3e-120">Remarks</span></span>

<span data-ttu-id="fdd3e-p101">Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

