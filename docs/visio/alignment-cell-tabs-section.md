---
title: Celda Alignment (Sección de tabulaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Especifica la alineación de las tabulaciones.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341541"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="e8dcd-103">Celda Alignment (Sección de tabulaciones)</span><span class="sxs-lookup"><span data-stu-id="e8dcd-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="e8dcd-104">Especifica la alineación de las tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="e8dcd-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="e8dcd-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-105">**Value**</span></span>|<span data-ttu-id="e8dcd-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-106">**Alignment**</span></span>|<span data-ttu-id="e8dcd-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e8dcd-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="e8dcd-108">0</span></span>  <br/> | <span data-ttu-id="e8dcd-109">Left</span><span class="sxs-lookup"><span data-stu-id="e8dcd-109">Left</span></span>  <br/> |<span data-ttu-id="e8dcd-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="e8dcd-111">1</span><span class="sxs-lookup"><span data-stu-id="e8dcd-111">1</span></span>  <br/> | <span data-ttu-id="e8dcd-112">Hacia el centro</span><span class="sxs-lookup"><span data-stu-id="e8dcd-112">Center</span></span>  <br/> |<span data-ttu-id="e8dcd-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="e8dcd-114">segundo</span><span class="sxs-lookup"><span data-stu-id="e8dcd-114">2</span></span>  <br/> | <span data-ttu-id="e8dcd-115">Derecha</span><span class="sxs-lookup"><span data-stu-id="e8dcd-115">Right</span></span>  <br/> |<span data-ttu-id="e8dcd-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="e8dcd-117">3</span><span class="sxs-lookup"><span data-stu-id="e8dcd-117">3</span></span>  <br/> | <span data-ttu-id="e8dcd-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="e8dcd-118">Decimal</span></span>  <br/> |<span data-ttu-id="e8dcd-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="e8dcd-120">4</span><span class="sxs-lookup"><span data-stu-id="e8dcd-120">4</span></span>  <br/> | <span data-ttu-id="e8dcd-121">Coma</span><span class="sxs-lookup"><span data-stu-id="e8dcd-121">Comma</span></span>  <br/> |<span data-ttu-id="e8dcd-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8dcd-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8dcd-123">Remarks</span></span>

<span data-ttu-id="e8dcd-124">Para obtener una referencia a la celda Alignment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dcd-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-125">Cell name:</span></span>  <br/> | <span data-ttu-id="e8dcd-126">Etiquetas.</span><span class="sxs-lookup"><span data-stu-id="e8dcd-126">Tabs.</span></span>  <span data-ttu-id="e8dcd-127">*ij* donde *i y j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="e8dcd-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="e8dcd-128">Para obtener una referencia a la celda Alignment por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dcd-129">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-129">Section index:</span></span>  <br/> |<span data-ttu-id="e8dcd-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="e8dcd-131">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-131">Row index:</span></span>  <br/> |<span data-ttu-id="e8dcd-132">**visRowTab +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e8dcd-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e8dcd-133">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e8dcd-133">Cell index:</span></span>  <br/> | <span data-ttu-id="e8dcd-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="e8dcd-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

