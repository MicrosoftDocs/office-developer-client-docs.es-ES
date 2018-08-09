---
title: Celda PageShapeSplit (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indica si las formas de la página se pueden dividir de forma automática.
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822730"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="72d1f-103">Celda PageShapeSplit (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="72d1f-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="72d1f-104">Indica si las formas de la página se pueden dividir de forma automática.</span><span class="sxs-lookup"><span data-stu-id="72d1f-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="72d1f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="72d1f-105">**Value**</span></span>|<span data-ttu-id="72d1f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72d1f-106">**Description**</span></span>|<span data-ttu-id="72d1f-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="72d1f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72d1f-108">0</span><span class="sxs-lookup"><span data-stu-id="72d1f-108">0</span></span>  <br/> |<span data-ttu-id="72d1f-109">No se permite la división automática de formas.</span><span class="sxs-lookup"><span data-stu-id="72d1f-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="72d1f-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="72d1f-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="72d1f-111">1</span><span class="sxs-lookup"><span data-stu-id="72d1f-111">1</span></span>  <br/> |<span data-ttu-id="72d1f-112">Se permite la división automática de formas (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="72d1f-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="72d1f-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="72d1f-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72d1f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72d1f-114">Remarks</span></span>

<span data-ttu-id="72d1f-p101">La división automática de formas se habilita y deshabilita en tres niveles distintos: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas. La configuración predeterminada para las formas depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="72d1f-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="72d1f-118">Para habilitar o deshabilitar la división en el nivel de aplicación, use la opción **Habilitar división de conectores** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en el botón de **Office** , haga clic en **Opciones** en el de **Visio** ficha y, a continuación, haga clic en **Opciones avanzadas** ).</span><span class="sxs-lookup"><span data-stu-id="72d1f-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="72d1f-119">Para habilitar o deshabilitar la división en el nivel de la forma, vea las celdas ShapeSplit y ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="72d1f-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="72d1f-120">Para obtener una referencia a la celda PageShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="72d1f-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72d1f-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="72d1f-121">Cell name:</span></span>  <br/> |<span data-ttu-id="72d1f-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="72d1f-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="72d1f-123">Para obtener una referencia desde un programa a la celda PageShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="72d1f-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72d1f-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="72d1f-124">Section index:</span></span>  <br/> |<span data-ttu-id="72d1f-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72d1f-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="72d1f-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="72d1f-126">Row index:</span></span>  <br/> |<span data-ttu-id="72d1f-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="72d1f-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="72d1f-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="72d1f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="72d1f-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="72d1f-129">**visPLOSplit**</span></span> <br/> |
   

