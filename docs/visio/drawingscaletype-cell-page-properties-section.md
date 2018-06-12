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
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822039"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="d70ea-103">Celda DrawingScaleType (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="d70ea-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="d70ea-104">Determina la escala de dibujo seleccionada en el cuadro de diálogo **Configurar página** (haga clic en la flecha de **Configurar página** en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="d70ea-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="d70ea-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d70ea-105">**Value**</span></span>|<span data-ttu-id="d70ea-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d70ea-106">**Description**</span></span>|<span data-ttu-id="d70ea-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="d70ea-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d70ea-108">0</span><span class="sxs-lookup"><span data-stu-id="d70ea-108">0</span></span>  <br/> | <span data-ttu-id="d70ea-109">Sin escala</span><span class="sxs-lookup"><span data-stu-id="d70ea-109">No Scale</span></span>  <br/> |<span data-ttu-id="d70ea-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="d70ea-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="d70ea-111">1</span><span class="sxs-lookup"><span data-stu-id="d70ea-111">1</span></span>  <br/> | <span data-ttu-id="d70ea-112">Escala arquitectónica</span><span class="sxs-lookup"><span data-stu-id="d70ea-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="d70ea-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="d70ea-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="d70ea-114">2</span><span class="sxs-lookup"><span data-stu-id="d70ea-114">2</span></span>  <br/> | <span data-ttu-id="d70ea-115">Escala de obras públicas</span><span class="sxs-lookup"><span data-stu-id="d70ea-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="d70ea-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="d70ea-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="d70ea-117">3</span><span class="sxs-lookup"><span data-stu-id="d70ea-117">3</span></span>  <br/> | <span data-ttu-id="d70ea-118">Escala personalizada</span><span class="sxs-lookup"><span data-stu-id="d70ea-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="d70ea-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="d70ea-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="d70ea-120">4</span><span class="sxs-lookup"><span data-stu-id="d70ea-120">4</span></span>  <br/> | <span data-ttu-id="d70ea-121">Métrica</span><span class="sxs-lookup"><span data-stu-id="d70ea-121">Metric</span></span>  <br/> |<span data-ttu-id="d70ea-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="d70ea-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="d70ea-123">5</span><span class="sxs-lookup"><span data-stu-id="d70ea-123">5</span></span>  <br/> | <span data-ttu-id="d70ea-124">Escala de ingeniería mecánica</span><span class="sxs-lookup"><span data-stu-id="d70ea-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="d70ea-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="d70ea-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d70ea-126">Notas</span><span class="sxs-lookup"><span data-stu-id="d70ea-126">Remarks</span></span>

<span data-ttu-id="d70ea-127">Para obtener una referencia a la celda DrawingScaleType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="d70ea-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d70ea-128">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d70ea-128">Cell name:</span></span>  <br/> | <span data-ttu-id="d70ea-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="d70ea-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="d70ea-130">Para obtener una referencia a la celda DrawingScaleType por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d70ea-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d70ea-131">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d70ea-131">Section index:</span></span>  <br/> |<span data-ttu-id="d70ea-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d70ea-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d70ea-133">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d70ea-133">Row index:</span></span>  <br/> |<span data-ttu-id="d70ea-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="d70ea-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="d70ea-135">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d70ea-135">Cell index:</span></span>  <br/> |<span data-ttu-id="d70ea-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="d70ea-136">**visPageDrawScaleType**</span></span> <br/> |
   

