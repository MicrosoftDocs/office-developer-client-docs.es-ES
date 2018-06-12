---
title: Celda LockHeight (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822514"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="3b4a0-103">Celda LockHeight (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="3b4a0-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="3b4a0-104">Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="3b4a0-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="3b4a0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3b4a0-105">**Value**</span></span>|<span data-ttu-id="3b4a0-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b4a0-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3b4a0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b4a0-107">TRUE</span></span>  <br/> | <span data-ttu-id="3b4a0-108">El alto se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3b4a0-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="3b4a0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b4a0-109">FALSE</span></span>  <br/> | <span data-ttu-id="3b4a0-110">El alto no se encuentra bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3b4a0-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b4a0-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b4a0-111">Remarks</span></span>

<span data-ttu-id="3b4a0-112">Para obtener una referencia a la celda LockHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b4a0-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3b4a0-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="3b4a0-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="3b4a0-115">Para obtener una referencia a la celda LockHeight por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b4a0-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-116">Section index:</span></span>  <br/> |<span data-ttu-id="3b4a0-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b4a0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b4a0-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-118">Row index:</span></span>  <br/> |<span data-ttu-id="3b4a0-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3b4a0-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3b4a0-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3b4a0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3b4a0-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="3b4a0-121">**visLockHeight**</span></span> <br/> |
   

