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
description: Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439467"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="33288-103">Fila PolylineTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="33288-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="33288-104">Contiene las coordenadas *x* e y del último punto de una polilínea y una fórmula de polilínea. \*\*</span><span class="sxs-lookup"><span data-stu-id="33288-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="33288-105">Las filas PolylineTo contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="33288-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="33288-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="33288-106">**Cell**</span></span>|<span data-ttu-id="33288-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33288-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33288-108">X</span><span class="sxs-lookup"><span data-stu-id="33288-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="33288-109">Coordenada *x* del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="33288-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="33288-110">Y</span><span class="sxs-lookup"><span data-stu-id="33288-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="33288-111">Coordenada *y* del vértice del extremo de una polilínea.</span><span class="sxs-lookup"><span data-stu-id="33288-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="33288-112">A</span><span class="sxs-lookup"><span data-stu-id="33288-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="33288-113">Fórmula de polilínea.</span><span class="sxs-lookup"><span data-stu-id="33288-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33288-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33288-114">Remarks</span></span>

<span data-ttu-id="33288-115">Las líneas representadas como fila Polyline son equivalentes a las líneas representadas como una secuencia de filas lineTo, pero la fila Polyline es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="33288-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="33288-116">Puede cambiar una fila PolylineTo a una fila lineTo para que pueda ver fácilmente la geometría de forma.</span><span class="sxs-lookup"><span data-stu-id="33288-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="33288-117">Para ello, haga clic con el botón secundario en la fila PolylineTo y, a continuación, haga clic en **expandir fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="33288-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="33288-118">Para cambiar un tipo de fila a una fila PolylineTo, haga clic con el botón secundario en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="33288-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

