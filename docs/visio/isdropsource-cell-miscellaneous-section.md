---
title: Celda IsDropSource (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Determina si se puede agregar una forma a un grupo soltándola en él.
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822355"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="887f0-103">Celda IsDropSource (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="887f0-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="887f0-104">Determina si se puede agregar una forma a un grupo soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="887f0-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="887f0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="887f0-105">**Value**</span></span>|<span data-ttu-id="887f0-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="887f0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="887f0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="887f0-107">TRUE</span></span>  <br/> |<span data-ttu-id="887f0-108">Se puede agregar una forma a un grupo soltándola e él.</span><span class="sxs-lookup"><span data-stu-id="887f0-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="887f0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="887f0-109">FALSE</span></span>  <br/> |<span data-ttu-id="887f0-110">No se puede agregar una forma a un grupo.</span><span class="sxs-lookup"><span data-stu-id="887f0-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="887f0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="887f0-111">Remarks</span></span>

<span data-ttu-id="887f0-112">También puede establecer este valor mediante la selección de la forma, haciendo clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, selecciona la casilla de verificación **Agregar formas a grupos en el buzón** .</span><span class="sxs-lookup"><span data-stu-id="887f0-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="887f0-113">Además de habilitar este comportamiento para una forma, también debe habilitar un grupo Aceptar formas que se arrastran en él.</span><span class="sxs-lookup"><span data-stu-id="887f0-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="887f0-114">Para ello, seleccione el grupo, haga clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccione la casilla de verificación **Aceptar formas colocadas** .</span><span class="sxs-lookup"><span data-stu-id="887f0-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="887f0-115">Este valor se almacena en la celda IsDropTarget, en la sección Propiedades del grupo.</span><span class="sxs-lookup"><span data-stu-id="887f0-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="887f0-116">Para obtener una referencia a la celda IsDropSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="887f0-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="887f0-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="887f0-117">Cell name:</span></span>  <br/> |<span data-ttu-id="887f0-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="887f0-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="887f0-119">Para obtener una referencia a la celda IsDropSource por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="887f0-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="887f0-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="887f0-120">Section index:</span></span>  <br/> |<span data-ttu-id="887f0-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="887f0-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="887f0-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="887f0-122">Row index:</span></span>  <br/> |<span data-ttu-id="887f0-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="887f0-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="887f0-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="887f0-124">Cell index:</span></span>  <br/> |<span data-ttu-id="887f0-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="887f0-125">**visDropSource**</span></span> <br/> |
   

