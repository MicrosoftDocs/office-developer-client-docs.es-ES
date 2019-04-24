---
title: Celda XGridDensity (sección &amp; regla y cuadrícula)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328994"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="4a054-103">Celda XGridDensity (sección &amp; regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="4a054-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="4a054-104">Especifica el tipo de cuadrícula horizontal que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="4a054-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="4a054-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="4a054-105">**Value**</span></span>|<span data-ttu-id="4a054-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a054-106">**Description**</span></span>|<span data-ttu-id="4a054-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="4a054-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a054-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="4a054-108">0</span></span>  <br/> |<span data-ttu-id="4a054-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="4a054-109">Fixed</span></span>  <br/> |<span data-ttu-id="4a054-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="4a054-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="4a054-111">segundo</span><span class="sxs-lookup"><span data-stu-id="4a054-111">2</span></span>  <br/> |<span data-ttu-id="4a054-112">Generales</span><span class="sxs-lookup"><span data-stu-id="4a054-112">Coarse</span></span>  <br/> |<span data-ttu-id="4a054-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="4a054-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="4a054-114">4</span><span class="sxs-lookup"><span data-stu-id="4a054-114">4</span></span>  <br/> |<span data-ttu-id="4a054-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="4a054-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="4a054-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="4a054-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="4a054-117">8,5</span><span class="sxs-lookup"><span data-stu-id="4a054-117">8</span></span>  <br/> |<span data-ttu-id="4a054-118">Minucioso</span><span class="sxs-lookup"><span data-stu-id="4a054-118">Fine</span></span>  <br/> |<span data-ttu-id="4a054-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="4a054-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a054-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a054-120">Remarks</span></span>

<span data-ttu-id="4a054-121">Esta celda corresponde a la opción espaciado de la **cuadrícula** horizontal del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="4a054-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="4a054-122">Para obtener una referencia a la celda XGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4a054-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a054-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4a054-123">Cell name:</span></span>  <br/> |<span data-ttu-id="4a054-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="4a054-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="4a054-125">Para obtener una referencia desde un programa a la celda XGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a054-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a054-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4a054-126">Section index:</span></span>  <br/> |<span data-ttu-id="4a054-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4a054-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4a054-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4a054-128">Row index:</span></span>  <br/> |<span data-ttu-id="4a054-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="4a054-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="4a054-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4a054-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4a054-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="4a054-131">**visXGridDensity**</span></span> <br/> |
   

