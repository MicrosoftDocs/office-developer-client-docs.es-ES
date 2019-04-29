---
title: Sección de geometría
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423912"
---
# <a name="geometry-section"></a><span data-ttu-id="c7fb9-103">Sección de geometría</span><span class="sxs-lookup"><span data-stu-id="c7fb9-103">Geometry Section</span></span>

<span data-ttu-id="c7fb9-104">Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="c7fb9-105">La geometría de una forma se puede expresar en varias secciones de **geometría** .</span><span class="sxs-lookup"><span data-stu-id="c7fb9-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="c7fb9-106">Las rutas de varias rutas pueden ser útiles cuando varias rutas tienen propiedades diferentes (por ejemplo, rutas de recorte de [imágenes](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="c7fb9-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7fb9-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7fb9-107">Remarks</span></span>

<span data-ttu-id="c7fb9-108">La sección **Geometry** contiene los siguientes tipos de fila.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="c7fb9-109">Para obtener más detalles, vea los temas acerca de las filas.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="c7fb9-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-110">**Row**</span></span>|<span data-ttu-id="c7fb9-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7fb9-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-113">Va a una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-115">Dibuja una línea en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-117">Dibuja un arco circular en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-119">Dibuja un arco elíptico en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-121">Dibuja una polilínea, o líneas consecutivas, en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-123">Dibuja una spline B racional no uniforme (NURBS) en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="c7fb9-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-125">Inicia una spline.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="c7fb9-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-127">Dibuja un segmento de spline en la coordenada de un nodo.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="c7fb9-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-129">Dibuja una línea infinita de una coordenada a otra.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-130">Origina</span><span class="sxs-lookup"><span data-stu-id="c7fb9-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-131">Dibuja una elipse a partir de una coordenada central y unos ejes mayor y menor.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-133">Dibuja una curva Bézier cúbica en relación con el ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-135">Dibuja un arco elíptico en una coordenada con relación al alto y ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-137">Dibuja una línea en una coordenada con relación al alto y el ancho de una forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-139">Se desplaza a una coordenada con relación al ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c7fb9-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="c7fb9-141">Dibuja una curva Bézier cuadrática con relación al ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="c7fb9-142">Para cambiar un tipo de fila en esta sección, haga clic con el botón secundario en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

