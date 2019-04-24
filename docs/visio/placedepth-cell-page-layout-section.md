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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346798"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="13fc2-103">Celda PlaceDepth (sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="13fc2-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="13fc2-104">Determina el método mediante el que se analiza el dibujo antes de crear el diseño y determina el tipo de diseño.</span><span class="sxs-lookup"><span data-stu-id="13fc2-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="13fc2-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="13fc2-105">**Value**</span></span>|<span data-ttu-id="13fc2-106">**Profundidad de colocación para los diseños verticales y horizontales**</span><span class="sxs-lookup"><span data-stu-id="13fc2-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="13fc2-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="13fc2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="13fc2-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="13fc2-108">0</span></span>  <br/> | <span data-ttu-id="13fc2-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="13fc2-109">Page default</span></span>  <br/> |<span data-ttu-id="13fc2-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="13fc2-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="13fc2-111">1</span><span class="sxs-lookup"><span data-stu-id="13fc2-111">1</span></span>  <br/> | <span data-ttu-id="13fc2-112">Medio</span><span class="sxs-lookup"><span data-stu-id="13fc2-112">Medium</span></span>  <br/> |<span data-ttu-id="13fc2-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="13fc2-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="13fc2-114">segundo</span><span class="sxs-lookup"><span data-stu-id="13fc2-114">2</span></span>  <br/> | <span data-ttu-id="13fc2-115">Gran</span><span class="sxs-lookup"><span data-stu-id="13fc2-115">Deep</span></span>  <br/> |<span data-ttu-id="13fc2-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="13fc2-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="13fc2-117">3</span><span class="sxs-lookup"><span data-stu-id="13fc2-117">3</span></span>  <br/> | <span data-ttu-id="13fc2-118">Profunda</span><span class="sxs-lookup"><span data-stu-id="13fc2-118">Shallow</span></span>  <br/> |<span data-ttu-id="13fc2-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="13fc2-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13fc2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13fc2-120">Remarks</span></span>

<span data-ttu-id="13fc2-121">Para obtener una referencia a la celda PlaceDepth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="13fc2-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13fc2-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="13fc2-122">Cell name:</span></span>  <br/> | <span data-ttu-id="13fc2-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="13fc2-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="13fc2-124">Para obtener una referencia desde un programa a la celda PlaceDepth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="13fc2-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13fc2-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="13fc2-125">Section index:</span></span>  <br/> |<span data-ttu-id="13fc2-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13fc2-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="13fc2-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="13fc2-127">Row index:</span></span>  <br/> |<span data-ttu-id="13fc2-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="13fc2-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="13fc2-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="13fc2-129">Cell index:</span></span>  <br/> |<span data-ttu-id="13fc2-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="13fc2-130">**visPLOPlaceDepth**</span></span> <br/> |
   

