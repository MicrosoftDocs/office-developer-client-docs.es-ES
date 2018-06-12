---
title: Celda LockFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Bloquea el formato de una forma para no se pueda cambiar.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822507"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="8b5d4-103">Celda LockFormat (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="8b5d4-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="8b5d4-104">Bloquea el formato de una forma para no se pueda cambiar.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="8b5d4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8b5d4-105">**Value**</span></span>|<span data-ttu-id="8b5d4-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b5d4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8b5d4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8b5d4-107">TRUE</span></span>  <br/> | <span data-ttu-id="8b5d4-108">El formato no puede cambiarse.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="8b5d4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8b5d4-109">FALSE</span></span>  <br/> | <span data-ttu-id="8b5d4-110">El formato puede cambiarse.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b5d4-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b5d4-111">Remarks</span></span>

<span data-ttu-id="8b5d4-112">Para obtener una referencia a la celda LockFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b5d4-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8b5d4-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="8b5d4-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="8b5d4-115">Para obtener una referencia a la celda LockFormat por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b5d4-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-116">Section index:</span></span>  <br/> |<span data-ttu-id="8b5d4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b5d4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8b5d4-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-118">Row index:</span></span>  <br/> |<span data-ttu-id="8b5d4-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8b5d4-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8b5d4-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8b5d4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8b5d4-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="8b5d4-121">**visLockFormat**</span></span> <br/> |
   

