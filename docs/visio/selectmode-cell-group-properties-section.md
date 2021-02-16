---
title: Celda SelectMode (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Determina cómo se selecciona una forma de grupo y sus miembros.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435365"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="e32b5-103">Celda SelectMode (sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="e32b5-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="e32b5-104">Determina cómo se selecciona una forma de grupo y sus miembros.</span><span class="sxs-lookup"><span data-stu-id="e32b5-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="e32b5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e32b5-105">**Value**</span></span>|<span data-ttu-id="e32b5-106">**Modo de selección**</span><span class="sxs-lookup"><span data-stu-id="e32b5-106">**Selection mode**</span></span>|<span data-ttu-id="e32b5-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="e32b5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e32b5-108">0</span><span class="sxs-lookup"><span data-stu-id="e32b5-108">0</span></span>  <br/> |<span data-ttu-id="e32b5-109">Se selecciona sólo la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="e32b5-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="e32b5-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="e32b5-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="e32b5-111">1 </span><span class="sxs-lookup"><span data-stu-id="e32b5-111">1</span></span>  <br/> |<span data-ttu-id="e32b5-112">Se selecciona primero la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="e32b5-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="e32b5-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="e32b5-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="e32b5-114">2 </span><span class="sxs-lookup"><span data-stu-id="e32b5-114">2</span></span>  <br/> |<span data-ttu-id="e32b5-115">Se seleccionan primero los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="e32b5-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="e32b5-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="e32b5-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e32b5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e32b5-117">Remarks</span></span>

<span data-ttu-id="e32b5-118">También puede establecer este  valor en el cuadro de diálogo Comportamiento (con  la forma de grupo seleccionada, en la  ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en un modo de la lista Selección en Comportamiento de **grupo).** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="e32b5-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="e32b5-119">Para obtener una referencia a la celda SelectMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e32b5-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e32b5-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e32b5-120">Cell name:</span></span>  <br/> |<span data-ttu-id="e32b5-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="e32b5-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="e32b5-122">Para obtener una referencia desde un programa a la celda SelectMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e32b5-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e32b5-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e32b5-123">Section index:</span></span>  <br/> |<span data-ttu-id="e32b5-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e32b5-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e32b5-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e32b5-125">Row index:</span></span>  <br/> |<span data-ttu-id="e32b5-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="e32b5-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="e32b5-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e32b5-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e32b5-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="e32b5-128">**visGroupSelectMode**</span></span> <br/> |
   

