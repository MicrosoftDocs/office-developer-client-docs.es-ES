---
title: Celda ShapeSplittable (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indica si la forma unidimensional se puede dividir.
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823189"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="61459-103">Celda ShapeSplittable (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="61459-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="61459-104">Indica si la forma unidimensional se puede dividir.</span><span class="sxs-lookup"><span data-stu-id="61459-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="61459-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="61459-105">**Value**</span></span>|<span data-ttu-id="61459-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61459-106">**Description**</span></span>|<span data-ttu-id="61459-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="61459-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="61459-108">0</span><span class="sxs-lookup"><span data-stu-id="61459-108">0</span></span>  <br/> | <span data-ttu-id="61459-109">No se permite la división de la forma.</span><span class="sxs-lookup"><span data-stu-id="61459-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="61459-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="61459-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="61459-111">1</span><span class="sxs-lookup"><span data-stu-id="61459-111">1</span></span>  <br/> | <span data-ttu-id="61459-112">Se permite la división de la forma.</span><span class="sxs-lookup"><span data-stu-id="61459-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="61459-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="61459-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61459-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61459-114">Remarks</span></span>

<span data-ttu-id="61459-115">El comportamiento predeterminado de los conectores y de otras formas unidimensionales depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="61459-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="61459-p101">La división automática de las formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas.</span><span class="sxs-lookup"><span data-stu-id="61459-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="61459-118">Para habilitar o deshabilitar la división en el nivel de aplicación, use la opción **Habilitar división de conectores** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en ** Avanzada** ).</span><span class="sxs-lookup"><span data-stu-id="61459-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="61459-119">Para habilitar o deshabilitar la división en una página, vea la celda [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="61459-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="61459-120">Para hacer que una forma pueda dividir una forma unidimensional divisible, vea la celda [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="61459-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="61459-121">Para obtener una referencia a la celda ShapeSplittable por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="61459-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61459-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="61459-122">Cell name:</span></span>  <br/> | <span data-ttu-id="61459-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="61459-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="61459-124">Para obtener una referencia a la celda ShapeSplittable por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="61459-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61459-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="61459-125">Section index:</span></span>  <br/> |<span data-ttu-id="61459-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61459-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="61459-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="61459-127">Row index:</span></span>  <br/> |<span data-ttu-id="61459-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="61459-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="61459-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="61459-129">Cell index:</span></span>  <br/> |<span data-ttu-id="61459-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="61459-130">**visSLOSplittable**</span></span> <br/> |
   

