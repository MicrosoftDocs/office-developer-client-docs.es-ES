---
title: Celda ShapeFixedCode (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Especifica el comportamiento de colocación de una forma que puede colocarse.
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823140"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="9fd52-103">Celda ShapeFixedCode (sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="9fd52-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9fd52-104">Especifica el comportamiento de colocación de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="9fd52-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="9fd52-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9fd52-105">**Value**</span></span>|<span data-ttu-id="9fd52-106">**Modo de selección**</span><span class="sxs-lookup"><span data-stu-id="9fd52-106">**Selection mode**</span></span>|<span data-ttu-id="9fd52-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="9fd52-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fd52-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="9fd52-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="9fd52-109">No mover esta forma cuando se coloquen mediante el cuadro de diálogo **Configurar diseño** .</span><span class="sxs-lookup"><span data-stu-id="9fd52-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="9fd52-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="9fd52-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="9fd52-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="9fd52-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="9fd52-112">No mover esta forma y no permitir que se coloquen sobre ella otras formas que la quiten.</span><span class="sxs-lookup"><span data-stu-id="9fd52-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="9fd52-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="9fd52-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="9fd52-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="9fd52-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="9fd52-115">No mover esta forma y permitir colocar sobre ella otras formas que la quiten.</span><span class="sxs-lookup"><span data-stu-id="9fd52-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="9fd52-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="9fd52-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="9fd52-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="9fd52-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="9fd52-118">Omitir las ubicaciones de los puntos de conexión cuando se está enrutando.</span><span class="sxs-lookup"><span data-stu-id="9fd52-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="9fd52-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="9fd52-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="9fd52-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="9fd52-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="9fd52-121">Permitir el enrutamiento únicamente a los lados con puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="9fd52-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="9fd52-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="9fd52-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="9fd52-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="9fd52-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="9fd52-p101">No pegar al perímetro de esta forma. En lugar de ello, pegar al cuadro de alineación de la forma.</span><span class="sxs-lookup"><span data-stu-id="9fd52-p101">Don't glue to the perimeter of this shape. Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="9fd52-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="9fd52-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fd52-127">Notas</span><span class="sxs-lookup"><span data-stu-id="9fd52-127">Remarks</span></span>

<span data-ttu-id="9fd52-128">También puede establecer el valor de esta celda en la ficha de **colocación** en el cuadro de diálogo **comportamiento** (con una forma seleccionada, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en la ficha **colocación** ).</span><span class="sxs-lookup"><span data-stu-id="9fd52-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="9fd52-129">Puede establecer cualquier combinación de estos valores para esta celda.</span><span class="sxs-lookup"><span data-stu-id="9fd52-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="9fd52-130">Por ejemplo, puede escribir el valor 3 (&amp;H3), que elimina el movimiento al disponer formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño** , en el grupo **Diseño** , haga clic en **Página de diseño de Re**y, a continuación, haga clic en ** Más opciones de diseño** ) y cuando se colocan otras formas que puede colocarse en o cerca de la forma.</span><span class="sxs-lookup"><span data-stu-id="9fd52-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="9fd52-131">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="9fd52-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="9fd52-132">Para obtener una referencia a la celda ShapeFixedCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="9fd52-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fd52-133">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9fd52-133">Cell name:</span></span>  <br/> |<span data-ttu-id="9fd52-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="9fd52-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="9fd52-135">Para obtener una referencia a la celda ShapeFixedCode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9fd52-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fd52-136">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9fd52-136">Section index:</span></span>  <br/> |<span data-ttu-id="9fd52-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9fd52-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9fd52-138">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9fd52-138">Row index:</span></span>  <br/> |<span data-ttu-id="9fd52-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9fd52-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9fd52-140">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9fd52-140">Cell index:</span></span>  <br/> |<span data-ttu-id="9fd52-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="9fd52-141">**visSLOFixedCode**</span></span> <br/> |
   

