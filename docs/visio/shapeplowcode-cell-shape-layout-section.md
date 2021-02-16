---
title: Celda ShapePlowCode (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Determina si esta forma colocable se quita al colocar junto a ella otra forma colocable en la página de dibujo.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423898"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="b5f97-103">Celda ShapePlowCode (Sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="b5f97-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="b5f97-104">Determina si esta forma colocable se quita al colocar junto a ella otra forma colocable en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b5f97-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="b5f97-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b5f97-105">**Value**</span></span>|<span data-ttu-id="b5f97-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5f97-106">**Description**</span></span>|<span data-ttu-id="b5f97-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="b5f97-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5f97-108">0</span><span class="sxs-lookup"><span data-stu-id="b5f97-108">0</span></span>  <br/> |<span data-ttu-id="b5f97-109">Se quita tal como especifique la página.</span><span class="sxs-lookup"><span data-stu-id="b5f97-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="b5f97-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="b5f97-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="b5f97-111">1 </span><span class="sxs-lookup"><span data-stu-id="b5f97-111">1</span></span>  <br/> |<span data-ttu-id="b5f97-112">No se quita ninguna forma.</span><span class="sxs-lookup"><span data-stu-id="b5f97-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="b5f97-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="b5f97-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="b5f97-114">2 </span><span class="sxs-lookup"><span data-stu-id="b5f97-114">2</span></span>  <br/> |<span data-ttu-id="b5f97-115">Se quitan todas las formas.</span><span class="sxs-lookup"><span data-stu-id="b5f97-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="b5f97-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="b5f97-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5f97-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5f97-117">Remarks</span></span>

<span data-ttu-id="b5f97-118">También puede establecer el valor de esta celda para una  forma determinada en la ficha [](run-in-developer-mode-display-the-developer-tab.md) Colocación del  cuadro de diálogo Comportamiento (con una forma seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la ficha Colocación).   </span><span class="sxs-lookup"><span data-stu-id="b5f97-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="b5f97-119">Para establecer este comportamiento para  *todas las*  formas de la página de dibujo, use la celda PlowCode de la sección Diseño de página.</span><span class="sxs-lookup"><span data-stu-id="b5f97-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="b5f97-120">Para obtener una referencia a la celda ShapePlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b5f97-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5f97-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b5f97-121">Cell name:</span></span>  <br/> |<span data-ttu-id="b5f97-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="b5f97-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="b5f97-123">Para obtener una referencia desde un programa a la celda ShapePlowCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5f97-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5f97-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b5f97-124">Section index:</span></span>  <br/> |<span data-ttu-id="b5f97-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5f97-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b5f97-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b5f97-126">Row index:</span></span>  <br/> |<span data-ttu-id="b5f97-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="b5f97-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="b5f97-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b5f97-128">Cell index:</span></span>  <br/> |<span data-ttu-id="b5f97-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="b5f97-129">**visSLOPlowCode**</span></span> <br/> |
   

