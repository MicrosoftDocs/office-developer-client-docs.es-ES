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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425543"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="0bc9c-103">Celda Alignment (Sección de tabulaciones)</span><span class="sxs-lookup"><span data-stu-id="0bc9c-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="0bc9c-104">Especifica la alineación de las tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0bc9c-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="0bc9c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-105">**Value**</span></span>|<span data-ttu-id="0bc9c-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-106">**Alignment**</span></span>|<span data-ttu-id="0bc9c-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0bc9c-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="0bc9c-108">0</span></span>  <br/> | <span data-ttu-id="0bc9c-109">Left</span><span class="sxs-lookup"><span data-stu-id="0bc9c-109">Left</span></span>  <br/> |<span data-ttu-id="0bc9c-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="0bc9c-111">1</span><span class="sxs-lookup"><span data-stu-id="0bc9c-111">1</span></span>  <br/> | <span data-ttu-id="0bc9c-112">Hacia el centro</span><span class="sxs-lookup"><span data-stu-id="0bc9c-112">Center</span></span>  <br/> |<span data-ttu-id="0bc9c-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="0bc9c-114">segundo</span><span class="sxs-lookup"><span data-stu-id="0bc9c-114">2</span></span>  <br/> | <span data-ttu-id="0bc9c-115">Derecha</span><span class="sxs-lookup"><span data-stu-id="0bc9c-115">Right</span></span>  <br/> |<span data-ttu-id="0bc9c-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="0bc9c-117">3</span><span class="sxs-lookup"><span data-stu-id="0bc9c-117">3</span></span>  <br/> | <span data-ttu-id="0bc9c-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="0bc9c-118">Decimal</span></span>  <br/> |<span data-ttu-id="0bc9c-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="0bc9c-120">4 </span><span class="sxs-lookup"><span data-stu-id="0bc9c-120">4</span></span>  <br/> | <span data-ttu-id="0bc9c-121">Coma</span><span class="sxs-lookup"><span data-stu-id="0bc9c-121">Comma</span></span>  <br/> |<span data-ttu-id="0bc9c-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bc9c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bc9c-123">Remarks</span></span>

<span data-ttu-id="0bc9c-124">Para obtener una referencia a la celda Alignment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0bc9c-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-125">Cell name:</span></span>  <br/> | <span data-ttu-id="0bc9c-126">Etiquetas.</span><span class="sxs-lookup"><span data-stu-id="0bc9c-126">Tabs.</span></span>  <span data-ttu-id="0bc9c-127">*ij* donde *i y j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="0bc9c-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="0bc9c-128">Para obtener una referencia a la celda Alignment por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0bc9c-129">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-129">Section index:</span></span>  <br/> |<span data-ttu-id="0bc9c-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="0bc9c-131">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-131">Row index:</span></span>  <br/> |<span data-ttu-id="0bc9c-132">**visRowTab +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0bc9c-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0bc9c-133">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0bc9c-133">Cell index:</span></span>  <br/> | <span data-ttu-id="0bc9c-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="0bc9c-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

