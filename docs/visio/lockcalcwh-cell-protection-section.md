---
title: Celda LockCalcWH (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Bloquea un rectángulo de selección de una forma de modo que no se pueda volver a calcular cuando se modifique un vértice o se cambie un tipo de fila en la sección de geometría.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423044"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="623ef-103">Celda LockCalcWH (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="623ef-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="623ef-104">Bloquea un rectángulo de selección de una forma de modo que no se pueda volver a calcular cuando se modifique un vértice o se cambie un tipo de fila en la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="623ef-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="623ef-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="623ef-105">**Value**</span></span>|<span data-ttu-id="623ef-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="623ef-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="623ef-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="623ef-107">TRUE</span></span>  <br/> | <span data-ttu-id="623ef-108">El ancho y el alto no pueden volver a calcularse.</span><span class="sxs-lookup"><span data-stu-id="623ef-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="623ef-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="623ef-109">FALSE</span></span>  <br/> | <span data-ttu-id="623ef-110">El ancho y el alto pueden volver a calcularse.</span><span class="sxs-lookup"><span data-stu-id="623ef-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="623ef-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="623ef-111">Remarks</span></span>

<span data-ttu-id="623ef-112">Para obtener una referencia a la celda LockCalcWH por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="623ef-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="623ef-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="623ef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="623ef-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="623ef-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="623ef-115">Para obtener una referencia desde un programa a la celda LockCalcWH por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="623ef-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="623ef-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="623ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="623ef-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="623ef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="623ef-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="623ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="623ef-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="623ef-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="623ef-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="623ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="623ef-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="623ef-121">**visLockCalcWH**</span></span> <br/> |
   

