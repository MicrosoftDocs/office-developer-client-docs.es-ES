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
description: Determina si los objetos son colocables o enrutables en diagramas cuando se disponen las formas con el comando Configurar diseño.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361015"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="6b4aa-103">Celda ObjType (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="6b4aa-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6b4aa-104">Determina si los objetos son colocables o enrutables en diagramas cuando se disponen las formas con el comando **Configurar diseño**.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="6b4aa-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-105">**Value**</span></span>|<span data-ttu-id="6b4aa-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-106">**Description**</span></span>|<span data-ttu-id="6b4aa-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b4aa-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="6b4aa-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="6b4aa-109">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-109">Default.</span></span> <span data-ttu-id="6b4aa-110">La aplicación decide según el contexto del dibujo.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-110">The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="6b4aa-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="6b4aa-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="6b4aa-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="6b4aa-113">La forma es colocable.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="6b4aa-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="6b4aa-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="6b4aa-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="6b4aa-116">La forma es enrutable.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-116">Shape is routable.</span></span> <span data-ttu-id="6b4aa-117">Debe ser una forma unidimensional (1D).</span><span class="sxs-lookup"><span data-stu-id="6b4aa-117">Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="6b4aa-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="6b4aa-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="6b4aa-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="6b4aa-120">La forma no es colocable ni enrutable.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="6b4aa-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="6b4aa-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="6b4aa-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="6b4aa-123">El grupo contiene formas colocables o enrutables.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="6b4aa-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b4aa-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b4aa-125">Remarks</span></span>

<span data-ttu-id="6b4aa-p103">De manera predeterminada, la celda ObjType se establece a No Formula para una forma. Esto equivale a 0, que significa que la aplicación determina si la forma puede ser colocable según su contexto. Por ejemplo, si dibuja un rectángulo simple, el valor de su celda ObjType es 0. Si, a continuación, usa la herramienta **Conector** para conectar el rectángulo a otra forma, Visio restablece el valor de la celda ObjType del rectángulo a 1 (colocable).</span><span class="sxs-lookup"><span data-stu-id="6b4aa-p103">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context. For example, if you draw a simple rectangle, the value of its ObjType cell is 0. If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="6b4aa-129">El valor de la celda ObjType puede ser una combinación de valores.</span><span class="sxs-lookup"><span data-stu-id="6b4aa-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="6b4aa-130">Sin embargo, si el bit no colocable&amp;está establecido (H4), tiene prioridad sobre otros valores excepto el valor de grupo&amp;(H8).</span><span class="sxs-lookup"><span data-stu-id="6b4aa-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="6b4aa-131">Para obtener una referencia a la celda ObjType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b4aa-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-132">Cell name:</span></span>  <br/> |<span data-ttu-id="6b4aa-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="6b4aa-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="6b4aa-134">Para obtener una referencia desde un programa a la celda ObjType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b4aa-135">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-135">Section index:</span></span>  <br/> |<span data-ttu-id="6b4aa-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6b4aa-137">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-137">Row index:</span></span>  <br/> |<span data-ttu-id="6b4aa-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="6b4aa-139">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6b4aa-139">Cell index:</span></span>  <br/> |<span data-ttu-id="6b4aa-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="6b4aa-140">**visLOFlags**</span></span> <br/> |
   

