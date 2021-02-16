---
title: Celda XRulerDensity (Sección &amp; de cuadrícula de regla)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica las subdivisiones horizontales de la regla en la página.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411473"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="acae2-103">Celda XRulerDensity (Sección &amp; de cuadrícula de regla)</span><span class="sxs-lookup"><span data-stu-id="acae2-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="acae2-104">Especifica las subdivisiones horizontales de la regla en la página.</span><span class="sxs-lookup"><span data-stu-id="acae2-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="acae2-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="acae2-105">**Value**</span></span>|<span data-ttu-id="acae2-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acae2-106">**Description**</span></span>|<span data-ttu-id="acae2-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="acae2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="acae2-108">0</span><span class="sxs-lookup"><span data-stu-id="acae2-108">0</span></span>  <br/> |<span data-ttu-id="acae2-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="acae2-109">Fixed</span></span>  <br/> |<span data-ttu-id="acae2-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="acae2-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="acae2-111">8 ( &amp; H8)</span><span class="sxs-lookup"><span data-stu-id="acae2-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="acae2-112">Grueso</span><span class="sxs-lookup"><span data-stu-id="acae2-112">Coarse</span></span>  <br/> |<span data-ttu-id="acae2-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="acae2-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="acae2-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="acae2-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="acae2-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="acae2-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="acae2-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="acae2-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="acae2-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="acae2-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="acae2-118">Bien</span><span class="sxs-lookup"><span data-stu-id="acae2-118">Fine</span></span>  <br/> |<span data-ttu-id="acae2-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="acae2-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acae2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acae2-120">Remarks</span></span>

<span data-ttu-id="acae2-121">Esta celda corresponde a la opción **Subdivisiones** horizontales del  cuadro de diálogo Cuadrícula de regla (en la ficha Ver, haga clic en **la flecha** Mostrar). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="acae2-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="acae2-122">Para obtener una referencia a la celda XRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="acae2-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acae2-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="acae2-123">Cell name:</span></span>  <br/> |<span data-ttu-id="acae2-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="acae2-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="acae2-125">Para obtener una referencia desde un programa a la celda XRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="acae2-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acae2-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="acae2-126">Section index:</span></span>  <br/> |<span data-ttu-id="acae2-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="acae2-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="acae2-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="acae2-128">Row index:</span></span>  <br/> |<span data-ttu-id="acae2-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="acae2-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="acae2-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="acae2-130">Cell index:</span></span>  <br/> |<span data-ttu-id="acae2-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="acae2-131">**visXRulerDensity**</span></span> <br/> |
   

