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
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421896"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="ddaa3-103">Celda IsDropSource (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="ddaa3-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ddaa3-104">Determina si se puede agregar una forma a un grupo soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="ddaa3-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="ddaa3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ddaa3-105">**Value**</span></span>|<span data-ttu-id="ddaa3-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddaa3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddaa3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ddaa3-107">TRUE</span></span>  <br/> |<span data-ttu-id="ddaa3-108">Se puede agregar una forma a un grupo soltándola e él.</span><span class="sxs-lookup"><span data-stu-id="ddaa3-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="ddaa3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ddaa3-109">FALSE</span></span>  <br/> |<span data-ttu-id="ddaa3-110">No se puede agregar una forma a un grupo.</span><span class="sxs-lookup"><span data-stu-id="ddaa3-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddaa3-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddaa3-111">Remarks</span></span>

<span data-ttu-id="ddaa3-112">También puede ajustar este valor si selecciona la forma, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, selecciona la casilla **Agregar formas a un grupo al colocarlas**.</span><span class="sxs-lookup"><span data-stu-id="ddaa3-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="ddaa3-p101">Además de habilitar este comportamiento para una forma, debe habilitar también un grupo donde se puedan soltar las formas. Para ello, seleccione el grupo, haga clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, active la casilla **Aceptar formas colocadas**. Este valor se almacena en la celda IsDropTarget, en la sección de propiedades del grupo.</span><span class="sxs-lookup"><span data-stu-id="ddaa3-p101">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it. To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box. This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="ddaa3-116">Para obtener una referencia a la celda IsDropSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddaa3-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-117">Cell name:</span></span>  <br/> |<span data-ttu-id="ddaa3-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="ddaa3-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="ddaa3-119">Para obtener una referencia desde un programa a la celda IsDropSource por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddaa3-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-120">Section index:</span></span>  <br/> |<span data-ttu-id="ddaa3-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddaa3-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ddaa3-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-122">Row index:</span></span>  <br/> |<span data-ttu-id="ddaa3-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ddaa3-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="ddaa3-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ddaa3-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ddaa3-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="ddaa3-125">**visDropSource**</span></span> <br/> |
   

