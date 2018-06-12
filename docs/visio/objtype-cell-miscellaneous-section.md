---
title: Celda ObjType (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Determina si los objetos son colocables o enrutables en diagramas cuando se usa el cuadro de diálogo Configurar diseño para diseñar las formas.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822703"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="791cb-103">Celda ObjType (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="791cb-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="791cb-104">Determina si los objetos son colocables o enrutables en diagramas cuando se usa el cuadro de diálogo **Configurar diseño** para diseñar las formas.</span><span class="sxs-lookup"><span data-stu-id="791cb-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="791cb-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="791cb-105">**Value**</span></span>|<span data-ttu-id="791cb-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="791cb-106">**Description**</span></span>|<span data-ttu-id="791cb-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="791cb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="791cb-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="791cb-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="791cb-p101">Valor predeterminado. La aplicación decide según el contexto del dibujo.</span><span class="sxs-lookup"><span data-stu-id="791cb-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="791cb-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="791cb-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="791cb-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="791cb-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="791cb-113">La forma es colocable.</span><span class="sxs-lookup"><span data-stu-id="791cb-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="791cb-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="791cb-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="791cb-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="791cb-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="791cb-p102">La forma es enrutable. Debe ser una forma unidimensional (1D).</span><span class="sxs-lookup"><span data-stu-id="791cb-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="791cb-118">**Crea**</span><span class="sxs-lookup"><span data-stu-id="791cb-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="791cb-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="791cb-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="791cb-120">La forma no es colocable ni enrutable.</span><span class="sxs-lookup"><span data-stu-id="791cb-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="791cb-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="791cb-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="791cb-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="791cb-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="791cb-123">El grupo contiene formas colocables o enrutables.</span><span class="sxs-lookup"><span data-stu-id="791cb-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="791cb-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="791cb-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="791cb-125">Notas</span><span class="sxs-lookup"><span data-stu-id="791cb-125">Remarks</span></span>

<span data-ttu-id="791cb-126">De forma predeterminada, la celda ObjType se establece a No Formula para una forma, que se evalúa como 0, lo que significa que la aplicación determina si la forma puede ser colocable según su contexto.</span><span class="sxs-lookup"><span data-stu-id="791cb-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="791cb-127">Por ejemplo, si dibuja un rectángulo simple, el valor de su celda ObjType es 0.</span><span class="sxs-lookup"><span data-stu-id="791cb-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="791cb-128">Si, a continuación, use la herramienta **conector** para conectar el rectángulo a otra forma, Visio restablece el valor de su celda ObjType del rectángulo en 1 (que puede colocarse).</span><span class="sxs-lookup"><span data-stu-id="791cb-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="791cb-129">El valor de la celda ObjType puede ser una combinación de valores.</span><span class="sxs-lookup"><span data-stu-id="791cb-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="791cb-130">Si está establecido el bit no colocable (&amp;H4), sin embargo, tiene prioridad sobre otros valores excepto el valor de grupo (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="791cb-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="791cb-131">Para obtener una referencia a la celda ObjType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="791cb-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="791cb-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="791cb-132">Cell name:</span></span>  <br/> |<span data-ttu-id="791cb-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="791cb-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="791cb-134">Para obtener una referencia a la celda ObjType por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="791cb-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="791cb-135">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="791cb-135">Section index:</span></span>  <br/> |<span data-ttu-id="791cb-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="791cb-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="791cb-137">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="791cb-137">Row index:</span></span>  <br/> |<span data-ttu-id="791cb-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="791cb-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="791cb-139">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="791cb-139">Cell index:</span></span>  <br/> |<span data-ttu-id="791cb-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="791cb-140">**visLOFlags**</span></span> <br/> |
   

