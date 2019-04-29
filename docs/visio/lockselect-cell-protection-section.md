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
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409758"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="e9b2f-103">Celda LockSelect (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="e9b2f-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="e9b2f-104">Impide que una forma pueda seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="e9b2f-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="e9b2f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e9b2f-105">**Value**</span></span>|<span data-ttu-id="e9b2f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9b2f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e9b2f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e9b2f-107">TRUE</span></span>  <br/> | <span data-ttu-id="e9b2f-108">La forma no puede seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="e9b2f-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="e9b2f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e9b2f-109">FALSE</span></span>  <br/> | <span data-ttu-id="e9b2f-110">La forma puede seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="e9b2f-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9b2f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b2f-111">Remarks</span></span>

<span data-ttu-id="e9b2f-112">Para que LockSelect surta efecto, la casilla de verificación **Formas** debe estar activada en el cuadro de diálogo **Proteger documento**.</span><span class="sxs-lookup"><span data-stu-id="e9b2f-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="e9b2f-113">Para obtener una referencia a la celda LockSelect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9b2f-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-114">Cell name:</span></span>  <br/> | <span data-ttu-id="e9b2f-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="e9b2f-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="e9b2f-116">Para obtener una referencia desde un programa a la celda LockSelect por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9b2f-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-117">Section index:</span></span>  <br/> |<span data-ttu-id="e9b2f-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9b2f-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9b2f-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-119">Row index:</span></span>  <br/> |<span data-ttu-id="e9b2f-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e9b2f-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e9b2f-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e9b2f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e9b2f-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="e9b2f-122">**visLockSelect**</span></span> <br/> |
   

