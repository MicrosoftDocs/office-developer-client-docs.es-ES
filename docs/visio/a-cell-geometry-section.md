---
title: Celda A (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda A según la fila en la que se encuentre.
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821494"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="3506b-104">Celda A (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="3506b-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="3506b-p102">Representa distinta información según las filas. En la tabla siguiente se describe la celda A según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="3506b-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="3506b-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="3506b-107">**Row**</span></span>|<span data-ttu-id="3506b-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3506b-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3506b-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="3506b-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-110">Distancia desde el punto medio del arco hasta el punto medio de su cuerda.</span><span class="sxs-lookup"><span data-stu-id="3506b-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="3506b-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3506b-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-112">La *x* -coordenadas del punto de control del arco, un punto del arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco. De lo contrario, el arco puede crecer demasiado para pasar por el punto de control, con resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="3506b-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="3506b-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="3506b-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-114">Fórmula de polilínea.</span><span class="sxs-lookup"><span data-stu-id="3506b-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="3506b-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3506b-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-116">Penúltimo nodo de la spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="3506b-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="3506b-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="3506b-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-118">Segundo nodo de la spline.</span><span class="sxs-lookup"><span data-stu-id="3506b-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="3506b-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="3506b-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-120">Uno de los nodos de la spline (cualquiera menos el último o los dos primeros).</span><span class="sxs-lookup"><span data-stu-id="3506b-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="3506b-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="3506b-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-122">Una *x* -coordenadas de un punto de la línea infinita, emparejada con la *y* -coordenada representada por la celda [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3506b-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="3506b-123">Elipse</span><span class="sxs-lookup"><span data-stu-id="3506b-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="3506b-124">Una *x* -coordenadas de un punto de la elipse; emparejada con la *y* -coordenada representada por la celda [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3506b-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3506b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3506b-125">Remarks</span></span>

<span data-ttu-id="3506b-126">Para obtener una referencia a la celda A por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3506b-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3506b-127">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3506b-127">Cell name:</span></span>  <br/> | <span data-ttu-id="3506b-128">Geometría *i* . Un *j* donde *i* y *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3506b-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="3506b-129">Geometría *i* . A1 (filas InfiniteLine y Ellipse) donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3506b-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3506b-130">Para obtener una referencia a la celda A por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3506b-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3506b-131">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3506b-131">Section index:</span></span>  <br/> |<span data-ttu-id="3506b-132">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3506b-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3506b-133">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3506b-133">Row index:</span></span>  <br/> |<span data-ttu-id="3506b-134">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3506b-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="3506b-135">**visRowVertex** (filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3506b-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="3506b-136">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3506b-136">Cell index:</span></span>  <br/> |<span data-ttu-id="3506b-137">**visBow** (fila ArcTo)</span><span class="sxs-lookup"><span data-stu-id="3506b-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3506b-138">**visControlX** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="3506b-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3506b-139">**visControlY** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="3506b-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3506b-140">**visPolylineData** (fila Polyline)</span><span class="sxs-lookup"><span data-stu-id="3506b-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="3506b-141">**visNURBSKnot** (fila NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="3506b-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="3506b-142">**visSplineKnot** (filas SplineStart y SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="3506b-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="3506b-143">**visInfiniteLineX2** (fila InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="3506b-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="3506b-144">**visEllipseMajorX** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3506b-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

