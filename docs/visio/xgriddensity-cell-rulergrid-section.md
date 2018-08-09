---
title: Celda XGridDensity (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica el tipo de cuadrícula horizontal que se va a utilizar.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823571"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="d3c12-103">Celda XGridDensity (sección Regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="d3c12-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="d3c12-104">Especifica el tipo de cuadrícula horizontal que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="d3c12-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="d3c12-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3c12-105">**Value**</span></span>|<span data-ttu-id="d3c12-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3c12-106">**Description**</span></span>|<span data-ttu-id="d3c12-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="d3c12-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d3c12-108">0</span><span class="sxs-lookup"><span data-stu-id="d3c12-108">0</span></span>  <br/> |<span data-ttu-id="d3c12-109">Fija</span><span class="sxs-lookup"><span data-stu-id="d3c12-109">Fixed</span></span>  <br/> |<span data-ttu-id="d3c12-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="d3c12-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="d3c12-111">2</span><span class="sxs-lookup"><span data-stu-id="d3c12-111">2</span></span>  <br/> |<span data-ttu-id="d3c12-112">Gruesa</span><span class="sxs-lookup"><span data-stu-id="d3c12-112">Coarse</span></span>  <br/> |<span data-ttu-id="d3c12-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="d3c12-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="d3c12-114">4</span><span class="sxs-lookup"><span data-stu-id="d3c12-114">4</span></span>  <br/> |<span data-ttu-id="d3c12-115">Normal (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="d3c12-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="d3c12-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="d3c12-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="d3c12-117">8</span><span class="sxs-lookup"><span data-stu-id="d3c12-117">8</span></span>  <br/> |<span data-ttu-id="d3c12-118">Fina</span><span class="sxs-lookup"><span data-stu-id="d3c12-118">Fine</span></span>  <br/> |<span data-ttu-id="d3c12-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="d3c12-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3c12-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3c12-120">Remarks</span></span>

<span data-ttu-id="d3c12-121">Esta celda corresponde a la horizontal **espaciado de la cuadrícula** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="d3c12-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="d3c12-122">Para obtener una referencia a la celda XGridDensity por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d3c12-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3c12-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d3c12-123">Cell name:</span></span>  <br/> |<span data-ttu-id="d3c12-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="d3c12-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="d3c12-125">Para obtener una referencia desde un programa a la celda XGridDensity por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3c12-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3c12-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d3c12-126">Section index:</span></span>  <br/> |<span data-ttu-id="d3c12-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3c12-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d3c12-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d3c12-128">Row index:</span></span>  <br/> |<span data-ttu-id="d3c12-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="d3c12-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="d3c12-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d3c12-130">Cell index:</span></span>  <br/> |<span data-ttu-id="d3c12-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="d3c12-131">**visXGridDensity**</span></span> <br/> |
   

