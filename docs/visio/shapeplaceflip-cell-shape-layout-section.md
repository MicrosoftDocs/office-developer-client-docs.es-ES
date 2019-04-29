---
title: Celda ShapePlaceFlip (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429281"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="c7bae-103">Celda ShapePlaceFlip (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="c7bae-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c7bae-104">Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="c7bae-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="c7bae-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c7bae-105">**Value**</span></span>|<span data-ttu-id="c7bae-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7bae-106">**Description**</span></span>|<span data-ttu-id="c7bae-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="c7bae-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7bae-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="c7bae-108">0</span></span>  <br/> |<span data-ttu-id="c7bae-109">Se utilizan las opciones predeterminadas de la página.</span><span class="sxs-lookup"><span data-stu-id="c7bae-109">Use page default.</span></span>  <br/> |<span data-ttu-id="c7bae-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="c7bae-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="c7bae-111">1</span><span class="sxs-lookup"><span data-stu-id="c7bae-111">1</span></span>  <br/> |<span data-ttu-id="c7bae-112">Se voltea horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c7bae-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="c7bae-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="c7bae-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="c7bae-114">segundo</span><span class="sxs-lookup"><span data-stu-id="c7bae-114">2</span></span>  <br/> |<span data-ttu-id="c7bae-115">Se voltea verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c7bae-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="c7bae-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="c7bae-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="c7bae-117">4 </span><span class="sxs-lookup"><span data-stu-id="c7bae-117">4</span></span>  <br/> |<span data-ttu-id="c7bae-118">Se voltea en incrementos de 90 grados entre 0 y 270.</span><span class="sxs-lookup"><span data-stu-id="c7bae-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="c7bae-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="c7bae-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="c7bae-120">8 </span><span class="sxs-lookup"><span data-stu-id="c7bae-120">8</span></span>  <br/> |<span data-ttu-id="c7bae-121">No se voltea.</span><span class="sxs-lookup"><span data-stu-id="c7bae-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="c7bae-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="c7bae-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7bae-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7bae-123">Remarks</span></span>

<span data-ttu-id="c7bae-124">El valor de la celda ShapePlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que esté conectada.</span><span class="sxs-lookup"><span data-stu-id="c7bae-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="c7bae-125">Para establecer este comportamiento para *todas* las formas de la página de dibujo, utilice la celda PlaceFlip de la sección de diseño de página.</span><span class="sxs-lookup"><span data-stu-id="c7bae-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="c7bae-126">Para obtener una referencia a la celda ShapePlaceFlip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="c7bae-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7bae-127">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c7bae-127">Cell name:</span></span>  <br/> |<span data-ttu-id="c7bae-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="c7bae-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="c7bae-129">Para obtener una referencia a la celda ShapePlaceFlip por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c7bae-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7bae-130">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c7bae-130">Section index:</span></span>  <br/> |<span data-ttu-id="c7bae-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7bae-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c7bae-132">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c7bae-132">Row index:</span></span>  <br/> |<span data-ttu-id="c7bae-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c7bae-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c7bae-134">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c7bae-134">Cell index:</span></span>  <br/> |<span data-ttu-id="c7bae-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="c7bae-135">**visSLOPlaceFlip**</span></span> <br/> |
   

