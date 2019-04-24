---
title: Fila SplineKnot (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contiene las coordenadas x e y del punto de control de una spline y de un nodo de una spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328129"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="95965-103">Fila SplineKnot (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="95965-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="95965-104">Contiene las coordenadas *x* e y del punto de control de una spline y de un nodo de una spline. \*\*</span><span class="sxs-lookup"><span data-stu-id="95965-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="95965-105">Las filas SplineKnot contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="95965-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="95965-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="95965-106">**Cell**</span></span>|<span data-ttu-id="95965-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95965-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95965-108">X</span><span class="sxs-lookup"><span data-stu-id="95965-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="95965-109">Coordenada *x* de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="95965-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="95965-110">Y</span><span class="sxs-lookup"><span data-stu-id="95965-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="95965-111">Coordenada *y* de un punto de control.</span><span class="sxs-lookup"><span data-stu-id="95965-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="95965-112">A</span><span class="sxs-lookup"><span data-stu-id="95965-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="95965-113">Uno de los nodos de la spline (cualquiera menos el último o los dos primeros).</span><span class="sxs-lookup"><span data-stu-id="95965-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95965-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95965-114">Remarks</span></span>

<span data-ttu-id="95965-p101">Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.</span><span class="sxs-lookup"><span data-stu-id="95965-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

