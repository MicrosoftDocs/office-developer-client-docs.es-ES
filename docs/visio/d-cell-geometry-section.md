---
title: Celda D (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda D según la fila en la que se encuentre.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542502"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="d58c0-104">Celda D (sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="d58c0-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="d58c0-105">Representa distinta información según las filas.</span><span class="sxs-lookup"><span data-stu-id="d58c0-105">Represents different information in different rows.</span></span> <span data-ttu-id="d58c0-106">En la tabla siguiente se describe la celda D según la fila en la que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="d58c0-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="d58c0-107">Fila</span><span class="sxs-lookup"><span data-stu-id="d58c0-107">Row</span></span>|<span data-ttu-id="d58c0-108">Description</span><span class="sxs-lookup"><span data-stu-id="d58c0-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d58c0-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="d58c0-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="d58c0-p103">Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="d58c0-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="d58c0-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d58c0-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d58c0-114">Primer grosor de la spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="d58c0-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="d58c0-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="d58c0-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="d58c0-116">Grado de la spline (un número entero entre 1 y 25).</span><span class="sxs-lookup"><span data-stu-id="d58c0-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="d58c0-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="d58c0-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="d58c0-118">*Coordenada y* de un punto de una elipse; emparejado con la coordenada *x* representada por la [celda C.](c-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="d58c0-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d58c0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d58c0-119">Remarks</span></span>

<span data-ttu-id="d58c0-120">Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d58c0-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d58c0-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d58c0-121">Cell name:</span></span>  <br/> | <span data-ttu-id="d58c0-122">Geometría  *i*  . D  *j*            donde  *i*  y  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d58c0-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="d58c0-123">Geometría  *i*  . D1 (fila Ellipse) donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d58c0-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d58c0-124">Para obtener una referencia desde un programa a la celda D por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d58c0-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d58c0-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d58c0-125">Section index:</span></span>  <br/> |<span data-ttu-id="d58c0-126">**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d58c0-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d58c0-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d58c0-127">Row index:</span></span>  <br/> |<span data-ttu-id="d58c0-128">**visRowVertex**  +   *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d58c0-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="d58c0-129">**visRowVertex** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="d58c0-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="d58c0-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d58c0-130">Cell index</span></span>  <br/> |<span data-ttu-id="d58c0-131">**visAspectRatio** (fila EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="d58c0-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="d58c0-132">**visNURBSWeightPrev** (fila NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="d58c0-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="d58c0-133">**visSplineDegree** (fila SplineStart)</span><span class="sxs-lookup"><span data-stu-id="d58c0-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="d58c0-134">**visEllipseMinorY** (fila Ellipse)</span><span class="sxs-lookup"><span data-stu-id="d58c0-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

