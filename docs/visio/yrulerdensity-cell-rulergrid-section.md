---
title: Celda YRulerDensity (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica las subdivisiones verticales de la regla en la página.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823599"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="ef602-103">Celda YRulerDensity (sección Regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="ef602-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ef602-104">Especifica las subdivisiones verticales de la regla en la página.</span><span class="sxs-lookup"><span data-stu-id="ef602-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="ef602-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ef602-105">**Value**</span></span>|<span data-ttu-id="ef602-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef602-106">**Description**</span></span>|<span data-ttu-id="ef602-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="ef602-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef602-108">0</span><span class="sxs-lookup"><span data-stu-id="ef602-108">0</span></span>  <br/> |<span data-ttu-id="ef602-109">Fija</span><span class="sxs-lookup"><span data-stu-id="ef602-109">Fixed</span></span>  <br/> |<span data-ttu-id="ef602-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="ef602-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="ef602-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="ef602-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="ef602-112">Gruesa</span><span class="sxs-lookup"><span data-stu-id="ef602-112">Coarse</span></span>  <br/> |<span data-ttu-id="ef602-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="ef602-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="ef602-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="ef602-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="ef602-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="ef602-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="ef602-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="ef602-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="ef602-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="ef602-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="ef602-118">Fina</span><span class="sxs-lookup"><span data-stu-id="ef602-118">Fine</span></span>  <br/> |<span data-ttu-id="ef602-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="ef602-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef602-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef602-120">Remarks</span></span>

<span data-ttu-id="ef602-121">Esta celda corresponde a la opción **subdivisiones** verticales en el **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="ef602-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ef602-122">Para obtener una referencia a la celda YRulerDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ef602-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef602-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ef602-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ef602-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="ef602-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="ef602-125">Para obtener una referencia desde un programa a la celda YRulerDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef602-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef602-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ef602-126">Section index:</span></span>  <br/> |<span data-ttu-id="ef602-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ef602-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ef602-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ef602-128">Row index:</span></span>  <br/> |<span data-ttu-id="ef602-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ef602-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ef602-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ef602-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ef602-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="ef602-131">**visYRulerDensity**</span></span> <br/> |
   

