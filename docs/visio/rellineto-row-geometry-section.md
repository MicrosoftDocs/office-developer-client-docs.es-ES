---
title: Fila de RelLineTo (sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contiene x - e y-coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822941"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="f0ad9-103">Fila de RelLineTo (sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="f0ad9-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="f0ad9-104">Contiene *x* - e *y* -coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0ad9-105">Una fila de **RelLineTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="f0ad9-106">Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelLineTo** se convierte en una fila [LineTo](lineto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ad9-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="f0ad9-107">Una fila de **RelLineTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="f0ad9-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f0ad9-108">**Cell**</span></span>|<span data-ttu-id="f0ad9-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0ad9-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ad9-110">X</span><span class="sxs-lookup"><span data-stu-id="f0ad9-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="f0ad9-111">La *x* -coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="f0ad9-112">Y</span><span class="sxs-lookup"><span data-stu-id="f0ad9-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="f0ad9-113">La *y* -coordenadas del vértice del extremo de un segmento de línea recta con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ad9-114">Notas</span><span class="sxs-lookup"><span data-stu-id="f0ad9-114">Remarks</span></span>

<span data-ttu-id="f0ad9-115">Valores de la fila de **RelLineTo** son equivalentes a los valores de una fila [LineTo](lineto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="f0ad9-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="f0ad9-116">Por ejemplo: una fila **RelLineTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" que se puede reemplazar con fila **LineTo** donde el valor de la celda **X** es la fórmula "ancho*0" y la celda **Y** es la fórmula de "alto*0,5."</span><span class="sxs-lookup"><span data-stu-id="f0ad9-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

