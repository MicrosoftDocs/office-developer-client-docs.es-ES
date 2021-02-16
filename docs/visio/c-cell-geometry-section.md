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
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541893"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="ad8a4-104">Celda C (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="ad8a4-105">Representa distinta información según las filas.</span><span class="sxs-lookup"><span data-stu-id="ad8a4-105">Represents different information in different rows.</span></span> <span data-ttu-id="ad8a4-106">En la tabla siguiente se describe la celda C según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="ad8a4-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="ad8a4-107">Fila</span><span class="sxs-lookup"><span data-stu-id="ad8a4-107">Row</span></span>|<span data-ttu-id="ad8a4-108">Description</span><span class="sxs-lookup"><span data-stu-id="ad8a4-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad8a4-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="ad8a4-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="ad8a4-110">Ángulo del eje principal de un arco con relación al eje  *X*  de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="ad8a4-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="ad8a4-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ad8a4-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ad8a4-112">Primer nodo de la spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="ad8a4-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="ad8a4-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="ad8a4-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="ad8a4-114">Último nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="ad8a4-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="ad8a4-115">Elipse</span><span class="sxs-lookup"><span data-stu-id="ad8a4-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="ad8a4-116">Coordenada *x* de un punto de una elipse; emparejado con la *coordenada y* representada por la [celda D.](d-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad8a4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad8a4-117">Remarks</span></span>

<span data-ttu-id="ad8a4-118">Para obtener una referencia a la celda C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad8a4-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ad8a4-120">Geometría  *i*  . C  *j*            donde  *i*  y  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ad8a4-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="ad8a4-121">Geometría  *i*  . C1 (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="ad8a4-122">Para obtener una referencia a la celda C por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad8a4-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-123">Section index:</span></span>  <br/> |<span data-ttu-id="ad8a4-124">**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ad8a4-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ad8a4-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-125">Row index:</span></span>  <br/> |<span data-ttu-id="ad8a4-126">**visRowVertex**  +   *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ad8a4-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="ad8a4-127">**visRowVertex** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="ad8a4-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ad8a4-128">Cell index:</span></span>  <br/> |<span data-ttu-id="ad8a4-129">**visEccentricityAngle** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="ad8a4-130">**visNURBSKnotPrev** (fila NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="ad8a4-131">**visSplineKnot3** (fila SplineStart)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="ad8a4-132">**visEllipseMinorX** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ad8a4-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

