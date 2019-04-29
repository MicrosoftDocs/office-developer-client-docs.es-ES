---
title: Celda B (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda B según la fila en la que se encuentre.
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423310"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="01ed8-104">Celda B (sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="01ed8-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="01ed8-105">Representa distinta información según las filas.</span><span class="sxs-lookup"><span data-stu-id="01ed8-105">Represents different information in different rows.</span></span> <span data-ttu-id="01ed8-106">En la tabla siguiente se describe la celda B según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="01ed8-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="01ed8-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="01ed8-107">**Row**</span></span>|<span data-ttu-id="01ed8-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01ed8-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01ed8-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="01ed8-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="01ed8-110">Coordenada *y* del punto de control de un arco.</span><span class="sxs-lookup"><span data-stu-id="01ed8-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="01ed8-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="01ed8-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="01ed8-112">Último grosor de la spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="01ed8-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="01ed8-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="01ed8-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="01ed8-114">Primer nodo de una spline.</span><span class="sxs-lookup"><span data-stu-id="01ed8-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="01ed8-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="01ed8-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="01ed8-116">Coordenada *y* de un punto de una línea infinita; emparejado con la coordenada *x* representada por la celda [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="01ed8-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="01ed8-117">Origina</span><span class="sxs-lookup"><span data-stu-id="01ed8-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="01ed8-118">Coordenada *y* de un punto de una elipse; emparejado con la coordenada *x* representada por la celda [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="01ed8-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01ed8-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01ed8-119">Remarks</span></span>

<span data-ttu-id="01ed8-120">Para obtener una referencia a la celda B por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="01ed8-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01ed8-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="01ed8-121">Cell name:</span></span>  <br/> | <span data-ttu-id="01ed8-122">Geometría *i* . B *j* donde *i* y *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="01ed8-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="01ed8-123">Geometría *i* . B1 (filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="01ed8-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="01ed8-124">Para obtener una referencia a la celda B por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="01ed8-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01ed8-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="01ed8-125">Section index:</span></span>  <br/> |<span data-ttu-id="01ed8-126">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="01ed8-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="01ed8-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="01ed8-127">Row index:</span></span>  <br/> |<span data-ttu-id="01ed8-128">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="01ed8-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="01ed8-129">**visRowVertex** (filas InfiniteLine y Ellipse)</span><span class="sxs-lookup"><span data-stu-id="01ed8-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="01ed8-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="01ed8-130">Cell index:</span></span>  <br/> |<span data-ttu-id="01ed8-131">**visControlX** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="01ed8-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="01ed8-132">**visControlY** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="01ed8-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="01ed8-133">**visNURBSWeight** (fila NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="01ed8-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="01ed8-134">**visSplineKnot2** (fila SplineStart)</span><span class="sxs-lookup"><span data-stu-id="01ed8-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="01ed8-135">**visInfiniteLineY2** (fila InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="01ed8-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="01ed8-136">**visEllipseMajorY** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="01ed8-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

