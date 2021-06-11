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
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409478"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="25c73-103">Celda ShapePermeableX (Sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="25c73-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="25c73-104">Determina si un conector puede enrutar horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="25c73-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="25c73-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="25c73-105">**Value**</span></span>|<span data-ttu-id="25c73-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25c73-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25c73-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="25c73-107">TRUE</span></span>  <br/> |<span data-ttu-id="25c73-108">Se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="25c73-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="25c73-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="25c73-109">FALSE</span></span>  <br/> |<span data-ttu-id="25c73-110">No se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.</span><span class="sxs-lookup"><span data-stu-id="25c73-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c73-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25c73-111">Remarks</span></span>

<span data-ttu-id="25c73-112">También puede establecer el valor de  esta celda en la ficha Ubicación del [](run-in-developer-mode-display-the-developer-tab.md) cuadro de diálogo Comportamiento (con una forma seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la pestaña Ubicación).   </span><span class="sxs-lookup"><span data-stu-id="25c73-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="25c73-113">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="25c73-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="25c73-114">Para obtener una referencia a la celda ShapePermeableX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="25c73-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c73-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="25c73-115">Cell name:</span></span>  <br/> |<span data-ttu-id="25c73-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="25c73-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="25c73-117">Para obtener una referencia desde un programa a la celda ShapePermeableX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="25c73-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c73-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="25c73-118">Section index:</span></span>  <br/> |<span data-ttu-id="25c73-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25c73-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="25c73-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="25c73-120">Row index:</span></span>  <br/> |<span data-ttu-id="25c73-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="25c73-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="25c73-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="25c73-122">Cell index:</span></span>  <br/> |<span data-ttu-id="25c73-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="25c73-123">**visSLOPermX**</span></span> <br/> |
   

