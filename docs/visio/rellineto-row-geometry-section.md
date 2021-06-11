---
title: Fila RelLineTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contiene las coordenadas x -e y del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437165"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="eb66d-103">Fila RelLineTo (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="eb66d-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="eb66d-104">Contiene  *las coordenadas x*  *-e y*  del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.</span><span class="sxs-lookup"><span data-stu-id="eb66d-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eb66d-105">Una **fila RelLineTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm.</span><span class="sxs-lookup"><span data-stu-id="eb66d-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="eb66d-106">Cuando se guarda un archivo en los formatos Visio 2003-2010, la fila **RelLineTo** se convierte en una [fila LineTo.](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="eb66d-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="eb66d-107">Una **fila RelLineTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb66d-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="eb66d-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="eb66d-108">**Cell**</span></span>|<span data-ttu-id="eb66d-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb66d-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb66d-110">X</span><span class="sxs-lookup"><span data-stu-id="eb66d-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="eb66d-111">Coordenada  *x*  del vértice final de un segmento de línea recta con relación al ancho de la forma.</span><span class="sxs-lookup"><span data-stu-id="eb66d-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="eb66d-112">Y</span><span class="sxs-lookup"><span data-stu-id="eb66d-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="eb66d-113">Coordenada  *y*  del vértice final de un segmento de línea recta con relación al alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="eb66d-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb66d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb66d-114">Remarks</span></span>

<span data-ttu-id="eb66d-115">Los valores de **la fila RelLineTo** son equivalentes a los valores de una fila [LineTo](lineto-row-geometry-section.md) que se multiplican por el ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="eb66d-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="eb66d-116">Por ejemplo: una fila **RelLineTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" se puede reemplazar por fila **LineTo** donde el valor de la celda **X** es la fórmula "Width *0"* y la celda Y es la fórmula "Height 0.5".</span><span class="sxs-lookup"><span data-stu-id="eb66d-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width *0" and the **Y** cell is the formula "Height* 0.5."</span></span> 
  

