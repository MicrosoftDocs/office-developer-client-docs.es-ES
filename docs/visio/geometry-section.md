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
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542286"
---
# <a name="geometry-section"></a><span data-ttu-id="8d9fe-103">Sección de geometría</span><span class="sxs-lookup"><span data-stu-id="8d9fe-103">Geometry Section</span></span>

<span data-ttu-id="8d9fe-104">Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="8d9fe-105">La geometría de una forma se puede expresar en varias secciones **de** geometría.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="8d9fe-106">Varias rutas de acceso pueden ser útiles cuando varias rutas de acceso tienen propiedades diferentes (por ejemplo, rutas de recorte [de](clippingpath-cell-foreign-image-info-section.md) imágenes).</span><span class="sxs-lookup"><span data-stu-id="8d9fe-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d9fe-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d9fe-107">Remarks</span></span>

<span data-ttu-id="8d9fe-108">La **sección Geometría** contiene los siguientes tipos de fila.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="8d9fe-109">Para obtener más detalles, vea los temas acerca de las filas.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="8d9fe-110">Fila</span><span class="sxs-lookup"><span data-stu-id="8d9fe-110">Row</span></span>|<span data-ttu-id="8d9fe-111">Description</span><span class="sxs-lookup"><span data-stu-id="8d9fe-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d9fe-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-113">Va a una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-115">Dibuja una línea en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-117">Dibuja un arco circular en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-119">Dibuja un arco elíptico en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-121">Dibuja una polilínea, o líneas consecutivas, en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-123">Dibuja una spline B racional no uniforme (NURBS) en una coordenada.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="8d9fe-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-125">Inicia una spline.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="8d9fe-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-127">Dibuja un segmento de spline en la coordenada de un nodo.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="8d9fe-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-129">Dibuja una línea infinita de una coordenada a otra.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-130">Elipse</span><span class="sxs-lookup"><span data-stu-id="8d9fe-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-131">Dibuja una elipse a partir de una coordenada central y unos ejes mayor y menor.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-132">RelMtBezTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-133">Dibuja una curva Bézier cúbica con relación al ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-135">Dibuja un arco elíptico en una coordenada con relación al alto y ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-137">Dibujar una línea a una coordenada relativa al alto y ancho de una forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-139">Desplazarse a una coordenada relativa al ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="8d9fe-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="8d9fe-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="8d9fe-141">Dibuja una curva Bézier cuadrática con relación al ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="8d9fe-142">Para cambiar un tipo de fila en esta sección, haga clic con el botón secundario en la fila y, a continuación, haga clic en Cambiar tipo de fila **en** el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="8d9fe-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

