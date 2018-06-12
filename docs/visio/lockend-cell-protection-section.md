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
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822508"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="f565e-103">Celda LockEnd (Sección Protección)</span><span class="sxs-lookup"><span data-stu-id="f565e-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="f565e-104">Bloquea el extremo (EndX, EndY) de una forma 1D para una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="f565e-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="f565e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f565e-105">**Value**</span></span>|<span data-ttu-id="f565e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f565e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f565e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f565e-107">TRUE</span></span>  <br/> | <span data-ttu-id="f565e-108">El extremo se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f565e-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="f565e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f565e-109">FALSE</span></span>  <br/> | <span data-ttu-id="f565e-110">El extremo no se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f565e-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f565e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f565e-111">Remarks</span></span>

<span data-ttu-id="f565e-112">Para obtener una referencia a la celda LockEnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="f565e-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f565e-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f565e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f565e-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="f565e-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="f565e-115">Para obtener una referencia a la celda LockEnd por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f565e-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f565e-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f565e-116">Section index:</span></span>  <br/> |<span data-ttu-id="f565e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f565e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f565e-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f565e-118">Row index:</span></span>  <br/> |<span data-ttu-id="f565e-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f565e-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f565e-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f565e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f565e-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="f565e-121">**visLockEnd**</span></span> <br/> |
   

