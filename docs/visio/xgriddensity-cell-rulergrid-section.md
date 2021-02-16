---
title: Celda XGridDensity (Sección &amp; de cuadrícula de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica el tipo de cuadrícula horizontal que se va a utilizar.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436044"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="df811-103">Celda XGridDensity (Sección &amp; de cuadrícula de regla)</span><span class="sxs-lookup"><span data-stu-id="df811-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="df811-104">Especifica el tipo de cuadrícula horizontal que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="df811-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="df811-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="df811-105">**Value**</span></span>|<span data-ttu-id="df811-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df811-106">**Description**</span></span>|<span data-ttu-id="df811-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="df811-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="df811-108">0</span><span class="sxs-lookup"><span data-stu-id="df811-108">0</span></span>  <br/> |<span data-ttu-id="df811-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="df811-109">Fixed</span></span>  <br/> |<span data-ttu-id="df811-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="df811-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="df811-111">2 </span><span class="sxs-lookup"><span data-stu-id="df811-111">2</span></span>  <br/> |<span data-ttu-id="df811-112">Grueso</span><span class="sxs-lookup"><span data-stu-id="df811-112">Coarse</span></span>  <br/> |<span data-ttu-id="df811-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="df811-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="df811-114">4 </span><span class="sxs-lookup"><span data-stu-id="df811-114">4</span></span>  <br/> |<span data-ttu-id="df811-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="df811-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="df811-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="df811-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="df811-117">8 </span><span class="sxs-lookup"><span data-stu-id="df811-117">8</span></span>  <br/> |<span data-ttu-id="df811-118">Bien</span><span class="sxs-lookup"><span data-stu-id="df811-118">Fine</span></span>  <br/> |<span data-ttu-id="df811-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="df811-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df811-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df811-120">Remarks</span></span>

<span data-ttu-id="df811-121">Esta celda corresponde a la opción **&amp;** **espaciado** horizontal de la  cuadrícula en el cuadro de diálogo Cuadrícula de regla (en la ficha Ver, haga clic en **la flecha mostrar).**</span><span class="sxs-lookup"><span data-stu-id="df811-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="df811-122">Para obtener una referencia a la celda XGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="df811-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df811-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="df811-123">Cell name:</span></span>  <br/> |<span data-ttu-id="df811-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="df811-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="df811-125">Para obtener una referencia desde un programa a la celda XGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="df811-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df811-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="df811-126">Section index:</span></span>  <br/> |<span data-ttu-id="df811-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df811-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="df811-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="df811-128">Row index:</span></span>  <br/> |<span data-ttu-id="df811-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="df811-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="df811-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="df811-130">Cell index:</span></span>  <br/> |<span data-ttu-id="df811-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="df811-131">**visXGridDensity**</span></span> <br/> |
   

