---
title: Celda LockEnd (Sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Bloquea el extremo (EndX, EndY) de una forma 1D para una ubicación específica.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425585"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="5a134-103">Celda LockEnd (Sección Protección)</span><span class="sxs-lookup"><span data-stu-id="5a134-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="5a134-104">Bloquea el extremo (EndX, EndY) de una forma 1D para una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="5a134-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="5a134-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5a134-105">**Value**</span></span>|<span data-ttu-id="5a134-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a134-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a134-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5a134-107">TRUE</span></span>  <br/> | <span data-ttu-id="5a134-108">El extremo se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5a134-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="5a134-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5a134-109">FALSE</span></span>  <br/> | <span data-ttu-id="5a134-110">El extremo no se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5a134-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a134-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a134-111">Remarks</span></span>

<span data-ttu-id="5a134-112">Para obtener una referencia a la celda LockEnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5a134-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a134-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5a134-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5a134-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="5a134-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="5a134-115">Para obtener una referencia desde un programa a la celda LockEnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5a134-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a134-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5a134-116">Section index:</span></span>  <br/> |<span data-ttu-id="5a134-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a134-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5a134-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5a134-118">Row index:</span></span>  <br/> |<span data-ttu-id="5a134-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5a134-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="5a134-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5a134-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5a134-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="5a134-121">**visLockEnd**</span></span> <br/> |
   

