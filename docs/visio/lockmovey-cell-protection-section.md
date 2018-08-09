---
title: Celda LockMoveY (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Bloquea la posición vertical de la forma de manera que ésta no se pueda desplazar verticalmente.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822513"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="22929-103">Celda LockMoveY (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="22929-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="22929-104">Bloquea la posición vertical de la forma de manera que ésta no se pueda desplazar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="22929-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="22929-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="22929-105">**Value**</span></span>|<span data-ttu-id="22929-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22929-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="22929-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="22929-107">TRUE</span></span>  <br/> | <span data-ttu-id="22929-108">La posición vertical se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="22929-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="22929-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="22929-109">FALSE</span></span>  <br/> | <span data-ttu-id="22929-110">La posición vertical no se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="22929-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22929-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22929-111">Remarks</span></span>

<span data-ttu-id="22929-112">Para obtener una referencia a la celda LockMoveY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="22929-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22929-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="22929-113">Cell name:</span></span>  <br/> | <span data-ttu-id="22929-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="22929-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="22929-115">Para obtener una referencia desde un programa a la celda LockMoveY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="22929-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22929-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="22929-116">Section index:</span></span>  <br/> |<span data-ttu-id="22929-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="22929-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="22929-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="22929-118">Row index:</span></span>  <br/> |<span data-ttu-id="22929-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="22929-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="22929-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="22929-120">Cell index:</span></span>  <br/> |<span data-ttu-id="22929-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="22929-121">**visLockMoveY**</span></span> <br/> |
   

