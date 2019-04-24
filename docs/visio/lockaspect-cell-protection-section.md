---
title: Celda LockAspect (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359643"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="132b5-103">Celda LockAspect (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="132b5-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="132b5-104">Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.</span><span class="sxs-lookup"><span data-stu-id="132b5-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="132b5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="132b5-105">**Value**</span></span>|<span data-ttu-id="132b5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="132b5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="132b5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="132b5-107">TRUE</span></span>  <br/> | <span data-ttu-id="132b5-108">La relación de aspecto se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="132b5-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="132b5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="132b5-109">FALSE</span></span>  <br/> | <span data-ttu-id="132b5-110">La relación de aspecto no se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="132b5-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="132b5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="132b5-111">Remarks</span></span>

<span data-ttu-id="132b5-112">Para obtener una referencia a la celda LockAspect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**,utilice:</span><span class="sxs-lookup"><span data-stu-id="132b5-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="132b5-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="132b5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="132b5-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="132b5-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="132b5-115">Para obtener una referencia desde un programa a la celda LockAspect por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="132b5-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="132b5-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="132b5-116">Section index:</span></span>  <br/> |<span data-ttu-id="132b5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="132b5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="132b5-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="132b5-118">Row index:</span></span>  <br/> |<span data-ttu-id="132b5-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="132b5-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="132b5-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="132b5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="132b5-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="132b5-121">**visLockAspect**</span></span> <br/> |
   

