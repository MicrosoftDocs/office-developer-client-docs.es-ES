---
title: Celda IsDropTarget (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Determina si el grupo permite agregar una forma soltándola en él.
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297231"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="5ed5b-103">Celda IsDropTarget (Sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="5ed5b-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="5ed5b-104">Determina si el grupo permite agregar una forma soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="5ed5b-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="5ed5b-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="5ed5b-105">**Value**</span></span>|<span data-ttu-id="5ed5b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ed5b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ed5b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ed5b-107">TRUE</span></span>  <br/> |<span data-ttu-id="5ed5b-108">Permite agregar una forma a un grupo soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="5ed5b-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="5ed5b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ed5b-109">FALSE</span></span>  <br/> |<span data-ttu-id="5ed5b-110">No permite soltar la forma en el grupo.</span><span class="sxs-lookup"><span data-stu-id="5ed5b-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ed5b-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ed5b-111">Remarks</span></span>

<span data-ttu-id="5ed5b-112">También puede ajustar este valor si selecciona el grupo, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, selecciona la casilla **Aceptar formas colocadas**.</span><span class="sxs-lookup"><span data-stu-id="5ed5b-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="5ed5b-p101">Para agregar una forma a un grupo colocándola en él, también debe habilitar un comportamiento de forma similar. Debe seleccionar la forma, hacer clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, activar la casilla **Agregar formas a un grupo al colocarlas**. Este valor se almacena en la celda IsDropSource en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="5ed5b-p101">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior. You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box. This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="5ed5b-116">Para obtener una referencia a la celda IsDropTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ed5b-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5ed5b-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="5ed5b-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="5ed5b-119">Para obtener una referencia desde un programa a la celda IsDropTarget por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ed5b-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-120">Section index:</span></span>  <br/> |<span data-ttu-id="5ed5b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ed5b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5ed5b-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-122">Row index:</span></span>  <br/> |<span data-ttu-id="5ed5b-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="5ed5b-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="5ed5b-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5ed5b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5ed5b-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="5ed5b-125">**visGroupIsDropTarget**</span></span> <br/> |
   

