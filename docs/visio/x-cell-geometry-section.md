---
title: Celda X (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Representa una coordenada x de una forma en coordenadas locales. En la tabla siguiente se describe la celda X según la fila en la que se encuentre.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423947"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="7fa37-104">Celda X (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="7fa37-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="7fa37-105">Representa una coordenada *x* de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="7fa37-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="7fa37-106">En la tabla siguiente se describe la celda X según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="7fa37-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="7fa37-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="7fa37-107">**Row**</span></span>|<span data-ttu-id="7fa37-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa37-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa37-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-110">Si la fila MoveTo es la primera fila de la sección, la celda X representa la coordenada *x* del primer vértice de una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="7fa37-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="7fa37-111">Si la fila MoveTo aparece entre dos filas, la celda X representa la coordenada *x* del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="7fa37-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-113">Coordenada *x* del vértice del extremo de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="7fa37-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-115">Coordenada *x* del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="7fa37-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-117">Coordenada *x* del vértice del extremo de un arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="7fa37-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-119">Coordenada *x* del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="7fa37-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="7fa37-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-121">Coordenada *x* del último punto de control de una spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="7fa37-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="7fa37-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="7fa37-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-123">Coordenada *x* del segundo punto de control de una spline.</span><span class="sxs-lookup"><span data-stu-id="7fa37-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="7fa37-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-125">Coordenada *x* de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="7fa37-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="7fa37-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-127">Coordenada *x* de un punto de la línea infinita.</span><span class="sxs-lookup"><span data-stu-id="7fa37-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="7fa37-128">Origina</span><span class="sxs-lookup"><span data-stu-id="7fa37-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="7fa37-129">Coordenada *x* del centro de la elipse.</span><span class="sxs-lookup"><span data-stu-id="7fa37-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fa37-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7fa37-130">Remarks</span></span>

<span data-ttu-id="7fa37-131">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7fa37-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7fa37-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7fa37-132">Cell name:</span></span>  <br/> | <span data-ttu-id="7fa37-133">Geometría *i* . X *j* donde *i* y *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7fa37-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="7fa37-134">Geometría *i* . X1 (filas InfiniteLine y Ellipse) donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7fa37-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7fa37-135">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7fa37-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7fa37-136">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7fa37-136">Section index:</span></span>  <br/> |<span data-ttu-id="7fa37-137">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7fa37-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7fa37-138">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7fa37-138">Row index:</span></span>  <br/> |<span data-ttu-id="7fa37-139">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7fa37-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="7fa37-140">**visRowVertex** (filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7fa37-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="7fa37-141">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7fa37-141">Cell index:</span></span>  <br/> |<span data-ttu-id="7fa37-142">**visX** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="7fa37-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="7fa37-143">**visInfiniteLineX1** (fila InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="7fa37-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="7fa37-144">**visEllipseCenterX** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7fa37-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

