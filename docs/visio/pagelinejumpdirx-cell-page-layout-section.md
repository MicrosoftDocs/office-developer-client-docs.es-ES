---
title: Celda PageLineJumpDirX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Determina la dirección de los saltos de línea en conectores dinámicos horizontales en la página de dibujo para los que no se ha aplicado una dirección de salto local.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822715"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="b7e3d-103">Celda PageLineJumpDirX (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="b7e3d-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="b7e3d-104">Determina la dirección de los saltos de línea en conectores dinámicos horizontales en la página de dibujo para los que no se ha aplicado una dirección de salto local.</span><span class="sxs-lookup"><span data-stu-id="b7e3d-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="b7e3d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-105">**Value**</span></span>|<span data-ttu-id="b7e3d-106">**Dirección del salto de línea**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-106">**Line jump direction**</span></span>|<span data-ttu-id="b7e3d-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b7e3d-108">0</span><span class="sxs-lookup"><span data-stu-id="b7e3d-108">0</span></span>  <br/> | <span data-ttu-id="b7e3d-109">Valor predeterminado; izquierda o la configuración de página para las formas</span><span class="sxs-lookup"><span data-stu-id="b7e3d-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="b7e3d-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="b7e3d-111">1</span><span class="sxs-lookup"><span data-stu-id="b7e3d-111">1</span></span>  <br/> | <span data-ttu-id="b7e3d-112">Arriba</span><span class="sxs-lookup"><span data-stu-id="b7e3d-112">Up</span></span>  <br/> |<span data-ttu-id="b7e3d-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="b7e3d-114">2</span><span class="sxs-lookup"><span data-stu-id="b7e3d-114">2</span></span>  <br/> | <span data-ttu-id="b7e3d-115">Abajo</span><span class="sxs-lookup"><span data-stu-id="b7e3d-115">Down</span></span>  <br/> |<span data-ttu-id="b7e3d-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7e3d-117">Notas</span><span class="sxs-lookup"><span data-stu-id="b7e3d-117">Remarks</span></span>

<span data-ttu-id="b7e3d-118">Para obtener una referencia a la celda PageLineJumpDirX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7e3d-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b7e3d-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="b7e3d-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="b7e3d-121">Para obtener una referencia a la celda PageLineJumpDirX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7e3d-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-122">Section index:</span></span>  <br/> |<span data-ttu-id="b7e3d-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b7e3d-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-124">Row index:</span></span>  <br/> |<span data-ttu-id="b7e3d-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b7e3d-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b7e3d-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b7e3d-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="b7e3d-127">**visPLOJumpDirX**</span></span> <br/> |
   

