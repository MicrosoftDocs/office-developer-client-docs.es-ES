---
title: Celda LockGroup (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Bloquea un grupo de modo que no pueda desagruparse.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341795"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="42694-103">Celda LockGroup (sección de protección)</span><span class="sxs-lookup"><span data-stu-id="42694-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="42694-104">Bloquea un grupo de modo que no pueda desagruparse.</span><span class="sxs-lookup"><span data-stu-id="42694-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="42694-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="42694-105">**Value**</span></span>|<span data-ttu-id="42694-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42694-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42694-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="42694-107">TRUE</span></span>  <br/> |<span data-ttu-id="42694-108">El grupo no puede desagruparse.</span><span class="sxs-lookup"><span data-stu-id="42694-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="42694-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="42694-109">FALSE</span></span>  <br/> |<span data-ttu-id="42694-110">El grupo puede desagruparse.</span><span class="sxs-lookup"><span data-stu-id="42694-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42694-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42694-111">Remarks</span></span>

<span data-ttu-id="42694-112">Al establecer el valor de LockGroupCell como TRUE también se evita la eliminación de las formas que son miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="42694-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="42694-113">Para obtener una referencia a la celda LockGroup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="42694-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42694-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="42694-114">Cell name:</span></span>  <br/> |<span data-ttu-id="42694-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="42694-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="42694-116">Para obtener una referencia desde un programa a la celda LockGroup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="42694-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42694-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="42694-117">Section index:</span></span>  <br/> |<span data-ttu-id="42694-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="42694-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="42694-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="42694-119">Row index:</span></span>  <br/> |<span data-ttu-id="42694-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="42694-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="42694-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="42694-121">Cell index:</span></span>  <br/> |<span data-ttu-id="42694-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="42694-122">**visLockGroup**</span></span> <br/> |
   

