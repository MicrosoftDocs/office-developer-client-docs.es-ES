---
title: Celda LockSelect (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Impide que una forma pueda seleccionarse.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822534"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="778ed-103">Celda LockSelect (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="778ed-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="778ed-104">Impide que una forma pueda seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="778ed-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="778ed-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="778ed-105">**Value**</span></span>|<span data-ttu-id="778ed-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="778ed-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="778ed-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="778ed-107">TRUE</span></span>  <br/> | <span data-ttu-id="778ed-108">La forma no puede seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="778ed-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="778ed-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="778ed-109">FALSE</span></span>  <br/> | <span data-ttu-id="778ed-110">La forma puede seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="778ed-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="778ed-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="778ed-111">Remarks</span></span>

<span data-ttu-id="778ed-112">Para que LockSelect surta efecto, la casilla de verificación **Formas** debe estar activada en el cuadro de diálogo **Proteger documento**.</span><span class="sxs-lookup"><span data-stu-id="778ed-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="778ed-113">Para obtener una referencia a la celda LockSelect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="778ed-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="778ed-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="778ed-114">Cell name:</span></span>  <br/> | <span data-ttu-id="778ed-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="778ed-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="778ed-116">Para obtener una referencia desde un programa a la celda LockSelect por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="778ed-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="778ed-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="778ed-117">Section index:</span></span>  <br/> |<span data-ttu-id="778ed-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="778ed-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="778ed-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="778ed-119">Row index:</span></span>  <br/> |<span data-ttu-id="778ed-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="778ed-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="778ed-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="778ed-121">Cell index:</span></span>  <br/> |<span data-ttu-id="778ed-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="778ed-122">**visLockSelect**</span></span> <br/> |
   

