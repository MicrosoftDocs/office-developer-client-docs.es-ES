---
title: Celda LockBegin (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Bloquea el punto inicial (BeginX, BeginY) de una forma 1D para una ubicación específica.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407763"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="3156e-103">Celda LockBegin (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="3156e-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="3156e-104">Bloquea el punto inicial (BeginX, BeginY) de una forma 1D para una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="3156e-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="3156e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3156e-105">**Value**</span></span>|<span data-ttu-id="3156e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3156e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3156e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3156e-107">TRUE</span></span>  <br/> | <span data-ttu-id="3156e-108">El punto inicial se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3156e-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="3156e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3156e-109">FALSE</span></span>  <br/> | <span data-ttu-id="3156e-110">El punto inicial no se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3156e-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3156e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3156e-111">Remarks</span></span>

<span data-ttu-id="3156e-112">Para obtener una referencia a la celda LockBegin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3156e-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3156e-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3156e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3156e-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="3156e-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="3156e-115">Para obtener una referencia desde un programa a la celda LockBegin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3156e-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3156e-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3156e-116">Section index:</span></span>  <br/> |<span data-ttu-id="3156e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3156e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3156e-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3156e-118">Row index:</span></span>  <br/> |<span data-ttu-id="3156e-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3156e-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3156e-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3156e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3156e-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="3156e-121">**visLockBegin**</span></span> <br/> |
   

