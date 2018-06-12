---
title: Celda ConLineJumpCode (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Determina cuándo salta un conector.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821843"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="f1c6b-103">Celda ConLineJumpCode (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="f1c6b-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f1c6b-104">Determina cuándo salta un conector.</span><span class="sxs-lookup"><span data-stu-id="f1c6b-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="f1c6b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-105">**Value**</span></span>|<span data-ttu-id="f1c6b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-106">**Description**</span></span>|<span data-ttu-id="f1c6b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1c6b-108">0</span><span class="sxs-lookup"><span data-stu-id="f1c6b-108">0</span></span>  <br/> |<span data-ttu-id="f1c6b-109">Tal y como se especifica en la página; en la ficha **Diseño** , haga clic en la flecha situada en el grupo **Configurar página** y, a continuación, haga clic en la ficha **Diseño y enrutamiento** para ver las especificaciones de página</span><span class="sxs-lookup"><span data-stu-id="f1c6b-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="f1c6b-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="f1c6b-111">1</span><span class="sxs-lookup"><span data-stu-id="f1c6b-111">1</span></span>  <br/> |<span data-ttu-id="f1c6b-112">Nunca</span><span class="sxs-lookup"><span data-stu-id="f1c6b-112">Never</span></span>  <br/> |<span data-ttu-id="f1c6b-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="f1c6b-114">2</span><span class="sxs-lookup"><span data-stu-id="f1c6b-114">2</span></span>  <br/> |<span data-ttu-id="f1c6b-115">Siempre</span><span class="sxs-lookup"><span data-stu-id="f1c6b-115">Always</span></span>  <br/> |<span data-ttu-id="f1c6b-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="f1c6b-117">3</span><span class="sxs-lookup"><span data-stu-id="f1c6b-117">3</span></span>  <br/> |<span data-ttu-id="f1c6b-118">Otro conector salta</span><span class="sxs-lookup"><span data-stu-id="f1c6b-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="f1c6b-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="f1c6b-120">4</span><span class="sxs-lookup"><span data-stu-id="f1c6b-120">4</span></span>  <br/> |<span data-ttu-id="f1c6b-121">Ningún conector salta</span><span class="sxs-lookup"><span data-stu-id="f1c6b-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="f1c6b-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1c6b-123">Notas</span><span class="sxs-lookup"><span data-stu-id="f1c6b-123">Remarks</span></span>

<span data-ttu-id="f1c6b-124">También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **Diseño de formas** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haga clic en la ficha **conector** .</span><span class="sxs-lookup"><span data-stu-id="f1c6b-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="f1c6b-125">Para obtener una referencia a la celda ConLineJumpCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1c6b-126">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-126">Cell name:</span></span>  <br/> |<span data-ttu-id="f1c6b-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="f1c6b-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="f1c6b-128">Para obtener una referencia a la celda ConLineJumpCode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1c6b-129">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-129">Section index:</span></span>  <br/> |<span data-ttu-id="f1c6b-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f1c6b-131">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-131">Row index:</span></span>  <br/> |<span data-ttu-id="f1c6b-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="f1c6b-133">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f1c6b-133">Cell index:</span></span>  <br/> |<span data-ttu-id="f1c6b-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="f1c6b-134">**visSLOJumpCode**</span></span> <br/> |
   

