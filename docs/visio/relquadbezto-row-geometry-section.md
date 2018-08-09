---
title: Fila RelQuadBezTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contiene x - y y - coordenadas del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y el x - e y-las coordenadas del punto de control del ancho y alto de la forma relativa de curva.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822985"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="44f71-103">Fila RelQuadBezTo (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="44f71-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="44f71-104">Contiene *el *x* - y *y* - coordenadas del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y el *x* - y* -las coordenadas del punto de control del ancho y alto de la forma relativa de curva.</span><span class="sxs-lookup"><span data-stu-id="44f71-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44f71-105">Una fila de **RelQuadBezTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="44f71-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="44f71-106">Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelQuadBezTo** se convierte en una fila [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="44f71-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="44f71-107">Una fila de **RelQuadBezTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="44f71-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="44f71-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="44f71-108">**Cell**</span></span>|<span data-ttu-id="44f71-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44f71-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44f71-110">X</span><span class="sxs-lookup"><span data-stu-id="44f71-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="44f71-111">La *x* -coordenadas del vértice del extremo de una curva Bézier cuadrática con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="44f71-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="44f71-112">Y</span><span class="sxs-lookup"><span data-stu-id="44f71-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="44f71-113">La *y* -coordenadas del vértice del extremo de una curva Bézier cuadrática con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="44f71-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="44f71-114">A</span><span class="sxs-lookup"><span data-stu-id="44f71-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="44f71-115">La *x* -coordenadas del punto de control de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco.</span><span class="sxs-lookup"><span data-stu-id="44f71-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="44f71-116">B</span><span class="sxs-lookup"><span data-stu-id="44f71-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="44f71-117">La *y* -coordenadas del punto de control de la curva con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="44f71-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

