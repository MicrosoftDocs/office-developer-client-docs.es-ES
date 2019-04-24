---
title: Celda ShapeSplit (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indica si la forma puede dividir formas divisibles.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349122"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="6900d-103">Celda ShapeSplit (Sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="6900d-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="6900d-104">Indica si la forma puede dividir formas divisibles.</span><span class="sxs-lookup"><span data-stu-id="6900d-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="6900d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6900d-105">**Value**</span></span>|<span data-ttu-id="6900d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6900d-106">**Description**</span></span>|<span data-ttu-id="6900d-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="6900d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6900d-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="6900d-108">0</span></span>  <br/> | <span data-ttu-id="6900d-109">No se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="6900d-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="6900d-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="6900d-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="6900d-111">1</span><span class="sxs-lookup"><span data-stu-id="6900d-111">1</span></span>  <br/> | <span data-ttu-id="6900d-112">Se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="6900d-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="6900d-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="6900d-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6900d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6900d-114">Remarks</span></span>

<span data-ttu-id="6900d-115">Una forma que pueda dividir otras tiene que ser una forma bidimensional o bien una forma colocable unidimensional.</span><span class="sxs-lookup"><span data-stu-id="6900d-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="6900d-p101">La división automática de formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas; para las formas, depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="6900d-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="6900d-118">Para habilitar o deshabilitar la división en el nivel de la aplicación, use la opción **Habilitar División de conectores** de la ficha **avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en \*\* Avanzado\*\*).</span><span class="sxs-lookup"><span data-stu-id="6900d-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="6900d-119">Para habilitar o deshabilitar la división en una página, vea la celda PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="6900d-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="6900d-120">Para hacer que una forma unidimensional sea divisible, vea la celda ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="6900d-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="6900d-121">Para obtener una referencia a la celda ShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="6900d-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6900d-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6900d-122">Cell name:</span></span>  <br/> | <span data-ttu-id="6900d-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="6900d-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="6900d-124">Para obtener una referencia desde un programa a la celda ShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6900d-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6900d-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6900d-125">Section index:</span></span>  <br/> |<span data-ttu-id="6900d-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6900d-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6900d-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6900d-127">Row index:</span></span>  <br/> |<span data-ttu-id="6900d-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="6900d-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="6900d-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6900d-129">Cell index:</span></span>  <br/> |<span data-ttu-id="6900d-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="6900d-130">**visSLOSplit**</span></span> <br/> |
   

