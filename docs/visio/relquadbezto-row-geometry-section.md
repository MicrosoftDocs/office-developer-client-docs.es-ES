---
title: Fila RelQuadBezTo (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contiene las coordenadas x - e y del extremo de una curva Bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas x - e y del punto de control del ancho y alto relativos de la forma de curva.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423359"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="b3319-103">Fila RelQuadBezTo (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="b3319-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="b3319-104">Contiene las coordenadas  *x*  - e  *y*  del extremo de una curva Bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas  *x*  - e  *y*  del punto de control del ancho y alto relativos de la forma de curva.</span><span class="sxs-lookup"><span data-stu-id="b3319-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b3319-105">Una **fila RelQuadBezTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="b3319-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="b3319-106">Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelQuadBezTo** se convierte en una fila [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="b3319-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="b3319-107">Una **fila RelQuadBezTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b3319-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="b3319-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b3319-108">**Cell**</span></span>|<span data-ttu-id="b3319-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3319-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3319-110">X</span><span class="sxs-lookup"><span data-stu-id="b3319-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b3319-111">Coordenada  *x*  del vértice final de una curva Bézier cuadrática con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="b3319-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b3319-112">Y</span><span class="sxs-lookup"><span data-stu-id="b3319-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b3319-113">Coordenada  *y*  del vértice final de una curva Bézier cuadrática con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="b3319-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b3319-114">A</span><span class="sxs-lookup"><span data-stu-id="b3319-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b3319-115">Coordenada  *x*  del punto de control de la curva con relación al ancho de la forma; un punto del arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco.</span><span class="sxs-lookup"><span data-stu-id="b3319-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b3319-116">B</span><span class="sxs-lookup"><span data-stu-id="b3319-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b3319-117">Coordenada  *y*  del punto de control de una curva con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="b3319-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

