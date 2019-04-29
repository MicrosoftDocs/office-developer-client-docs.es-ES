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
description: Contiene las coordenadas x e y del segundo punto de control de una spline, su segundo nodo, su primer nodo, el último nodo y el grado de la spline.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417479"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="cb568-103">Fila SplineStart (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="cb568-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="cb568-104">Contiene las coordenadas *x* e y del segundo punto de control de una spline, su segundo nodo, su primer nodo, el último nodo y el grado de la spline. \*\*</span><span class="sxs-lookup"><span data-stu-id="cb568-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="cb568-105">Las filas SplineStart contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cb568-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="cb568-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cb568-106">**Cell**</span></span>|<span data-ttu-id="cb568-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb568-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb568-108">X</span><span class="sxs-lookup"><span data-stu-id="cb568-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-109">Coordenada *x* del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="cb568-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="cb568-110">Y</span><span class="sxs-lookup"><span data-stu-id="cb568-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-111">Coordenada *y* del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="cb568-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="cb568-112">A</span><span class="sxs-lookup"><span data-stu-id="cb568-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-113">Segundo nodo de la spline.</span><span class="sxs-lookup"><span data-stu-id="cb568-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="cb568-114">B</span><span class="sxs-lookup"><span data-stu-id="cb568-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-115">Primer nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="cb568-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="cb568-116">CA</span><span class="sxs-lookup"><span data-stu-id="cb568-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-117">Último nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="cb568-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="cb568-118">D</span><span class="sxs-lookup"><span data-stu-id="cb568-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="cb568-119">Grado de la spline (un número entero entre 1 y 25).</span><span class="sxs-lookup"><span data-stu-id="cb568-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb568-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb568-120">Remarks</span></span>

<span data-ttu-id="cb568-p101">Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.</span><span class="sxs-lookup"><span data-stu-id="cb568-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

