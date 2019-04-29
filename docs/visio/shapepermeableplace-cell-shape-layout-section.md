---
title: Celda ShapePermeablePlace (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Determina si las formas colocables se pueden colocar encima de una forma al diseñarlas en el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427223"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="833c3-103">Celda ShapePermeablePlace (sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="833c3-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="833c3-104">Determina si las formas colocables se pueden colocar encima de una forma al diseñarlas en el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="833c3-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="833c3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="833c3-105">**Value**</span></span>|<span data-ttu-id="833c3-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="833c3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="833c3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="833c3-107">TRUE</span></span>  <br/> |<span data-ttu-id="833c3-108">Permite que se coloquen formas encima.</span><span class="sxs-lookup"><span data-stu-id="833c3-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="833c3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="833c3-109">FALSE</span></span>  <br/> |<span data-ttu-id="833c3-110">No permite que se coloquen formas encima.</span><span class="sxs-lookup"><span data-stu-id="833c3-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="833c3-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="833c3-111">Remarks</span></span>

<span data-ttu-id="833c3-112">También puede establecer el valor de esta celda en la ficha **colocación** del cuadro de diálogo **comportamiento** (seleccione una forma y, en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en la ficha **colocación** ).</span><span class="sxs-lookup"><span data-stu-id="833c3-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="833c3-113">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="833c3-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="833c3-114">Para obtener una referencia a la celda ShapePermeablePlace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="833c3-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="833c3-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="833c3-115">Cell name:</span></span>  <br/> |<span data-ttu-id="833c3-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="833c3-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="833c3-117">Para obtener una referencia desde un programa a la celda ShapePermeablePlace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="833c3-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="833c3-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="833c3-118">Section index:</span></span>  <br/> |<span data-ttu-id="833c3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="833c3-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="833c3-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="833c3-120">Row index:</span></span>  <br/> |<span data-ttu-id="833c3-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="833c3-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="833c3-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="833c3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="833c3-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="833c3-123">**visSLOPermeablePlace**</span></span> <br/> |
   

