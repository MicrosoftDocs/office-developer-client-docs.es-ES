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
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422022"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="8c50a-103">Celda PageShapeSplit (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="8c50a-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="8c50a-104">Indica si las formas de la página se pueden dividir de forma automática.</span><span class="sxs-lookup"><span data-stu-id="8c50a-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="8c50a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8c50a-105">**Value**</span></span>|<span data-ttu-id="8c50a-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c50a-106">**Description**</span></span>|<span data-ttu-id="8c50a-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8c50a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c50a-108">0</span><span class="sxs-lookup"><span data-stu-id="8c50a-108">0</span></span>  <br/> |<span data-ttu-id="8c50a-109">No se permite la división automática de formas.</span><span class="sxs-lookup"><span data-stu-id="8c50a-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="8c50a-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="8c50a-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="8c50a-111">1</span><span class="sxs-lookup"><span data-stu-id="8c50a-111">1</span></span>  <br/> |<span data-ttu-id="8c50a-112">Se permite la división automática de formas (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="8c50a-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="8c50a-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="8c50a-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c50a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c50a-114">Remarks</span></span>

<span data-ttu-id="8c50a-p101">La división automática de formas se habilita y deshabilita en tres niveles distintos: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas. La configuración predeterminada para las formas depende del tipo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8c50a-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="8c50a-118">Para habilitar o deshabilitar la división en  el nivel de aplicación, use la opción Habilitar división de conectores en la  ficha Avanzadas del cuadro de diálogo Opciones de **Visio** (haga clic en el botón **Office,** haga clic en Opciones en la pestaña **Visio y, a** continuación, haga clic en  **Avanzadas** ).</span><span class="sxs-lookup"><span data-stu-id="8c50a-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="8c50a-119">Para habilitar o deshabilitar la división en el nivel de forma, vea las celdas ShapeSplit y ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="8c50a-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="8c50a-120">Para obtener una referencia a la celda PageShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8c50a-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c50a-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8c50a-121">Cell name:</span></span>  <br/> |<span data-ttu-id="8c50a-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="8c50a-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="8c50a-123">Para obtener una referencia desde un programa a la celda PageShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8c50a-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c50a-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8c50a-124">Section index:</span></span>  <br/> |<span data-ttu-id="8c50a-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c50a-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8c50a-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8c50a-126">Row index:</span></span>  <br/> |<span data-ttu-id="8c50a-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8c50a-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8c50a-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8c50a-128">Cell index:</span></span>  <br/> |<span data-ttu-id="8c50a-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="8c50a-129">**visPLOSplit**</span></span> <br/> |
   

