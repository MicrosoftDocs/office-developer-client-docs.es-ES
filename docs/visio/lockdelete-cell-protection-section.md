---
title: Celda LockDelete (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Bloquea la forma de manera que ésta no pueda ser eliminada.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423142"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="b2153-103">Celda LockDelete (sección de protección)</span><span class="sxs-lookup"><span data-stu-id="b2153-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="b2153-104">Bloquea la forma de manera que ésta no pueda ser eliminada.</span><span class="sxs-lookup"><span data-stu-id="b2153-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="b2153-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b2153-105">**Value**</span></span>|<span data-ttu-id="b2153-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b2153-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b2153-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2153-107">TRUE</span></span>  <br/> | <span data-ttu-id="b2153-108">La forma no se puede eliminar</span><span class="sxs-lookup"><span data-stu-id="b2153-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="b2153-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2153-109">FALSE</span></span>  <br/> | <span data-ttu-id="b2153-110">La forma puede ser eliminada.</span><span class="sxs-lookup"><span data-stu-id="b2153-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2153-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2153-111">Remarks</span></span>

<span data-ttu-id="b2153-112">Para obtener una referencia a la celda LockDelete por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** utilice:</span><span class="sxs-lookup"><span data-stu-id="b2153-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2153-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b2153-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b2153-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="b2153-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="b2153-115">Para obtener una referencia desde un programa a la celda LockDelete por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2153-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2153-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b2153-116">Section index:</span></span>  <br/> |<span data-ttu-id="b2153-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2153-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2153-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b2153-118">Row index:</span></span>  <br/> |<span data-ttu-id="b2153-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b2153-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b2153-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b2153-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b2153-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="b2153-121">**visLockDelete**</span></span> <br/> |
   

