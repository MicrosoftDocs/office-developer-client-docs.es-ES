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
description: Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822216"
---
# <a name="geometry-section"></a><span data-ttu-id="26a2a-103">Sección de geometría</span><span class="sxs-lookup"><span data-stu-id="26a2a-103">Geometry Section</span></span>

<span data-ttu-id="26a2a-104">Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="26a2a-105">La geometría de una forma se puede expresar en varias secciones de **geometría** .</span><span class="sxs-lookup"><span data-stu-id="26a2a-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="26a2a-106">Varias rutas de acceso pueden ser útiles cuando varias rutas de acceso tienen propiedades diferentes (por ejemplo, las rutas de acceso de [recorte de imágenes](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="26a2a-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="26a2a-107">Notas</span><span class="sxs-lookup"><span data-stu-id="26a2a-107">Remarks</span></span>

<span data-ttu-id="26a2a-108">La sección de **geometría** contiene los siguientes tipos de fila.</span><span class="sxs-lookup"><span data-stu-id="26a2a-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="26a2a-109">Para obtener información detallada, vea los temas de la fila.</span><span class="sxs-lookup"><span data-stu-id="26a2a-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="26a2a-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="26a2a-110">**Row**</span></span>|<span data-ttu-id="26a2a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26a2a-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26a2a-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-113">Va a una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-115">Dibuja una línea en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-117">Dibuja un arco circular en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-119">Dibuja un arco elíptico en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-121">Dibuja una polilínea, o líneas consecutivas, en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-123">Dibuja una no uniforme spline B racional (NURBS) una coordenada.</span><span class="sxs-lookup"><span data-stu-id="26a2a-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="26a2a-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-125">Inicia una spline.</span><span class="sxs-lookup"><span data-stu-id="26a2a-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="26a2a-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-127">Dibuja un segmento de spline en la coordenada de un nodo.</span><span class="sxs-lookup"><span data-stu-id="26a2a-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="26a2a-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-129">Dibuja una línea infinita de una coordenada a otra.</span><span class="sxs-lookup"><span data-stu-id="26a2a-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-130">Elipse</span><span class="sxs-lookup"><span data-stu-id="26a2a-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-131">Dibuja una elipse a partir de una coordenada central y unos ejes mayor y menor.</span><span class="sxs-lookup"><span data-stu-id="26a2a-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-133">Dibujar una curva Bézier cúbica en relación con el ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-135">Dibuja un arco elíptico en una coordenada en relación con el alto y el ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-137">Dibuja una línea a una coordenada relativa el alto y el ancho de una forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-139">Mover a una coordenada en relación con el ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="26a2a-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="26a2a-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="26a2a-141">Dibuja una curva Bézier cuadrática en relación con el ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26a2a-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="26a2a-142">Para cambiar un tipo de fila en esta sección, haga clic en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="26a2a-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

