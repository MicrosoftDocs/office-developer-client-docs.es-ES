---
title: Fila ArcTo (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contiene las coordenadas x e y y la curvatura de un arco circular.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341408"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="acaf0-103">Fila ArcTo (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="acaf0-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="acaf0-104">Contiene las coordenadas *x* e \*\* y y la curvatura de un arco circular.</span><span class="sxs-lookup"><span data-stu-id="acaf0-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="acaf0-105">Las filas ArcTo contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="acaf0-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="acaf0-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="acaf0-106">**Cell**</span></span>|<span data-ttu-id="acaf0-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acaf0-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acaf0-108">X</span><span class="sxs-lookup"><span data-stu-id="acaf0-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="acaf0-109">Coordenada *x* del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="acaf0-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="acaf0-110">Y</span><span class="sxs-lookup"><span data-stu-id="acaf0-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="acaf0-111">Coordenada *y* del vértice del extremo de un arco.</span><span class="sxs-lookup"><span data-stu-id="acaf0-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="acaf0-112">A</span><span class="sxs-lookup"><span data-stu-id="acaf0-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="acaf0-113">Distancia desde el punto medio del arco hasta el punto medio de su cuerda.</span><span class="sxs-lookup"><span data-stu-id="acaf0-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acaf0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acaf0-114">Remarks</span></span>

<span data-ttu-id="acaf0-p101">Los arcos que dibuja Visio son elípticos, incluso si se basan en un círculo. De forma predeterminada, los arcos dibujados se representan mediante una fila EllipticalArcTo en la ventana ShapeSheet. Para mostrar una fila ArcTo en una ventana ShapeSheet, tiene que dibujar un arco y, a continuación, cambiar el tipo de fila EllipticalArcTo por el tipo ArcTo; en efecto, está cambiando un arco elíptico por un arco circular.</span><span class="sxs-lookup"><span data-stu-id="acaf0-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="acaf0-118">Para cambiar un tipo de fila, haga clic con el botón secundario en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="acaf0-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

