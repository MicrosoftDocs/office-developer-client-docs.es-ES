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
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823117"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="aad0e-103">Celda SelectMode (sección Propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="aad0e-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="aad0e-104">Determina cómo se selecciona una forma de grupo y sus miembros.</span><span class="sxs-lookup"><span data-stu-id="aad0e-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="aad0e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="aad0e-105">**Value**</span></span>|<span data-ttu-id="aad0e-106">**Modo de selección**</span><span class="sxs-lookup"><span data-stu-id="aad0e-106">**Selection mode**</span></span>|<span data-ttu-id="aad0e-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="aad0e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aad0e-108">0</span><span class="sxs-lookup"><span data-stu-id="aad0e-108">0</span></span>  <br/> |<span data-ttu-id="aad0e-109">Se selecciona sólo la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="aad0e-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="aad0e-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="aad0e-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="aad0e-111">1</span><span class="sxs-lookup"><span data-stu-id="aad0e-111">1</span></span>  <br/> |<span data-ttu-id="aad0e-112">Se selecciona primero la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="aad0e-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="aad0e-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="aad0e-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="aad0e-114">2</span><span class="sxs-lookup"><span data-stu-id="aad0e-114">2</span></span>  <br/> |<span data-ttu-id="aad0e-115">Se seleccionan primero los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="aad0e-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="aad0e-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="aad0e-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aad0e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aad0e-117">Remarks</span></span>

<span data-ttu-id="aad0e-118">También puede establecer este valor en el cuadro de diálogo **comportamiento** (con la forma de grupo, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en un modo en la lista de **selección** en **grupo Comportamiento de** ).</span><span class="sxs-lookup"><span data-stu-id="aad0e-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="aad0e-119">Para obtener una referencia a la celda SelectMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="aad0e-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aad0e-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="aad0e-120">Cell name:</span></span>  <br/> |<span data-ttu-id="aad0e-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="aad0e-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="aad0e-122">Para obtener una referencia desde un programa a la celda SelectMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="aad0e-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aad0e-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="aad0e-123">Section index:</span></span>  <br/> |<span data-ttu-id="aad0e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aad0e-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="aad0e-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="aad0e-125">Row index:</span></span>  <br/> |<span data-ttu-id="aad0e-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="aad0e-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="aad0e-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="aad0e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="aad0e-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="aad0e-128">**visGroupSelectMode**</span></span> <br/> |
   

