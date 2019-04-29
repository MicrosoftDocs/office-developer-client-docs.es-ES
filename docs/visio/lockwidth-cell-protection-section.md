---
title: Celda LockWidth (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439810"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="e2064-103">Celda LockWidth (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="e2064-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="e2064-104">Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="e2064-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="e2064-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e2064-105">**Value**</span></span>|<span data-ttu-id="e2064-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2064-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e2064-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e2064-107">TRUE</span></span>  <br/> | <span data-ttu-id="e2064-108">El ancho se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e2064-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="e2064-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e2064-109">FALSE</span></span>  <br/> | <span data-ttu-id="e2064-110">El ancho no se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e2064-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2064-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2064-111">Remarks</span></span>

<span data-ttu-id="e2064-112">Para obtener una referencia a la celda LockWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e2064-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2064-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e2064-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e2064-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="e2064-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="e2064-115">Para obtener una referencia desde un programa a la celda LockWidth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2064-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2064-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e2064-116">Section index:</span></span>  <br/> |<span data-ttu-id="e2064-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2064-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e2064-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e2064-118">Row index:</span></span>  <br/> |<span data-ttu-id="e2064-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e2064-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e2064-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e2064-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e2064-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="e2064-121">**visLockWidth**</span></span> <br/> |
   

