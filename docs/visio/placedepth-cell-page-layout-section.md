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
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432040"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="a9d58-103">Celda PlaceDepth (sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="a9d58-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="a9d58-104">Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.</span><span class="sxs-lookup"><span data-stu-id="a9d58-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="a9d58-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a9d58-105">**Value**</span></span>|<span data-ttu-id="a9d58-106">**Profundidad de colocación para los diseños verticales y horizontales**</span><span class="sxs-lookup"><span data-stu-id="a9d58-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="a9d58-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="a9d58-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a9d58-108">0</span><span class="sxs-lookup"><span data-stu-id="a9d58-108">0</span></span>  <br/> | <span data-ttu-id="a9d58-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="a9d58-109">Page default</span></span>  <br/> |<span data-ttu-id="a9d58-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="a9d58-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="a9d58-111">1 </span><span class="sxs-lookup"><span data-stu-id="a9d58-111">1</span></span>  <br/> | <span data-ttu-id="a9d58-112">Mediano</span><span class="sxs-lookup"><span data-stu-id="a9d58-112">Medium</span></span>  <br/> |<span data-ttu-id="a9d58-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="a9d58-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="a9d58-114">2 </span><span class="sxs-lookup"><span data-stu-id="a9d58-114">2</span></span>  <br/> | <span data-ttu-id="a9d58-115">Deep</span><span class="sxs-lookup"><span data-stu-id="a9d58-115">Deep</span></span>  <br/> |<span data-ttu-id="a9d58-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="a9d58-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="a9d58-117">3 </span><span class="sxs-lookup"><span data-stu-id="a9d58-117">3</span></span>  <br/> | <span data-ttu-id="a9d58-118">Superficial</span><span class="sxs-lookup"><span data-stu-id="a9d58-118">Shallow</span></span>  <br/> |<span data-ttu-id="a9d58-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="a9d58-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9d58-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9d58-120">Remarks</span></span>

<span data-ttu-id="a9d58-121">Para obtener una referencia a la celda PlaceDepth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a9d58-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9d58-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a9d58-122">Cell name:</span></span>  <br/> | <span data-ttu-id="a9d58-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="a9d58-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="a9d58-124">Para obtener una referencia desde un programa a la celda PlaceDepth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9d58-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9d58-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a9d58-125">Section index:</span></span>  <br/> |<span data-ttu-id="a9d58-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9d58-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a9d58-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a9d58-127">Row index:</span></span>  <br/> |<span data-ttu-id="a9d58-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a9d58-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a9d58-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a9d58-129">Cell index:</span></span>  <br/> |<span data-ttu-id="a9d58-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="a9d58-130">**visPLOPlaceDepth**</span></span> <br/> |
   

