---
title: Celda DrawingScaleType (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Determina la escala de dibujo seleccionada en el cuadro de diálogo Configurar página (haga clic en la flecha de Configurar página en la ficha Inicio).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428742"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="986c4-103">Celda DrawingScaleType (sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="986c4-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="986c4-104">Determina la escala de dibujo seleccionada en el cuadro de diálogo **Configurar página** (haga clic en la flecha de **Configurar página** en la ficha **Inicio**).</span><span class="sxs-lookup"><span data-stu-id="986c4-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="986c4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="986c4-105">**Value**</span></span>|<span data-ttu-id="986c4-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="986c4-106">**Description**</span></span>|<span data-ttu-id="986c4-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="986c4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="986c4-108">0</span><span class="sxs-lookup"><span data-stu-id="986c4-108">0</span></span>  <br/> | <span data-ttu-id="986c4-109">Sin escala</span><span class="sxs-lookup"><span data-stu-id="986c4-109">No Scale</span></span>  <br/> |<span data-ttu-id="986c4-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="986c4-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="986c4-111">1</span><span class="sxs-lookup"><span data-stu-id="986c4-111">1</span></span>  <br/> | <span data-ttu-id="986c4-112">Escala arquitectónica</span><span class="sxs-lookup"><span data-stu-id="986c4-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="986c4-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="986c4-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="986c4-114">2</span><span class="sxs-lookup"><span data-stu-id="986c4-114">2</span></span>  <br/> | <span data-ttu-id="986c4-115">Escala de obras públicas</span><span class="sxs-lookup"><span data-stu-id="986c4-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="986c4-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="986c4-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="986c4-117">3</span><span class="sxs-lookup"><span data-stu-id="986c4-117">3</span></span>  <br/> | <span data-ttu-id="986c4-118">Escala personalizada</span><span class="sxs-lookup"><span data-stu-id="986c4-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="986c4-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="986c4-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="986c4-120">4 </span><span class="sxs-lookup"><span data-stu-id="986c4-120">4</span></span>  <br/> | <span data-ttu-id="986c4-121">Métrica</span><span class="sxs-lookup"><span data-stu-id="986c4-121">Metric</span></span>  <br/> |<span data-ttu-id="986c4-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="986c4-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="986c4-123">5 </span><span class="sxs-lookup"><span data-stu-id="986c4-123">5</span></span>  <br/> | <span data-ttu-id="986c4-124">Escala de ingeniería mecánica</span><span class="sxs-lookup"><span data-stu-id="986c4-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="986c4-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="986c4-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="986c4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="986c4-126">Remarks</span></span>

<span data-ttu-id="986c4-127">Para obtener una referencia a la celda DrawingScaleType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="986c4-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="986c4-128">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="986c4-128">Cell name:</span></span>  <br/> | <span data-ttu-id="986c4-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="986c4-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="986c4-130">Para obtener una referencia desde un programa a la celda DrawingScaleType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="986c4-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="986c4-131">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="986c4-131">Section index:</span></span>  <br/> |<span data-ttu-id="986c4-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="986c4-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="986c4-133">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="986c4-133">Row index:</span></span>  <br/> |<span data-ttu-id="986c4-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="986c4-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="986c4-135">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="986c4-135">Cell index:</span></span>  <br/> |<span data-ttu-id="986c4-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="986c4-136">**visPageDrawScaleType**</span></span> <br/> |
   

