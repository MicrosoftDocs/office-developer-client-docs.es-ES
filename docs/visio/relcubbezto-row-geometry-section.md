---
title: Fila RelCubBezTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene x - y y - las coordenadas del punto final de una curva de Bézier cúbica con relación al ancho de la forma y height, x - y y - las coordenadas del punto de control del principio de la x y el alto y el ancho de la forma relativa de curva - e y-coordenadas del control Elija l de la hora de finalización del ancho y alto de la forma relativa de curva.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822937"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="26f18-103">Fila RelCubBezTo (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="26f18-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="26f18-104">Contiene *el *x* - y *y* - las coordenadas del punto final de una curva de Bézier cúbica con relación al ancho de la forma y height, *x* - y* -las coordenadas del punto de control del principio de la forma relativa de curva width y height, y la *x* e *y* -las coordenadas del punto de control de la hora de finalización del ancho y alto de la forma relativa de curva.</span><span class="sxs-lookup"><span data-stu-id="26f18-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26f18-105">Una fila de **RelCubBezTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="26f18-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="26f18-106">Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelCubBezTo** se convierte en una fila [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="26f18-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="26f18-107">Una fila de **RelCubBezTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="26f18-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="26f18-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="26f18-108">**Cell**</span></span>|<span data-ttu-id="26f18-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26f18-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26f18-110">X</span><span class="sxs-lookup"><span data-stu-id="26f18-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-111">La *x* -coordenadas del vértice del extremo de una curva de Bézier cúbica con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="26f18-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="26f18-112">Y</span><span class="sxs-lookup"><span data-stu-id="26f18-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-113">La *y* -coordenadas del vértice del extremo de una curva de Bézier cúbica con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26f18-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="26f18-114">A</span><span class="sxs-lookup"><span data-stu-id="26f18-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-115">La *x* -coordenada de la curva inicial del punto de control con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor ubicado entre el principio y el vértice final del arco.</span><span class="sxs-lookup"><span data-stu-id="26f18-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="26f18-116">B</span><span class="sxs-lookup"><span data-stu-id="26f18-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-117">La *y* -coordenada de una curva inicial del punto de control con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26f18-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="26f18-118">C</span><span class="sxs-lookup"><span data-stu-id="26f18-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-119">La *x* -coordenada de la curva final del punto de control con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor ubicado entre los vértices de final y de punto de control de principio del arco.</span><span class="sxs-lookup"><span data-stu-id="26f18-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="26f18-120">D</span><span class="sxs-lookup"><span data-stu-id="26f18-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="26f18-121">La *y* -coordenada de una curva final del punto de control con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="26f18-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

