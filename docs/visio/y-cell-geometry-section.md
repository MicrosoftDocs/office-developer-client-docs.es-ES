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
description: Representa una coordenada y de una forma en coordenadas locales. En la tabla siguiente se describe la celda Y según la fila en la que se encuentre.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420944"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="3ccda-104">Celda Y (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="3ccda-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="3ccda-105">Representa una coordenada *y* de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="3ccda-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="3ccda-106">En la tabla siguiente se describe la celda Y según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="3ccda-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="3ccda-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="3ccda-107">**Row**</span></span>|<span data-ttu-id="3ccda-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ccda-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ccda-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-110">Si la fila MoveTo es la primera fila de la sección, la celda Y representa la coordenada *Y* del primer vértice de una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3ccda-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="3ccda-111">Si la fila MoveTo aparece entre dos filas, la celda Y representa la coordenada *Y* del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3ccda-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-113">Coordenada *y* del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="3ccda-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-115">Coordenada *y* del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="3ccda-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-117">Coordenada *y* del vértice del extremo de un arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="3ccda-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-119">Coordenada *y* del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="3ccda-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3ccda-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-121">Coordenada *y* del último punto de control de una spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="3ccda-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="3ccda-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="3ccda-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-123">Coordenada *y* del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="3ccda-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="3ccda-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-125">Coordenada *y* de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="3ccda-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="3ccda-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-127">Coordenada *y* de un punto de la línea infinita.</span><span class="sxs-lookup"><span data-stu-id="3ccda-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="3ccda-128">Origina</span><span class="sxs-lookup"><span data-stu-id="3ccda-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="3ccda-129">Coordenada *y* del centro de la elipse.</span><span class="sxs-lookup"><span data-stu-id="3ccda-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ccda-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ccda-130">Remarks</span></span>

<span data-ttu-id="3ccda-131">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3ccda-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ccda-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3ccda-132">Cell name:</span></span>  <br/> | <span data-ttu-id="3ccda-133">Geometría *i* . Y *j* donde *i* y *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3ccda-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="3ccda-134">Geometría *i* . Y1 (filas InfiniteLine y Ellipse) donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3ccda-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3ccda-135">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3ccda-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ccda-136">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3ccda-136">Section index:</span></span>  <br/> |<span data-ttu-id="3ccda-137">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ccda-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ccda-138">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3ccda-138">Row index:</span></span>  <br/> |<span data-ttu-id="3ccda-139">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ccda-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="3ccda-140">**visRowVertex** (filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3ccda-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="3ccda-141">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3ccda-141">Cell index:</span></span>  <br/> |<span data-ttu-id="3ccda-142">**visY** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="3ccda-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="3ccda-143">**visInfiniteLineY1** (fila InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="3ccda-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="3ccda-144">**visEllipseCenterY** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3ccda-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

