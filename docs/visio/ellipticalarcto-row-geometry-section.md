---
title: Fila EllipticalArcTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contiene las coordenadas x - e y del extremo de un arco elíptico, x - e y - coordenadas de los puntos de control en el arco, el ángulo desde el eje x hasta el eje principal de la elipse y la relación entre los ejes principales y menores de la elipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421406"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="1bed7-103">Fila EllipticalArcTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="1bed7-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="1bed7-104">Contiene  *las*  coordenadas x - e  *y*  del extremo de un arco elíptico,  *x*  - e  *y*  -coordenadas de los puntos de control en el arco, el ángulo desde el eje  *x*  hasta el eje principal de la elipse y la relación entre los ejes principales y menores de la elipse.</span><span class="sxs-lookup"><span data-stu-id="1bed7-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="1bed7-105">Las filas EllipticalArcTo contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1bed7-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="1bed7-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1bed7-106">**Cell**</span></span>|<span data-ttu-id="1bed7-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1bed7-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bed7-108">X</span><span class="sxs-lookup"><span data-stu-id="1bed7-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-109">Coordenada  *x*  del vértice final de un arco.</span><span class="sxs-lookup"><span data-stu-id="1bed7-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="1bed7-110">Y</span><span class="sxs-lookup"><span data-stu-id="1bed7-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-111">*Coordenada y* del vértice final de un arco.</span><span class="sxs-lookup"><span data-stu-id="1bed7-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="1bed7-112">A</span><span class="sxs-lookup"><span data-stu-id="1bed7-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-113">Coordenada  *x*  del punto de control del arco; un punto del arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco. De lo contrario, el arco puede crecer hasta un tamaño extremo para pasar a través del punto de control, con resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="1bed7-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="1bed7-114">B</span><span class="sxs-lookup"><span data-stu-id="1bed7-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-115">Coordenada  *y*  del punto de control de un arco.</span><span class="sxs-lookup"><span data-stu-id="1bed7-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="1bed7-116">C</span><span class="sxs-lookup"><span data-stu-id="1bed7-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-117">Ángulo del eje principal de un arco con relación al eje  *X*  de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1bed7-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="1bed7-118">D</span><span class="sxs-lookup"><span data-stu-id="1bed7-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="1bed7-p101">Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="1bed7-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

