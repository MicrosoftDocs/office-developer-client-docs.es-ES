---
title: Fila MoveTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción en una ruta de acceso.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429701"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="38600-103">Fila MoveTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="38600-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="38600-104">Contiene las coordenadas *x* e \*\* y del primer vértice de una forma o representa las coordenadas *x* e y del primer vértice \*\* después de una interrupción en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="38600-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="38600-105">Las \*\*\*\* filas moveTo contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="38600-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="38600-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="38600-106">**Cell**</span></span>|<span data-ttu-id="38600-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38600-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38600-108">X</span><span class="sxs-lookup"><span data-stu-id="38600-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="38600-109">Si la \*\*\*\* fila MoveTo es la primera fila de la sección, la celda x representa la coordenada *x* del primer vértice de la forma.</span><span class="sxs-lookup"><span data-stu-id="38600-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="38600-110">Si la \*\*\*\* fila MoveTo aparece entre dos filas, la celda x representa la coordenada *x* del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="38600-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="38600-111">Y</span><span class="sxs-lookup"><span data-stu-id="38600-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="38600-112">Si la \*\*\*\* fila MoveTo es la primera fila de la sección, la celda y representa la coordenada *Y* del primer vértice de la forma.</span><span class="sxs-lookup"><span data-stu-id="38600-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="38600-113">Si la \*\*\*\* fila MoveTo aparece entre dos filas, la celda y representa la coordenada *Y* del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="38600-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38600-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38600-114">Remarks</span></span>

<span data-ttu-id="38600-115">La fila **moveTo** contiene las coordenadas *x* e \*\* y del primer vértice de la forma si la fila MoveTo \*\*\*\* es la primera fila de la sección.</span><span class="sxs-lookup"><span data-stu-id="38600-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="38600-116">Normalmente, se trata del primer vértice que se colocó al dibujar la forma y no corresponde necesariamente con el punto inicial de una forma unidimensional (1D).</span><span class="sxs-lookup"><span data-stu-id="38600-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="38600-117">Una sección Geometry debe comenzar con **RelMoveTo** o una fila **moveTo** , pero también puede usar las filas moveTo \*\*\*\* y **RelMoveTo** para representar un hueco en el trazado de la ruta de acceso de una forma.</span><span class="sxs-lookup"><span data-stu-id="38600-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="38600-118">Sin embargo, cuando la trayectoria se utiliza para definir el límite de una zona rellena, esta interrupción se interpreta como segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="38600-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="38600-119">Para insertar dicha brecha, inserte una fila entre dos filas y cambie el tipo de fila a **moveTo**.</span><span class="sxs-lookup"><span data-stu-id="38600-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="38600-120">Si la fila **moveTo** se encuentra entre dos filas, contiene las coordenadas *x* e \*\* y del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="38600-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

