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
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823149"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="a2a45-103">Celda ShapePermeablePlace (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="a2a45-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="a2a45-104">Determina si las formas colocables se pueden colocar encima de una forma al diseñarlas en el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="a2a45-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="a2a45-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a2a45-105">**Value**</span></span>|<span data-ttu-id="a2a45-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2a45-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2a45-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2a45-107">TRUE</span></span>  <br/> |<span data-ttu-id="a2a45-108">Permite que se coloquen formas encima.</span><span class="sxs-lookup"><span data-stu-id="a2a45-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="a2a45-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2a45-109">FALSE</span></span>  <br/> |<span data-ttu-id="a2a45-110">No permite que se coloquen formas encima.</span><span class="sxs-lookup"><span data-stu-id="a2a45-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2a45-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2a45-111">Remarks</span></span>

<span data-ttu-id="a2a45-112">También puede establecer el valor de esta celda en la ficha de **colocación** en el cuadro de diálogo **comportamiento** (con una forma seleccionada, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en la ficha **colocación** ).</span><span class="sxs-lookup"><span data-stu-id="a2a45-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="a2a45-113">En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.</span><span class="sxs-lookup"><span data-stu-id="a2a45-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="a2a45-114">Para obtener una referencia a la celda ShapePermeablePlace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="a2a45-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2a45-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a2a45-115">Cell name:</span></span>  <br/> |<span data-ttu-id="a2a45-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="a2a45-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="a2a45-117">Para obtener una referencia desde un programa a la celda ShapePermeablePlace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a2a45-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2a45-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a2a45-118">Section index:</span></span>  <br/> |<span data-ttu-id="a2a45-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2a45-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a2a45-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a2a45-120">Row index:</span></span>  <br/> |<span data-ttu-id="a2a45-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="a2a45-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="a2a45-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a2a45-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a2a45-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="a2a45-123">**visSLOPermeablePlace**</span></span> <br/> |
   

