---
title: Celda PageLineJumpDirY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Determina la dirección de los saltos de línea en conectores dinámicos verticales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414679"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="3fdf8-103">Celda PageLineJumpDirY (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="3fdf8-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="3fdf8-104">Determina la dirección de los saltos de línea en conectores dinámicos verticales en la página de dibujo para los que no se ha aplicado una dirección de salto local.</span><span class="sxs-lookup"><span data-stu-id="3fdf8-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="3fdf8-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-105">**Value**</span></span>|<span data-ttu-id="3fdf8-106">**Dirección del salto de línea**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-106">**Line jump direction**</span></span>|<span data-ttu-id="3fdf8-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3fdf8-108">0</span><span class="sxs-lookup"><span data-stu-id="3fdf8-108">0</span></span>  <br/> | <span data-ttu-id="3fdf8-109">Valor predeterminado; arriba o la configuración de página para las formas</span><span class="sxs-lookup"><span data-stu-id="3fdf8-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="3fdf8-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="3fdf8-111">1 </span><span class="sxs-lookup"><span data-stu-id="3fdf8-111">1</span></span>  <br/> | <span data-ttu-id="3fdf8-112">Hacia la izquierda</span><span class="sxs-lookup"><span data-stu-id="3fdf8-112">Left</span></span>  <br/> |<span data-ttu-id="3fdf8-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="3fdf8-114">2 </span><span class="sxs-lookup"><span data-stu-id="3fdf8-114">2</span></span>  <br/> | <span data-ttu-id="3fdf8-115">Derecha</span><span class="sxs-lookup"><span data-stu-id="3fdf8-115">Right</span></span>  <br/> |<span data-ttu-id="3fdf8-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fdf8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fdf8-117">Remarks</span></span>

<span data-ttu-id="3fdf8-118">Para obtener una referencia a la celda PageLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3fdf8-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-119">Cell name:</span></span>  <br/> | <span data-ttu-id="3fdf8-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="3fdf8-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="3fdf8-121">Para obtener una referencia desde un programa a la celda PageLineJumpDirY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3fdf8-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-122">Section index:</span></span>  <br/> |<span data-ttu-id="3fdf8-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3fdf8-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-124">Row index:</span></span>  <br/> |<span data-ttu-id="3fdf8-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="3fdf8-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3fdf8-126">Cell index:</span></span>  <br/> |<span data-ttu-id="3fdf8-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="3fdf8-127">**visPLOJumpDirY**</span></span> <br/> |
   

