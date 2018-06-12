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
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822365"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="e0bf6-103">Celda IsDropTarget (Sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="e0bf6-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="e0bf6-104">Determina si el grupo permite agregar una forma soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="e0bf6-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="e0bf6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e0bf6-105">**Value**</span></span>|<span data-ttu-id="e0bf6-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0bf6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0bf6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e0bf6-107">TRUE</span></span>  <br/> |<span data-ttu-id="e0bf6-108">Permite agregar una forma a un grupo soltándola en él.</span><span class="sxs-lookup"><span data-stu-id="e0bf6-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="e0bf6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e0bf6-109">FALSE</span></span>  <br/> |<span data-ttu-id="e0bf6-110">No permite soltar la forma en el grupo.</span><span class="sxs-lookup"><span data-stu-id="e0bf6-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0bf6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0bf6-111">Remarks</span></span>

<span data-ttu-id="e0bf6-112">También puede establecer este valor, seleccione el grupo, hace clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccione la casilla de verificación **Aceptar formas colocadas** .</span><span class="sxs-lookup"><span data-stu-id="e0bf6-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="e0bf6-113">Para agregar una forma a un grupo soltándola en el grupo, también debe habilitar un comportamiento de forma similar.</span><span class="sxs-lookup"><span data-stu-id="e0bf6-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="e0bf6-114">Debe seleccionar la forma, haga clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccione la casilla de verificación **Agregar formas a grupos en el buzón** .</span><span class="sxs-lookup"><span data-stu-id="e0bf6-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="e0bf6-115">Este valor se almacena en la celda IsDropSource en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="e0bf6-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="e0bf6-116">Para obtener una referencia a la celda IsDropTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0bf6-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="e0bf6-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="e0bf6-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="e0bf6-119">Para obtener una referencia a la celda IsDropTarget por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0bf6-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-120">Section index:</span></span>  <br/> |<span data-ttu-id="e0bf6-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0bf6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e0bf6-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-122">Row index:</span></span>  <br/> |<span data-ttu-id="e0bf6-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="e0bf6-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="e0bf6-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e0bf6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="e0bf6-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="e0bf6-125">**visGroupIsDropTarget**</span></span> <br/> |
   

