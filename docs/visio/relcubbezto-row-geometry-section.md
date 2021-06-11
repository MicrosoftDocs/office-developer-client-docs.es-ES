---
title: Fila RelCubBezTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene las coordenadas x - e y del extremo de una curva bézier cúbica en relación con el ancho y alto de la forma, las coordenadas x - e y del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas x - e y del punto de control del final del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430332"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="7b163-103">Fila RelCubBezTo (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="7b163-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="7b163-104">Contiene las coordenadas  *x*  - e  *y*  del extremo de una curva bézier cúbica en relación con el ancho y alto de la forma, las coordenadas  *x*  -  *e y*  del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas  *x*  - e y del  *punto*  de control del final del ancho y alto de la forma relativa de la curva.</span><span class="sxs-lookup"><span data-stu-id="7b163-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7b163-105">Una **fila RelCubBezTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="7b163-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="7b163-106">Cuando se guarda un archivo en los formatos Visio 2003-2010, la fila **RelCubBezTo** se convierte en una [fila NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="7b163-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="7b163-107">Una **fila RelCubBezTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7b163-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="7b163-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="7b163-108">**Cell**</span></span>|<span data-ttu-id="7b163-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b163-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b163-110">X</span><span class="sxs-lookup"><span data-stu-id="7b163-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-111">La coordenada  *x*  del vértice final de una curva bézier cúbica con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="7b163-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="7b163-112">Y</span><span class="sxs-lookup"><span data-stu-id="7b163-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-113">Coordenada  *y*  del vértice final de una curva bézier cúbica con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="7b163-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="7b163-114">A</span><span class="sxs-lookup"><span data-stu-id="7b163-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-115">La coordenada  *x*  del punto de control inicial de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre los vértices inicial y final del arco.</span><span class="sxs-lookup"><span data-stu-id="7b163-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="7b163-116">B</span><span class="sxs-lookup"><span data-stu-id="7b163-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-117">Coordenada  *y*  del punto de control inicial de una curva con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="7b163-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="7b163-118">C</span><span class="sxs-lookup"><span data-stu-id="7b163-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-119">La coordenada  *x*  del punto de control final de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre el punto de control inicial y los vértices finales del arco.</span><span class="sxs-lookup"><span data-stu-id="7b163-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="7b163-120">D</span><span class="sxs-lookup"><span data-stu-id="7b163-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="7b163-121">Coordenada  *y*  del punto de control final de una curva con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="7b163-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

