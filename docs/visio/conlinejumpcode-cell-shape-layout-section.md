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
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284091"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="05f34-103">Celda ConLineJumpCode (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="05f34-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="05f34-104">Determina cuándo salta un conector.</span><span class="sxs-lookup"><span data-stu-id="05f34-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="05f34-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="05f34-105">**Value**</span></span>|<span data-ttu-id="05f34-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05f34-106">**Description**</span></span>|<span data-ttu-id="05f34-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="05f34-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05f34-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="05f34-108">0</span></span>  <br/> |<span data-ttu-id="05f34-109">Según especifica la página; para ver las especificaciones de la página, en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página** y, a continuación, haga clic en la pestaña **Diseño y enrutamiento**</span><span class="sxs-lookup"><span data-stu-id="05f34-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="05f34-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="05f34-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="05f34-111">1</span><span class="sxs-lookup"><span data-stu-id="05f34-111">1</span></span>  <br/> |<span data-ttu-id="05f34-112">Nunca</span><span class="sxs-lookup"><span data-stu-id="05f34-112">Never</span></span>  <br/> |<span data-ttu-id="05f34-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="05f34-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="05f34-114">segundo</span><span class="sxs-lookup"><span data-stu-id="05f34-114">2</span></span>  <br/> |<span data-ttu-id="05f34-115">Siempre</span><span class="sxs-lookup"><span data-stu-id="05f34-115">Always</span></span>  <br/> |<span data-ttu-id="05f34-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="05f34-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="05f34-117">3</span><span class="sxs-lookup"><span data-stu-id="05f34-117">3</span></span>  <br/> |<span data-ttu-id="05f34-118">Otro conector salta</span><span class="sxs-lookup"><span data-stu-id="05f34-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="05f34-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="05f34-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="05f34-120">4</span><span class="sxs-lookup"><span data-stu-id="05f34-120">4</span></span>  <br/> |<span data-ttu-id="05f34-121">Ningún conector salta</span><span class="sxs-lookup"><span data-stu-id="05f34-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="05f34-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="05f34-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05f34-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05f34-123">Remarks</span></span>

<span data-ttu-id="05f34-124">También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **diseño de formas** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haciendo clic en la pestaña **conector** .</span><span class="sxs-lookup"><span data-stu-id="05f34-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="05f34-125">Para obtener una referencia a la celda ConLineJumpCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="05f34-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05f34-126">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="05f34-126">Cell name:</span></span>  <br/> |<span data-ttu-id="05f34-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="05f34-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="05f34-128">Para obtener una referencia desde un programa a la celda ConLineJumpCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="05f34-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05f34-129">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="05f34-129">Section index:</span></span>  <br/> |<span data-ttu-id="05f34-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05f34-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="05f34-131">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="05f34-131">Row index:</span></span>  <br/> |<span data-ttu-id="05f34-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="05f34-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="05f34-133">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="05f34-133">Cell index:</span></span>  <br/> |<span data-ttu-id="05f34-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="05f34-134">**visSLOJumpCode**</span></span> <br/> |
   

