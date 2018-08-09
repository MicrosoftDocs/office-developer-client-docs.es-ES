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
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822496"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="c2b18-103">Celda LockCalcWH (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="c2b18-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="c2b18-104">Bloquea un rectángulo de selección de una forma de modo que no se pueda volver a calcular cuando se modifique un vértice o se cambie un tipo de fila en la sección de geometría.</span><span class="sxs-lookup"><span data-stu-id="c2b18-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="c2b18-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2b18-105">**Value**</span></span>|<span data-ttu-id="c2b18-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2b18-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c2b18-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2b18-107">TRUE</span></span>  <br/> | <span data-ttu-id="c2b18-108">El ancho y el alto no pueden volver a calcularse.</span><span class="sxs-lookup"><span data-stu-id="c2b18-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="c2b18-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2b18-109">FALSE</span></span>  <br/> | <span data-ttu-id="c2b18-110">El ancho y el alto pueden volver a calcularse.</span><span class="sxs-lookup"><span data-stu-id="c2b18-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2b18-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2b18-111">Remarks</span></span>

<span data-ttu-id="c2b18-112">Para obtener una referencia a la celda LockCalcWH por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c2b18-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2b18-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c2b18-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c2b18-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="c2b18-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="c2b18-115">Para obtener una referencia desde un programa a la celda LockCalcWH por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2b18-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2b18-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c2b18-116">Section index:</span></span>  <br/> |<span data-ttu-id="c2b18-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2b18-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2b18-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c2b18-118">Row index:</span></span>  <br/> |<span data-ttu-id="c2b18-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c2b18-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c2b18-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c2b18-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c2b18-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="c2b18-121">**visLockCalcWH**</span></span> <br/> |
   

