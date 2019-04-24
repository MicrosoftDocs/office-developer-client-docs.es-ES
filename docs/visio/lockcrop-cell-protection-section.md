---
title: Celda LockCrop (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Bloquea un objeto desde otro programa en lugar de recortarlo con la herramienta Recortar.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359629"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="eb6a2-103">Celda LockCrop (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="eb6a2-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="eb6a2-104">Bloquea un objeto desde otro programa en lugar de recortarlo con la herramienta **Recortar**.</span><span class="sxs-lookup"><span data-stu-id="eb6a2-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="eb6a2-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="eb6a2-105">**Value**</span></span>|<span data-ttu-id="eb6a2-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb6a2-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eb6a2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eb6a2-107">TRUE</span></span>  <br/> | <span data-ttu-id="eb6a2-108">La forma no se puede recortar.</span><span class="sxs-lookup"><span data-stu-id="eb6a2-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="eb6a2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eb6a2-109">FALSE</span></span>  <br/> | <span data-ttu-id="eb6a2-110">La forma se puede recortar.</span><span class="sxs-lookup"><span data-stu-id="eb6a2-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb6a2-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb6a2-111">Remarks</span></span>

<span data-ttu-id="eb6a2-112">Para obtener una referencia a la celda LockCrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb6a2-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-113">Cell name:</span></span>  <br/> | <span data-ttu-id="eb6a2-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="eb6a2-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="eb6a2-115">Para obtener una referencia desde un programa a la celda LockCrop por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb6a2-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-116">Section index:</span></span>  <br/> |<span data-ttu-id="eb6a2-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb6a2-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb6a2-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-118">Row index:</span></span>  <br/> |<span data-ttu-id="eb6a2-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="eb6a2-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="eb6a2-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="eb6a2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="eb6a2-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="eb6a2-121">**visLockCrop**</span></span> <br/> |
   

