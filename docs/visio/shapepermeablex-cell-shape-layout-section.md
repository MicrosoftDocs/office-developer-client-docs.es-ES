---
title: Celda ShapePermeableX (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Determina si un conector puede enrutar horizontalmente a través de una forma que puede colocarse.
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19823155"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="84f9e-103">Celda ShapePermeableX (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="84f9e-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="84f9e-104">Determina si un conector puede enrutar horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="84f9e-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="84f9e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="84f9e-105">**Value**</span></span>|<span data-ttu-id="84f9e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84f9e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84f9e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="84f9e-107">TRUE</span></span>  <br/> |<span data-ttu-id="84f9e-108">Se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="84f9e-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="84f9e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="84f9e-109">FALSE</span></span>  <br/> |<span data-ttu-id="84f9e-110">No se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="84f9e-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84f9e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84f9e-111">Remarks</span></span>

<span data-ttu-id="84f9e-112">También puede establecer el valor de esta celda en la ficha de **colocación** en el cuadro de diálogo **comportamiento** (con una forma seleccionada, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en la ficha **colocación** ).</span><span class="sxs-lookup"><span data-stu-id="84f9e-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="84f9e-113">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="84f9e-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="84f9e-114">Para obtener una referencia a la celda ShapePermeableX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="84f9e-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84f9e-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="84f9e-115">Cell name:</span></span>  <br/> |<span data-ttu-id="84f9e-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="84f9e-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="84f9e-117">Para obtener una referencia desde un programa a la celda ShapePermeableX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="84f9e-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84f9e-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="84f9e-118">Section index:</span></span>  <br/> |<span data-ttu-id="84f9e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84f9e-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="84f9e-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="84f9e-120">Row index:</span></span>  <br/> |<span data-ttu-id="84f9e-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="84f9e-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="84f9e-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="84f9e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="84f9e-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="84f9e-123">**visSLOPermX**</span></span> <br/> |
   

