---
title: Fila PolylineTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contiene x - e y-coordenadas del último punto de una polilínea y una fórmula de polilínea.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822765"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="41b9c-103">Fila PolylineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="41b9c-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="41b9c-104">Contiene *x* - e *y* -coordenadas del último punto de una polilínea y una fórmula de polilínea.</span><span class="sxs-lookup"><span data-stu-id="41b9c-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="41b9c-105">Las filas PolylineTo contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="41b9c-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="41b9c-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="41b9c-106">**Cell**</span></span>|<span data-ttu-id="41b9c-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41b9c-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41b9c-108">X</span><span class="sxs-lookup"><span data-stu-id="41b9c-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="41b9c-109">La *x* -coordenadas del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="41b9c-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="41b9c-110">Y</span><span class="sxs-lookup"><span data-stu-id="41b9c-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="41b9c-111">La *y* -coordenadas del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="41b9c-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="41b9c-112">A</span><span class="sxs-lookup"><span data-stu-id="41b9c-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="41b9c-113">Fórmula de polilínea.</span><span class="sxs-lookup"><span data-stu-id="41b9c-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b9c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41b9c-114">Remarks</span></span>

<span data-ttu-id="41b9c-115">Las líneas representadas por una fila de polilínea son equivalentes a las líneas que se representan como una secuencia de filas LineTo, pero la fila Polyline es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="41b9c-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="41b9c-116">Puede cambiar una fila PolylineTo a una fila LineTo para que pueda ver fácilmente la geometría de forma.</span><span class="sxs-lookup"><span data-stu-id="41b9c-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="41b9c-117">Para ello, haga clic en la fila PolylineTo y, a continuación, haga clic en **Expandir fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="41b9c-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="41b9c-118">Para cambiar un tipo de fila por una fila PolylineTo, haga clic en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="41b9c-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

