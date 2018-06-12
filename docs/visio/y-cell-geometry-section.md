---
title: Celda Y (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Representa una y-coordenadas en una forma en coordenadas locales. En esta tabla se describe la celda Y según la fila en la que se encuentre.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823595"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="d7fa1-104">Celda Y (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="d7fa1-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="d7fa1-105">Representa una *y* -coordenadas en una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="d7fa1-106">En esta tabla se describe la celda Y según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="d7fa1-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="d7fa1-107">**Row**</span></span>|<span data-ttu-id="d7fa1-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7fa1-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7fa1-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-110">Si la fila MoveTo es la primera fila en la sección, la celda Y representa la *y* -coordenadas del primer vértice de una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="d7fa1-111">Si la fila MoveTo aparece entre dos filas, la celda Y representa la *y* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-113">La *y* -coordenadas del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-115">La *y* -coordenadas del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-117">La *y* -coordenadas del vértice del extremo de un arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-119">La *y* -coordenadas del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d7fa1-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-121">La *y* -coordenadas del último punto de control de una B-spline racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="d7fa1-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="d7fa1-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-123">La *y* -coordenadas del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="d7fa1-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-125">La *y* -coordenadas de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="d7fa1-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-127">Una coordenada *y* de un punto de la línea infinita.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="d7fa1-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="d7fa1-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="d7fa1-129">La *y* -coordenadas del centro de la elipse.</span><span class="sxs-lookup"><span data-stu-id="d7fa1-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7fa1-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d7fa1-130">Remarks</span></span>

<span data-ttu-id="d7fa1-131">Para obtener una referencia a la celda Y por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7fa1-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-132">Cell name:</span></span>  <br/> | <span data-ttu-id="d7fa1-133">Geometría *i* . Y *j* donde *i* y *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d7fa1-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="d7fa1-134">Geometría *i* . Y1 (filas InfiniteLine y Ellipse) donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d7fa1-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d7fa1-135">Para obtener una referencia a la celda Y por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7fa1-136">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-136">Section index:</span></span>  <br/> |<span data-ttu-id="d7fa1-137">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7fa1-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7fa1-138">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-138">Row index:</span></span>  <br/> |<span data-ttu-id="d7fa1-139">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7fa1-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="d7fa1-140">**visRowVertex** (Filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="d7fa1-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="d7fa1-141">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d7fa1-141">Cell index:</span></span>  <br/> |<span data-ttu-id="d7fa1-142">**visY** (Filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="d7fa1-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="d7fa1-143">**visInfiniteLineY1** (Fila InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="d7fa1-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="d7fa1-144">**visEllipseCenterY** (Fila ellipse)</span><span class="sxs-lookup"><span data-stu-id="d7fa1-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

