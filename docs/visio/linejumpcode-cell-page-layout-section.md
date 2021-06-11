---
title: Celda LineJumpCode (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Determina los conectores a los que desea agregar saltos.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416254"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="e3eee-103">Celda LineJumpCode (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="e3eee-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="e3eee-104">Determina los conectores a los que desea agregar saltos.</span><span class="sxs-lookup"><span data-stu-id="e3eee-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="e3eee-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e3eee-105">**Value**</span></span>|<span data-ttu-id="e3eee-106">**Conectores a los que desea agregar saltos**</span><span class="sxs-lookup"><span data-stu-id="e3eee-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="e3eee-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="e3eee-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3eee-108">0</span><span class="sxs-lookup"><span data-stu-id="e3eee-108">0</span></span>  <br/> |<span data-ttu-id="e3eee-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3eee-109">None</span></span>  <br/> |<span data-ttu-id="e3eee-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="e3eee-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="e3eee-111">1</span><span class="sxs-lookup"><span data-stu-id="e3eee-111">1</span></span>  <br/> |<span data-ttu-id="e3eee-112">Líneas horizontales</span><span class="sxs-lookup"><span data-stu-id="e3eee-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="e3eee-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="e3eee-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="e3eee-114">2</span><span class="sxs-lookup"><span data-stu-id="e3eee-114">2</span></span>  <br/> |<span data-ttu-id="e3eee-115">Líneas verticales</span><span class="sxs-lookup"><span data-stu-id="e3eee-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="e3eee-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="e3eee-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="e3eee-117">3</span><span class="sxs-lookup"><span data-stu-id="e3eee-117">3</span></span>  <br/> |<span data-ttu-id="e3eee-118">Última línea enrutada</span><span class="sxs-lookup"><span data-stu-id="e3eee-118">Last routed line</span></span>  <br/> |<span data-ttu-id="e3eee-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="e3eee-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="e3eee-120">4 </span><span class="sxs-lookup"><span data-stu-id="e3eee-120">4</span></span>  <br/> |<span data-ttu-id="e3eee-121">Última línea mostrada (forma superior en *el orden z)*</span><span class="sxs-lookup"><span data-stu-id="e3eee-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="e3eee-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="e3eee-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="e3eee-123">5 </span><span class="sxs-lookup"><span data-stu-id="e3eee-123">5</span></span>  <br/> |<span data-ttu-id="e3eee-124">Primera línea mostrada (forma en la parte inferior del *orden z)*</span><span class="sxs-lookup"><span data-stu-id="e3eee-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="e3eee-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="e3eee-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3eee-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3eee-126">Remarks</span></span>

<span data-ttu-id="e3eee-127">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="e3eee-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="e3eee-128">Para obtener una referencia a la celda LineJumpCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e3eee-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3eee-129">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e3eee-129">Cell name:</span></span>  <br/> |<span data-ttu-id="e3eee-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="e3eee-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="e3eee-131">Para obtener una referencia desde un programa a la celda LineJumpCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e3eee-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3eee-132">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e3eee-132">Section index:</span></span>  <br/> |<span data-ttu-id="e3eee-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3eee-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e3eee-134">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e3eee-134">Row index:</span></span>  <br/> |<span data-ttu-id="e3eee-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e3eee-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="e3eee-136">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e3eee-136">Cell index:</span></span>  <br/> |<span data-ttu-id="e3eee-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="e3eee-137">**visPLOJumpCode**</span></span> <br/> |
   

