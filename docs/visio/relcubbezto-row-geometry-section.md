---
title: Fila RelCubBezTo (sección geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene las coordenadas x e y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas x e y del punto de control del principio del ancho y el alto de la forma relativa de la curva, y las coordenadas x-e y-de contr punto l del final del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320037"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="6ff1b-103">Fila RelCubBezTo (sección geometría)</span><span class="sxs-lookup"><span data-stu-id="6ff1b-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="6ff1b-104">Contiene las coordenadas *x* e \*\* y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas *x* e y del punto de control del principio del ancho y el alto de la forma relativa de la curva. \*\* y las coordenadas *x* -e *y* -del punto de control del final del ancho y alto de la forma relativa de la curva.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ff1b-105">Una fila **RelCubBezTo** solo puede persistir en los formatos de archivo. vsdx,. vsdm,. vstx,. vstm,. vssx y. VSSM.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="6ff1b-106">Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelCubBezTo** se convierte en [](nurbsto-row-geometry-section.md) una fila NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="6ff1b-107">Una fila **RelCubBezTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="6ff1b-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6ff1b-108">**Cell**</span></span>|<span data-ttu-id="6ff1b-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ff1b-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ff1b-110">X</span><span class="sxs-lookup"><span data-stu-id="6ff1b-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-111">Coordenada *x* del vértice del extremo de una curva cúbica de Bézier con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="6ff1b-112">Y</span><span class="sxs-lookup"><span data-stu-id="6ff1b-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-113">Coordenada *y* del vértice del extremo de una curva cúbica de Bézier con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="6ff1b-114">A</span><span class="sxs-lookup"><span data-stu-id="6ff1b-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-115">Coordenada *x* del punto de control inicial de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor situado entre los vértices inicial y final del arco.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="6ff1b-116">B</span><span class="sxs-lookup"><span data-stu-id="6ff1b-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-117">Coordenada *y* del punto de control inicial de una curva en relación con el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="6ff1b-118">CA</span><span class="sxs-lookup"><span data-stu-id="6ff1b-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-119">Coordenada *x* del punto de control final de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor situado entre el punto de control inicial y los vértices finales del arco.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="6ff1b-120">D</span><span class="sxs-lookup"><span data-stu-id="6ff1b-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="6ff1b-121">Coordenada *y* del punto de control final de una curva en relación con el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

