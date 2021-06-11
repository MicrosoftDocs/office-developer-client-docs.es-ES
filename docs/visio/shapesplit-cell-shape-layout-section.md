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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423562"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="4218c-103">Celda ShapeSplit (Sección de diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="4218c-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="4218c-104">Indica si la forma puede dividir formas divisibles.</span><span class="sxs-lookup"><span data-stu-id="4218c-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="4218c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4218c-105">**Value**</span></span>|<span data-ttu-id="4218c-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4218c-106">**Description**</span></span>|<span data-ttu-id="4218c-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="4218c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4218c-108">0</span><span class="sxs-lookup"><span data-stu-id="4218c-108">0</span></span>  <br/> | <span data-ttu-id="4218c-109">No se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="4218c-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="4218c-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="4218c-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="4218c-111">1</span><span class="sxs-lookup"><span data-stu-id="4218c-111">1</span></span>  <br/> | <span data-ttu-id="4218c-112">Se permite que esta forma divida otras formas.</span><span class="sxs-lookup"><span data-stu-id="4218c-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="4218c-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="4218c-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4218c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4218c-114">Remarks</span></span>

<span data-ttu-id="4218c-115">Una forma que pueda dividir otras tiene que ser una forma bidimensional o bien una forma colocable unidimensional.</span><span class="sxs-lookup"><span data-stu-id="4218c-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="4218c-p101">La división automática de formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas; para las formas, depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="4218c-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="4218c-118">Para habilitar o deshabilitar la división en  el nivel de  aplicación, use la opción Habilitar división  del conector en la ficha Avanzadas del cuadro de diálogo Opciones de Visio (haga clic en la pestaña Archivo, en Opciones y, **a** continuación, en Avanzadas **).**</span><span class="sxs-lookup"><span data-stu-id="4218c-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="4218c-119">Para habilitar o deshabilitar la división en una página, vea la celda PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="4218c-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="4218c-120">Para hacer que una forma unidimensional sea divisible, vea la celda ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="4218c-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="4218c-121">Para obtener una referencia a la celda ShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="4218c-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4218c-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4218c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="4218c-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="4218c-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="4218c-124">Para obtener una referencia desde un programa a la celda ShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4218c-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4218c-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4218c-125">Section index:</span></span>  <br/> |<span data-ttu-id="4218c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4218c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4218c-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4218c-127">Row index:</span></span>  <br/> |<span data-ttu-id="4218c-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="4218c-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="4218c-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4218c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="4218c-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="4218c-130">**visSLOSplit**</span></span> <br/> |
   

