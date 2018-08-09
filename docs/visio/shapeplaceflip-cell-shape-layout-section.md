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
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823156"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="c6bdd-103">Celda ShapePlaceFlip (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="c6bdd-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c6bdd-104">Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="c6bdd-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="c6bdd-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-105">**Value**</span></span>|<span data-ttu-id="c6bdd-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-106">**Description**</span></span>|<span data-ttu-id="c6bdd-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c6bdd-108">0</span><span class="sxs-lookup"><span data-stu-id="c6bdd-108">0</span></span>  <br/> |<span data-ttu-id="c6bdd-109">Se utilizan las opciones predeterminadas de la página.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-109">Use page default.</span></span>  <br/> |<span data-ttu-id="c6bdd-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="c6bdd-111">1</span><span class="sxs-lookup"><span data-stu-id="c6bdd-111">1</span></span>  <br/> |<span data-ttu-id="c6bdd-112">Se voltea horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="c6bdd-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="c6bdd-114">2</span><span class="sxs-lookup"><span data-stu-id="c6bdd-114">2</span></span>  <br/> |<span data-ttu-id="c6bdd-115">Se voltea verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="c6bdd-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="c6bdd-117">4</span><span class="sxs-lookup"><span data-stu-id="c6bdd-117">4</span></span>  <br/> |<span data-ttu-id="c6bdd-118">Se voltea en incrementos de 90 grados entre 0 y 270.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="c6bdd-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="c6bdd-120">8</span><span class="sxs-lookup"><span data-stu-id="c6bdd-120">8</span></span>  <br/> |<span data-ttu-id="c6bdd-121">No se voltea.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="c6bdd-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6bdd-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6bdd-123">Remarks</span></span>

<span data-ttu-id="c6bdd-124">El valor de la celda ShapePlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que esté conectada.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="c6bdd-125">Para establecer este comportamiento para *todas* las formas en la página de dibujo, utilice la celda PlaceFlip de la sección de diseño de página.</span><span class="sxs-lookup"><span data-stu-id="c6bdd-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="c6bdd-126">Para obtener una referencia a la celda ShapePlaceFlip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6bdd-127">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-127">Cell name:</span></span>  <br/> |<span data-ttu-id="c6bdd-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="c6bdd-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="c6bdd-129">Para obtener una referencia a la celda ShapePlaceFlip por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6bdd-130">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-130">Section index:</span></span>  <br/> |<span data-ttu-id="c6bdd-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c6bdd-132">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-132">Row index:</span></span>  <br/> |<span data-ttu-id="c6bdd-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c6bdd-134">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c6bdd-134">Cell index:</span></span>  <br/> |<span data-ttu-id="c6bdd-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="c6bdd-135">**visSLOPlaceFlip**</span></span> <br/> |
   

