---
title: Celda YGridDensity (Sección &amp; de cuadrícula de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica el tipo de cuadrícula vertical que se va a utilizar.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429813"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="e0512-103">Celda YGridDensity (Sección &amp; de cuadrícula de regla)</span><span class="sxs-lookup"><span data-stu-id="e0512-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="e0512-104">Especifica el tipo de cuadrícula vertical que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="e0512-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="e0512-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e0512-105">**Value**</span></span>|<span data-ttu-id="e0512-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0512-106">**Description**</span></span>|<span data-ttu-id="e0512-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="e0512-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0512-108">0</span><span class="sxs-lookup"><span data-stu-id="e0512-108">0</span></span>  <br/> |<span data-ttu-id="e0512-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="e0512-109">Fixed</span></span>  <br/> |<span data-ttu-id="e0512-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="e0512-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="e0512-111">2 </span><span class="sxs-lookup"><span data-stu-id="e0512-111">2</span></span>  <br/> |<span data-ttu-id="e0512-112">Grueso</span><span class="sxs-lookup"><span data-stu-id="e0512-112">Coarse</span></span>  <br/> |<span data-ttu-id="e0512-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="e0512-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="e0512-114">4 </span><span class="sxs-lookup"><span data-stu-id="e0512-114">4</span></span>  <br/> |<span data-ttu-id="e0512-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="e0512-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="e0512-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="e0512-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="e0512-117">8 </span><span class="sxs-lookup"><span data-stu-id="e0512-117">8</span></span>  <br/> |<span data-ttu-id="e0512-118">Bien</span><span class="sxs-lookup"><span data-stu-id="e0512-118">Fine</span></span>  <br/> |<span data-ttu-id="e0512-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="e0512-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0512-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0512-120">Remarks</span></span>

<span data-ttu-id="e0512-121">Esta celda corresponde a la opción **&amp;** **de** espaciado vertical de  la cuadrícula en el cuadro de diálogo Cuadrícula de regla (en la ficha Ver, haga clic en **la flecha mostrar).**</span><span class="sxs-lookup"><span data-stu-id="e0512-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="e0512-122">Para obtener una referencia a la celda YGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e0512-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0512-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e0512-123">Cell name:</span></span>  <br/> |<span data-ttu-id="e0512-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="e0512-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="e0512-125">Para obtener una referencia desde un programa a la celda YGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0512-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0512-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e0512-126">Section index:</span></span>  <br/> |<span data-ttu-id="e0512-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0512-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e0512-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e0512-128">Row index:</span></span>  <br/> |<span data-ttu-id="e0512-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="e0512-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="e0512-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e0512-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e0512-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="e0512-131">**visYGridDensity**</span></span> <br/> |
   

