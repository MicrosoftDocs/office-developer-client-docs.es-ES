---
title: Celda PlaceFlip (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Determina de qué manera se voltean o rotan las formas colocables en una página al usar el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434301"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="59e01-103">Celda PlaceFlip (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="59e01-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="59e01-104">Determina de qué manera se voltean o rotan las formas colocables en una página al usar el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="59e01-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="59e01-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="59e01-105">**Value**</span></span>|<span data-ttu-id="59e01-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59e01-106">**Description**</span></span>|<span data-ttu-id="59e01-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="59e01-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59e01-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="59e01-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="59e01-109">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="59e01-109">Default.</span></span> <span data-ttu-id="59e01-110">No se voltea.</span><span class="sxs-lookup"><span data-stu-id="59e01-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="59e01-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="59e01-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="59e01-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="59e01-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="59e01-113">Se voltea horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="59e01-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="59e01-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="59e01-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="59e01-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="59e01-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="59e01-116">Se voltea verticalmente.</span><span class="sxs-lookup"><span data-stu-id="59e01-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="59e01-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="59e01-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="59e01-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="59e01-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="59e01-119">Se voltea en incrementos de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="59e01-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="59e01-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="59e01-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="59e01-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="59e01-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="59e01-122">No se voltea.</span><span class="sxs-lookup"><span data-stu-id="59e01-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="59e01-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="59e01-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e01-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59e01-124">Remarks</span></span>

<span data-ttu-id="59e01-p102">El valor de la celda PlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que está conectada. Suele emplearse cuando se diseñan dibujos que precisan pegado estático.</span><span class="sxs-lookup"><span data-stu-id="59e01-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="59e01-127">Para establecer este comportamiento para una forma en particular, use la celda ShapePlaceFlip en la sección de diseño de la forma.</span><span class="sxs-lookup"><span data-stu-id="59e01-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="59e01-128">Para obtener una referencia a la celda PlaceFlip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="59e01-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59e01-129">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="59e01-129">Cell name:</span></span>  <br/> |<span data-ttu-id="59e01-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="59e01-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="59e01-131">Para obtener una referencia desde un programa a la celda PlaceFlip por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="59e01-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59e01-132">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="59e01-132">Section index:</span></span>  <br/> |<span data-ttu-id="59e01-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59e01-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="59e01-134">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="59e01-134">Row index:</span></span>  <br/> |<span data-ttu-id="59e01-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="59e01-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="59e01-136">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="59e01-136">Cell index:</span></span>  <br/> |<span data-ttu-id="59e01-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="59e01-137">**visPLOPlaceFlip**</span></span> <br/> |
   

