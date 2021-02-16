---
title: Celda YRulerDensity (Sección &amp; de cuadrícula de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica las subdivisiones verticales de la regla en la página.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406804"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="64e05-103">Celda YRulerDensity (Sección &amp; de cuadrícula de regla)</span><span class="sxs-lookup"><span data-stu-id="64e05-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="64e05-104">Especifica las subdivisiones verticales de la regla en la página.</span><span class="sxs-lookup"><span data-stu-id="64e05-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="64e05-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="64e05-105">**Value**</span></span>|<span data-ttu-id="64e05-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64e05-106">**Description**</span></span>|<span data-ttu-id="64e05-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="64e05-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64e05-108">0</span><span class="sxs-lookup"><span data-stu-id="64e05-108">0</span></span>  <br/> |<span data-ttu-id="64e05-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="64e05-109">Fixed</span></span>  <br/> |<span data-ttu-id="64e05-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="64e05-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="64e05-111">8 ( &amp; H8)</span><span class="sxs-lookup"><span data-stu-id="64e05-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="64e05-112">Grueso</span><span class="sxs-lookup"><span data-stu-id="64e05-112">Coarse</span></span>  <br/> |<span data-ttu-id="64e05-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="64e05-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="64e05-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="64e05-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="64e05-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="64e05-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="64e05-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="64e05-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="64e05-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="64e05-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="64e05-118">Bien</span><span class="sxs-lookup"><span data-stu-id="64e05-118">Fine</span></span>  <br/> |<span data-ttu-id="64e05-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="64e05-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64e05-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64e05-120">Remarks</span></span>

<span data-ttu-id="64e05-121">Esta celda corresponde a la opción **Subdivisiones** verticales del  cuadro de diálogo Cuadrícula de regla (en la ficha Ver, haga clic en **la flecha** Mostrar). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="64e05-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="64e05-122">Para obtener una referencia a la celda YRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="64e05-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64e05-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="64e05-123">Cell name:</span></span>  <br/> |<span data-ttu-id="64e05-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="64e05-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="64e05-125">Para obtener una referencia desde un programa a la celda YRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="64e05-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64e05-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="64e05-126">Section index:</span></span>  <br/> |<span data-ttu-id="64e05-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="64e05-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="64e05-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="64e05-128">Row index:</span></span>  <br/> |<span data-ttu-id="64e05-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="64e05-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="64e05-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="64e05-130">Cell index:</span></span>  <br/> |<span data-ttu-id="64e05-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="64e05-131">**visYRulerDensity**</span></span> <br/> |
   

