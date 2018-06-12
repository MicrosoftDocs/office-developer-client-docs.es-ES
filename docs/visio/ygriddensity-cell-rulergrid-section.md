---
title: Celda YGridDensity (regla &amp; sección de la cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica el tipo de cuadrícula vertical que se va a utilizar.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823601"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="719fb-103">Celda YGridDensity (regla &amp; sección de la cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="719fb-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="719fb-104">Especifica el tipo de cuadrícula vertical que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="719fb-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="719fb-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="719fb-105">**Value**</span></span>|<span data-ttu-id="719fb-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="719fb-106">**Description**</span></span>|<span data-ttu-id="719fb-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="719fb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="719fb-108">0</span><span class="sxs-lookup"><span data-stu-id="719fb-108">0</span></span>  <br/> |<span data-ttu-id="719fb-109">Fija</span><span class="sxs-lookup"><span data-stu-id="719fb-109">Fixed</span></span>  <br/> |<span data-ttu-id="719fb-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="719fb-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="719fb-111">2</span><span class="sxs-lookup"><span data-stu-id="719fb-111">2</span></span>  <br/> |<span data-ttu-id="719fb-112">Gruesa</span><span class="sxs-lookup"><span data-stu-id="719fb-112">Coarse</span></span>  <br/> |<span data-ttu-id="719fb-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="719fb-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="719fb-114">4</span><span class="sxs-lookup"><span data-stu-id="719fb-114">4</span></span>  <br/> |<span data-ttu-id="719fb-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="719fb-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="719fb-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="719fb-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="719fb-117">8</span><span class="sxs-lookup"><span data-stu-id="719fb-117">8</span></span>  <br/> |<span data-ttu-id="719fb-118">Fina</span><span class="sxs-lookup"><span data-stu-id="719fb-118">Fine</span></span>  <br/> |<span data-ttu-id="719fb-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="719fb-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="719fb-120">Notas</span><span class="sxs-lookup"><span data-stu-id="719fb-120">Remarks</span></span>

<span data-ttu-id="719fb-121">Esta celda corresponde a la vertical **espaciado de la cuadrícula** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="719fb-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="719fb-122">Para obtener una referencia a la celda YGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="719fb-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="719fb-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="719fb-123">Cell name:</span></span>  <br/> |<span data-ttu-id="719fb-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="719fb-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="719fb-125">Para obtener una referencia a la celda YGridDensity por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="719fb-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="719fb-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="719fb-126">Section index:</span></span>  <br/> |<span data-ttu-id="719fb-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="719fb-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="719fb-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="719fb-128">Row index:</span></span>  <br/> |<span data-ttu-id="719fb-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="719fb-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="719fb-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="719fb-130">Cell index:</span></span>  <br/> |<span data-ttu-id="719fb-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="719fb-131">**visYGridDensity**</span></span> <br/> |
   

