---
title: Celda C (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda C según la fila en la que se encuentre.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821700"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="f2afb-104">Celda C (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="f2afb-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="f2afb-p102">Representa distinta información según las filas. En la tabla siguiente se describe la celda C según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="f2afb-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="f2afb-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="f2afb-107">**Row**</span></span>|<span data-ttu-id="f2afb-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2afb-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2afb-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f2afb-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="f2afb-110">Ángulo del eje mayor de un arco con respecto a la *x* -eje de su forma principal.</span><span class="sxs-lookup"><span data-stu-id="f2afb-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="f2afb-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="f2afb-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="f2afb-112">Primer nodo de la spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="f2afb-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="f2afb-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="f2afb-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="f2afb-114">Último nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="f2afb-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f2afb-115">Elipse</span><span class="sxs-lookup"><span data-stu-id="f2afb-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="f2afb-116">Una *x* -coordenadas de un punto de una elipse; emparejada con la *y* -coordenada representada por la celda [d.](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f2afb-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2afb-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2afb-117">Remarks</span></span>

<span data-ttu-id="f2afb-118">Para obtener una referencia a la celda C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f2afb-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2afb-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f2afb-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f2afb-120">Geometría *i* . C *j* donde *i* y *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f2afb-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="f2afb-121">Geometría *i* . C1 (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2afb-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="f2afb-122">Para obtener una referencia a la celda C por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2afb-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2afb-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f2afb-123">Section index:</span></span>  <br/> |<span data-ttu-id="f2afb-124">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2afb-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f2afb-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f2afb-125">Row index:</span></span>  <br/> |<span data-ttu-id="f2afb-126">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2afb-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="f2afb-127">**visRowVertex** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2afb-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="f2afb-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f2afb-128">Cell index:</span></span>  <br/> |<span data-ttu-id="f2afb-129">**visEccentricityAngle** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="f2afb-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="f2afb-130">**visNURBSKnotPrev** (fila NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="f2afb-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="f2afb-131">**visSplineKnot3** (fila SplineStart)</span><span class="sxs-lookup"><span data-stu-id="f2afb-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="f2afb-132">**visEllipseMinorX** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2afb-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

