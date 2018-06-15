---
title: Celda LockVtxEdit (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Bloquea los vértices de una forma para que no se puedan editar.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822547"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="69b6e-103">Celda LockVtxEdit (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="69b6e-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="69b6e-104">Bloquea los vértices de una forma para que no se puedan editar.</span><span class="sxs-lookup"><span data-stu-id="69b6e-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="69b6e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69b6e-105">**Value**</span></span>|<span data-ttu-id="69b6e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69b6e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69b6e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="69b6e-107">TRUE</span></span>  <br/> |<span data-ttu-id="69b6e-108">Los vértices no se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="69b6e-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="69b6e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="69b6e-109">FALSE</span></span>  <br/> |<span data-ttu-id="69b6e-110">Los vértices se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="69b6e-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69b6e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69b6e-111">Remarks</span></span>

<span data-ttu-id="69b6e-112">Para obtener una referencia a la celda LockVtxEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="69b6e-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69b6e-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="69b6e-113">Cell name:</span></span>  <br/> |<span data-ttu-id="69b6e-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="69b6e-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="69b6e-115">Para obtener una referencia a la celda LockVtxEdit por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="69b6e-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69b6e-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="69b6e-116">Section index:</span></span>  <br/> |<span data-ttu-id="69b6e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69b6e-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="69b6e-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="69b6e-118">Row index:</span></span>  <br/> |<span data-ttu-id="69b6e-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="69b6e-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="69b6e-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="69b6e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="69b6e-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="69b6e-121">**visLockVtxEdit**</span></span> <br/> |
   

