---
title: Celda ConFixedCode (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Determina cuándo un conector vuelve a enrutarse.
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404186"
---
# <a name="confixedcode-cell-shape-layout-section"></a><span data-ttu-id="b9edb-103">Celda ConFixedCode (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="b9edb-103">ConFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="b9edb-104">Determina cuándo un conector vuelve a enrutarse.</span><span class="sxs-lookup"><span data-stu-id="b9edb-104">Determines when a connector reroutes.</span></span>
  
|<span data-ttu-id="b9edb-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b9edb-105">**Value**</span></span>|<span data-ttu-id="b9edb-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9edb-106">**Description**</span></span>|<span data-ttu-id="b9edb-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="b9edb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9edb-108">0</span><span class="sxs-lookup"><span data-stu-id="b9edb-108">0</span></span>  <br/> |<span data-ttu-id="b9edb-109">Vuelve a enrutarse libremente.</span><span class="sxs-lookup"><span data-stu-id="b9edb-109">Reroute freely</span></span>  <br/> |<span data-ttu-id="b9edb-110">**visSLOConFixedRerouteFreely**</span><span class="sxs-lookup"><span data-stu-id="b9edb-110">**visSLOConFixedRerouteFreely**</span></span> <br/> |
|<span data-ttu-id="b9edb-111">1 </span><span class="sxs-lookup"><span data-stu-id="b9edb-111">1</span></span>  <br/> |<span data-ttu-id="b9edb-112">Vuelve a enrutarse según sea necesario (nuevo enrutamiento manual).</span><span class="sxs-lookup"><span data-stu-id="b9edb-112">Reroute as needed (manual reroute)</span></span>  <br/> |<span data-ttu-id="b9edb-113">**visSLOConFixedRerouteAsNeeded**</span><span class="sxs-lookup"><span data-stu-id="b9edb-113">**visSLOConFixedRerouteAsNeeded**</span></span> <br/> |
|<span data-ttu-id="b9edb-114">2 </span><span class="sxs-lookup"><span data-stu-id="b9edb-114">2</span></span>  <br/> |<span data-ttu-id="b9edb-115">No vuelve a enrutarse nunca.</span><span class="sxs-lookup"><span data-stu-id="b9edb-115">Never reroute</span></span>  <br/> |<span data-ttu-id="b9edb-116">**visSLOConFixedRerouteNever**</span><span class="sxs-lookup"><span data-stu-id="b9edb-116">**visSLOConFixedRerouteNever**</span></span> <br/> |
|<span data-ttu-id="b9edb-117">3 </span><span class="sxs-lookup"><span data-stu-id="b9edb-117">3</span></span>  <br/> |<span data-ttu-id="b9edb-118">Vuelve a enrutarse al cruzar.</span><span class="sxs-lookup"><span data-stu-id="b9edb-118">Reroute on crossover</span></span>  <br/> |<span data-ttu-id="b9edb-119">**visSLOConFixedRerouteOnCrossover**</span><span class="sxs-lookup"><span data-stu-id="b9edb-119">**visSLOConFixedRerouteOnCrossover**</span></span> <br/> |
|<span data-ttu-id="b9edb-120">4 </span><span class="sxs-lookup"><span data-stu-id="b9edb-120">4</span></span>  <br/> |<span data-ttu-id="b9edb-121">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="b9edb-121">For internal use only</span></span>  <br/> |<span data-ttu-id="b9edb-122">**visSLOConFixedByAlgFrom**</span><span class="sxs-lookup"><span data-stu-id="b9edb-122">**visSLOConFixedByAlgFrom**</span></span> <br/> |
|<span data-ttu-id="b9edb-123">5 </span><span class="sxs-lookup"><span data-stu-id="b9edb-123">5</span></span>  <br/> |<span data-ttu-id="b9edb-124">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="b9edb-124">For internal use only</span></span>  <br/> |<span data-ttu-id="b9edb-125">**visSLOConFixedByAlgTo**</span><span class="sxs-lookup"><span data-stu-id="b9edb-125">**visSLOConFixedByAlgTo**</span></span> <br/> |
|<span data-ttu-id="b9edb-126">6 </span><span class="sxs-lookup"><span data-stu-id="b9edb-126">6</span></span>  <br/> |<span data-ttu-id="b9edb-127">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="b9edb-127">For internal use only</span></span>  <br/> |<span data-ttu-id="b9edb-128">**visSLOConFixedByAlgFromTo**</span><span class="sxs-lookup"><span data-stu-id="b9edb-128">**visSLOConFixedByAlgFromTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9edb-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9edb-129">Remarks</span></span>

<span data-ttu-id="b9edb-130">También puede establecer el valor de esta celda seleccionando un  conector dinámico, [](run-in-developer-mode-display-the-developer-tab.md) haciendo clic en Comportamiento en el grupo Diseño de formas de la ficha Programador y, a continuación, haciendo clic en la **pestaña** Conector. </span><span class="sxs-lookup"><span data-stu-id="b9edb-130">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="b9edb-131">Para obtener una referencia a la celda ConFixedCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b9edb-131">To get a reference to the ConFixedCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9edb-132">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b9edb-132">Cell name:</span></span>  <br/> |<span data-ttu-id="b9edb-133">ConFixedCode</span><span class="sxs-lookup"><span data-stu-id="b9edb-133">ConFixedCode</span></span>  <br/> |
   
<span data-ttu-id="b9edb-134">Para obtener una referencia desde un programa a la celda ConFixedCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b9edb-134">To get a reference to the ConFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9edb-135">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b9edb-135">Section index:</span></span>  <br/> |<span data-ttu-id="b9edb-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9edb-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b9edb-137">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b9edb-137">Row index:</span></span>  <br/> |<span data-ttu-id="b9edb-138">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="b9edb-138">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="b9edb-139">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b9edb-139">Cell index:</span></span>  <br/> |<span data-ttu-id="b9edb-140">**visSLOConFixedCode**</span><span class="sxs-lookup"><span data-stu-id="b9edb-140">**visSLOConFixedCode**</span></span> <br/> |
   

