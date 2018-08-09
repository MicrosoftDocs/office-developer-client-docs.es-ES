---
title: Celda DynFeedback (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Cambia el tipo de efecto visual ofrecido a los usuarios cuando arrastran un conector. Al soltar el botón del mouse (ratón), la forma conector resultante no se ve afectada por esta configuración. Esta configuración no se aplica a conectores enrutables.
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822052"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="8e8db-105">Celda DynFeedback (sección Varios)</span><span class="sxs-lookup"><span data-stu-id="8e8db-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="8e8db-p102">Cambia el tipo de efecto visual ofrecido a los usuarios cuando arrastran un conector. Al soltar el botón del mouse (ratón), la forma conector resultante no se ve afectada por esta configuración. Esta configuración no se aplica a conectores enrutables.</span><span class="sxs-lookup"><span data-stu-id="8e8db-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="8e8db-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e8db-109">**Value**</span></span>|<span data-ttu-id="8e8db-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e8db-110">**Description**</span></span>|<span data-ttu-id="8e8db-111">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8e8db-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8e8db-112">0</span><span class="sxs-lookup"><span data-stu-id="8e8db-112">0</span></span>  <br/> | <span data-ttu-id="8e8db-113">Permanece recto (sin segmentos).</span><span class="sxs-lookup"><span data-stu-id="8e8db-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="8e8db-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="8e8db-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="8e8db-115">1</span><span class="sxs-lookup"><span data-stu-id="8e8db-115">1</span></span>  <br/> | <span data-ttu-id="8e8db-116">Al arrastrarlo, presenta tres segmentos.</span><span class="sxs-lookup"><span data-stu-id="8e8db-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="8e8db-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="8e8db-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="8e8db-118">2</span><span class="sxs-lookup"><span data-stu-id="8e8db-118">2</span></span>  <br/> | <span data-ttu-id="8e8db-119">Al arrastrarlo, presenta cinco segmentos.</span><span class="sxs-lookup"><span data-stu-id="8e8db-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="8e8db-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="8e8db-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e8db-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e8db-121">Remarks</span></span>

<span data-ttu-id="8e8db-122">Para obtener una referencia a la celda DynFeedback por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8e8db-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e8db-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8e8db-123">Cell name:</span></span>  <br/> | <span data-ttu-id="8e8db-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="8e8db-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="8e8db-125">Para obtener una referencia desde un programa a la celda DynFeedback por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e8db-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e8db-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8e8db-126">Section index:</span></span>  <br/> |<span data-ttu-id="8e8db-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e8db-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e8db-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8e8db-128">Row index:</span></span>  <br/> |<span data-ttu-id="8e8db-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="8e8db-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="8e8db-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8e8db-130">Cell index:</span></span>  <br/> |<span data-ttu-id="8e8db-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="8e8db-131">**visDynFeedback**</span></span> <br/> |
   

