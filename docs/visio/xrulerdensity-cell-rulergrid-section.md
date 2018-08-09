---
title: Celda XRulerDensity (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica las subdivisiones horizontales de la regla en la página.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823567"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="5267b-103">Celda XRulerDensity (sección Regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="5267b-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="5267b-104">Especifica las subdivisiones horizontales de la regla en la página.</span><span class="sxs-lookup"><span data-stu-id="5267b-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="5267b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5267b-105">**Value**</span></span>|<span data-ttu-id="5267b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5267b-106">**Description**</span></span>|<span data-ttu-id="5267b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="5267b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5267b-108">0</span><span class="sxs-lookup"><span data-stu-id="5267b-108">0</span></span>  <br/> |<span data-ttu-id="5267b-109">Fija</span><span class="sxs-lookup"><span data-stu-id="5267b-109">Fixed</span></span>  <br/> |<span data-ttu-id="5267b-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="5267b-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="5267b-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="5267b-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="5267b-112">Gruesa</span><span class="sxs-lookup"><span data-stu-id="5267b-112">Coarse</span></span>  <br/> |<span data-ttu-id="5267b-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="5267b-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="5267b-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="5267b-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="5267b-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="5267b-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="5267b-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="5267b-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="5267b-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="5267b-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="5267b-118">Fina</span><span class="sxs-lookup"><span data-stu-id="5267b-118">Fine</span></span>  <br/> |<span data-ttu-id="5267b-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="5267b-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5267b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5267b-120">Remarks</span></span>

<span data-ttu-id="5267b-121">Esta celda corresponde a la opción **subdivisiones** horizontales en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="5267b-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="5267b-122">Para obtener una referencia a la celda XRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5267b-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5267b-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5267b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="5267b-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="5267b-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="5267b-125">Para obtener una referencia desde un programa a la celda XRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5267b-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5267b-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5267b-126">Section index:</span></span>  <br/> |<span data-ttu-id="5267b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5267b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5267b-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5267b-128">Row index:</span></span>  <br/> |<span data-ttu-id="5267b-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="5267b-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="5267b-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5267b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="5267b-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="5267b-131">**visXRulerDensity**</span></span> <br/> |
   

