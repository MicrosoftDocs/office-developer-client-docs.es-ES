---
title: Celda LockMoveX (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Bloquea la posición horizontal de la forma de manera que ésta no se puede desplazar horizontalmente.
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822531"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="788ed-103">Celda LockMoveX (sección de protección)</span><span class="sxs-lookup"><span data-stu-id="788ed-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="788ed-104">Bloquea la posición horizontal de la forma de manera que ésta no se puede desplazar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="788ed-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="788ed-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="788ed-105">**Value**</span></span>|<span data-ttu-id="788ed-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="788ed-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="788ed-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="788ed-107">TRUE</span></span>  <br/> | <span data-ttu-id="788ed-108">La posición horizontal se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="788ed-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="788ed-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="788ed-109">FALSE</span></span>  <br/> | <span data-ttu-id="788ed-110">La posición horizontal no se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="788ed-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="788ed-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="788ed-111">Remarks</span></span>

<span data-ttu-id="788ed-112">Para obtener una referencia a la celda LockMoveX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="788ed-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="788ed-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="788ed-113">Cell name:</span></span>  <br/> | <span data-ttu-id="788ed-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="788ed-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="788ed-115">Para obtener una referencia a la celda LockMoveX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="788ed-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="788ed-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="788ed-116">Section index:</span></span>  <br/> |<span data-ttu-id="788ed-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="788ed-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="788ed-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="788ed-118">Row index:</span></span>  <br/> |<span data-ttu-id="788ed-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="788ed-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="788ed-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="788ed-120">Cell index:</span></span>  <br/> |<span data-ttu-id="788ed-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="788ed-121">**visLockMoveX**</span></span> <br/> |
   

