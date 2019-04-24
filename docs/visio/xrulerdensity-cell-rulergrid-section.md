---
title: Celda XRulerDensity (sección &amp; regla y cuadrícula)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331853"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="dd8ff-103">Celda XRulerDensity (sección &amp; regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="dd8ff-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="dd8ff-104">Especifica las subdivisiones horizontales de la regla en la página.</span><span class="sxs-lookup"><span data-stu-id="dd8ff-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="dd8ff-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-105">**Value**</span></span>|<span data-ttu-id="dd8ff-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-106">**Description**</span></span>|<span data-ttu-id="dd8ff-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd8ff-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="dd8ff-108">0</span></span>  <br/> |<span data-ttu-id="dd8ff-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="dd8ff-109">Fixed</span></span>  <br/> |<span data-ttu-id="dd8ff-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="dd8ff-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="dd8ff-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="dd8ff-112">Generales</span><span class="sxs-lookup"><span data-stu-id="dd8ff-112">Coarse</span></span>  <br/> |<span data-ttu-id="dd8ff-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="dd8ff-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="dd8ff-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="dd8ff-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="dd8ff-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="dd8ff-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="dd8ff-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="dd8ff-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="dd8ff-118">Minucioso</span><span class="sxs-lookup"><span data-stu-id="dd8ff-118">Fine</span></span>  <br/> |<span data-ttu-id="dd8ff-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd8ff-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd8ff-120">Remarks</span></span>

<span data-ttu-id="dd8ff-121">Esta celda corresponde a la opción **subdivisiones** horizontales del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="dd8ff-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="dd8ff-122">Para obtener una referencia a la celda XRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd8ff-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-123">Cell name:</span></span>  <br/> |<span data-ttu-id="dd8ff-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="dd8ff-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="dd8ff-125">Para obtener una referencia desde un programa a la celda XRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd8ff-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-126">Section index:</span></span>  <br/> |<span data-ttu-id="dd8ff-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd8ff-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-128">Row index:</span></span>  <br/> |<span data-ttu-id="dd8ff-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="dd8ff-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dd8ff-130">Cell index:</span></span>  <br/> |<span data-ttu-id="dd8ff-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="dd8ff-131">**visXRulerDensity**</span></span> <br/> |
   

