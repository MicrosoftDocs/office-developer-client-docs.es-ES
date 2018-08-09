---
title: Celda PlaceDepth (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822739"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="9c96d-103">Celda PlaceDepth (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="9c96d-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="9c96d-104">Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.</span><span class="sxs-lookup"><span data-stu-id="9c96d-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="9c96d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9c96d-105">**Value**</span></span>|<span data-ttu-id="9c96d-106">**Profundidad de colocación para los diseños verticales y horizontales**</span><span class="sxs-lookup"><span data-stu-id="9c96d-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="9c96d-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="9c96d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9c96d-108">0</span><span class="sxs-lookup"><span data-stu-id="9c96d-108">0</span></span>  <br/> | <span data-ttu-id="9c96d-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="9c96d-109">Page default</span></span>  <br/> |<span data-ttu-id="9c96d-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="9c96d-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="9c96d-111">1</span><span class="sxs-lookup"><span data-stu-id="9c96d-111">1</span></span>  <br/> | <span data-ttu-id="9c96d-112">Media</span><span class="sxs-lookup"><span data-stu-id="9c96d-112">Medium</span></span>  <br/> |<span data-ttu-id="9c96d-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="9c96d-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="9c96d-114">2</span><span class="sxs-lookup"><span data-stu-id="9c96d-114">2</span></span>  <br/> | <span data-ttu-id="9c96d-115">Profunda</span><span class="sxs-lookup"><span data-stu-id="9c96d-115">Deep</span></span>  <br/> |<span data-ttu-id="9c96d-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="9c96d-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="9c96d-117">3</span><span class="sxs-lookup"><span data-stu-id="9c96d-117">3</span></span>  <br/> | <span data-ttu-id="9c96d-118">Superficial</span><span class="sxs-lookup"><span data-stu-id="9c96d-118">Shallow</span></span>  <br/> |<span data-ttu-id="9c96d-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="9c96d-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c96d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c96d-120">Remarks</span></span>

<span data-ttu-id="9c96d-121">Para obtener una referencia a la celda PlaceDepth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9c96d-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c96d-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9c96d-122">Cell name:</span></span>  <br/> | <span data-ttu-id="9c96d-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="9c96d-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="9c96d-124">Para obtener una referencia desde un programa a la celda PlaceDepth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c96d-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c96d-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9c96d-125">Section index:</span></span>  <br/> |<span data-ttu-id="9c96d-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9c96d-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9c96d-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9c96d-127">Row index:</span></span>  <br/> |<span data-ttu-id="9c96d-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9c96d-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9c96d-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9c96d-129">Cell index:</span></span>  <br/> |<span data-ttu-id="9c96d-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="9c96d-130">**visPLOPlaceDepth**</span></span> <br/> |
   

