---
title: Celda DisplayLevel (sección de diseño de la forma [Shape Layout])
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Determina la banda del nivel de presentación (el intervalo relativo de la agrupación de orden Z) de la forma.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408148"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="fce0b-103">Celda DisplayLevel (sección de diseño de la forma [Shape Layout])</span><span class="sxs-lookup"><span data-stu-id="fce0b-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="fce0b-104">Determina la banda del nivel de presentación (el intervalo relativo de la agrupación de orden Z) de la forma.</span><span class="sxs-lookup"><span data-stu-id="fce0b-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fce0b-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fce0b-105">Remarks</span></span>

<span data-ttu-id="fce0b-p101">El orden Z es el orden de presentación de las formas en la página de dibujo. Una forma que se encuentra más arriba en el orden Z aparecerá delante de otra que se encuentra más abajo en el orden Z cuando una se superpone a la otra.</span><span class="sxs-lookup"><span data-stu-id="fce0b-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="fce0b-p102">El nivel de presentación divide las formas en agrupaciones o bandas. Todas las formas de una banda determinada tienen un orden Z superior al de las formas en la banda inferior. De manera predeterminada, la mayoría de las formas tiene un nivel de presentación igual a cero (0).</span><span class="sxs-lookup"><span data-stu-id="fce0b-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="fce0b-p103">El intervalo de los niveles de presentación oscila entre -32.767 y +32.767. Las formas que tienen el mismo nivel de presentación se combinan en una única banda, donde también se clasificarán entre sí según el orden Z.</span><span class="sxs-lookup"><span data-stu-id="fce0b-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="fce0b-113">Puede cambiar el orden Z de las formas dentro de una banda mediante los comandos **Bring Forward**, **Send Backward**, Bring to **Front** y Send **to Back**.</span><span class="sxs-lookup"><span data-stu-id="fce0b-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="fce0b-114">Si esos comandos mueven una forma fuera de su banda determinada, Microsoft Visio muestra el valor reservado -32768 en la celda DisplayLevel de la forma, a menos que la celda esté resguardada.</span><span class="sxs-lookup"><span data-stu-id="fce0b-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="fce0b-115">En ese caso, la forma no se puede mover a una banda diferente y Visio muestra la advertencia "La protección de formas o las propiedades de capa impiden la ejecución completa de este comando".</span><span class="sxs-lookup"><span data-stu-id="fce0b-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="fce0b-116">Para obtener una referencia desde otra fórmula a la celda DisplayLevel por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="fce0b-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fce0b-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fce0b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="fce0b-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="fce0b-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="fce0b-119">Para obtener una referencia desde un programa a la celda DisplayLevel por su índice, use la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fce0b-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fce0b-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fce0b-120">Section index:</span></span>  <br/> |<span data-ttu-id="fce0b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fce0b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fce0b-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fce0b-122">Row index:</span></span>  <br/> |<span data-ttu-id="fce0b-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="fce0b-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="fce0b-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fce0b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fce0b-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="fce0b-125">**visSLODisplayLevel**</span></span> <br/> |
   

