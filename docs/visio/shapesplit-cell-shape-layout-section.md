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
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823182"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="1205c-103">Celda ShapeSplit (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="1205c-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="1205c-104">Indica si la forma puede dividir formas divisibles.</span><span class="sxs-lookup"><span data-stu-id="1205c-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="1205c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1205c-105">**Value**</span></span>|<span data-ttu-id="1205c-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1205c-106">**Description**</span></span>|<span data-ttu-id="1205c-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="1205c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1205c-108">0</span><span class="sxs-lookup"><span data-stu-id="1205c-108">0</span></span>  <br/> | <span data-ttu-id="1205c-109">No se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="1205c-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="1205c-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="1205c-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="1205c-111">1</span><span class="sxs-lookup"><span data-stu-id="1205c-111">1</span></span>  <br/> | <span data-ttu-id="1205c-112">Se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="1205c-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="1205c-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="1205c-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1205c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1205c-114">Remarks</span></span>

<span data-ttu-id="1205c-115">Una forma que pueda dividir otras tiene que ser una forma bidimensional o bien una forma colocable unidimensional.</span><span class="sxs-lookup"><span data-stu-id="1205c-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="1205c-p101">La división automática de formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas; para las formas, depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1205c-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="1205c-118">Para habilitar o deshabilitar la división en el nivel de aplicación, use la opción **Habilitar división de conectores** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en ** Avanzada**).</span><span class="sxs-lookup"><span data-stu-id="1205c-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="1205c-119">Para habilitar o deshabilitar la división en una página, vea la celda PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="1205c-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="1205c-120">Para hacer que una forma unidimensional sea divisible, vea la celda ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="1205c-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="1205c-121">Para obtener una referencia a la celda ShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1205c-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1205c-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1205c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="1205c-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="1205c-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="1205c-124">Para obtener una referencia desde un programa a la celda ShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1205c-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1205c-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1205c-125">Section index:</span></span>  <br/> |<span data-ttu-id="1205c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1205c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1205c-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1205c-127">Row index:</span></span>  <br/> |<span data-ttu-id="1205c-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="1205c-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="1205c-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1205c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1205c-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="1205c-130">**visSLOSplit**</span></span> <br/> |
   

