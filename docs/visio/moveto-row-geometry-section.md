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
description: Contiene x - e y - las coordenadas del primer vértice de una forma o representa la x - e y-las coordenadas del primer vértice después de una interrupción de una ruta de acceso.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822663"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="cddbb-103">Fila MoveTo (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="cddbb-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="cddbb-104">Contiene el *x* - e *y* - las coordenadas del primer vértice de una forma o representa la *x* - e *y* -las coordenadas del primer vértice después de una interrupción de una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cddbb-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="cddbb-105">Una fila **MoveTo** contiene las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cddbb-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="cddbb-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cddbb-106">**Cell**</span></span>|<span data-ttu-id="cddbb-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cddbb-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cddbb-108">X</span><span class="sxs-lookup"><span data-stu-id="cddbb-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="cddbb-109">Si la fila **MoveTo** es la primera fila en la sección, la celda X representa la *x* -coordenadas del primer vértice de una forma.</span><span class="sxs-lookup"><span data-stu-id="cddbb-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="cddbb-110">Si la fila **MoveTo** aparece entre dos filas, la celda X representa la *x* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cddbb-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="cddbb-111">Y</span><span class="sxs-lookup"><span data-stu-id="cddbb-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="cddbb-112">Si la fila **MoveTo** es la primera fila en la sección, la celda Y representa la *y* -coordenadas del primer vértice de una forma.</span><span class="sxs-lookup"><span data-stu-id="cddbb-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="cddbb-113">Si la fila **MoveTo** aparece entre dos filas, la celda Y representa la *y* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cddbb-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cddbb-114">Notas</span><span class="sxs-lookup"><span data-stu-id="cddbb-114">Remarks</span></span>

<span data-ttu-id="cddbb-115">La fila **MoveTo** contiene el *x* - e *y* -las coordenadas del primer vértice de la forma si la fila **MoveTo** es la primera fila en la sección.</span><span class="sxs-lookup"><span data-stu-id="cddbb-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="cddbb-116">Suele ser el primer vértice que se colocó al dibujar la forma y no se corresponde necesariamente con el punto inicial de una forma 1-D.</span><span class="sxs-lookup"><span data-stu-id="cddbb-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="cddbb-117">Una sección de geometría debe comenzar con un **RelMoveTo** o una fila **MoveTo** , pero también puede utilizar las filas **MoveTo** y **RelMoveTo** para representar una interrupción en la trayectoria de una forma.</span><span class="sxs-lookup"><span data-stu-id="cddbb-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="cddbb-118">Sin embargo, cuando se usa la ruta de acceso para definir el límite de una región rellena, esta interrupción se interpreta como un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="cddbb-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="cddbb-119">Para insertar un espacio de este tipo, inserte una fila entre dos filas y cambie el tipo de fila a **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="cddbb-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="cddbb-120">Si la fila **MoveTo** está entre dos filas, contiene el *x* - e *y* -las coordenadas del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="cddbb-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

