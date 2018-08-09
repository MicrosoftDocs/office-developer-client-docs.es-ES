---
title: Celda ConLineJumpDirY (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821823"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="fb97b-103">Celda ConLineJumpDirY (sección Diseño de forma)</span><span class="sxs-lookup"><span data-stu-id="fb97b-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="fb97b-104">Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.</span><span class="sxs-lookup"><span data-stu-id="fb97b-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="fb97b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fb97b-105">**Value**</span></span>|<span data-ttu-id="fb97b-106">**Dirección del salto de línea**</span><span class="sxs-lookup"><span data-stu-id="fb97b-106">**Line Jump Direction**</span></span>|<span data-ttu-id="fb97b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="fb97b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fb97b-108">0</span><span class="sxs-lookup"><span data-stu-id="fb97b-108">0</span></span>  <br/> | <span data-ttu-id="fb97b-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="fb97b-109">Page default</span></span>  <br/> |<span data-ttu-id="fb97b-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="fb97b-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="fb97b-111">1</span><span class="sxs-lookup"><span data-stu-id="fb97b-111">1</span></span>  <br/> | <span data-ttu-id="fb97b-112">Izquierda</span><span class="sxs-lookup"><span data-stu-id="fb97b-112">Left</span></span>  <br/> |<span data-ttu-id="fb97b-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="fb97b-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="fb97b-114">2</span><span class="sxs-lookup"><span data-stu-id="fb97b-114">2</span></span>  <br/> | <span data-ttu-id="fb97b-115">Derecha</span><span class="sxs-lookup"><span data-stu-id="fb97b-115">Right</span></span>  <br/> |<span data-ttu-id="fb97b-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="fb97b-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb97b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb97b-117">Remarks</span></span>

<span data-ttu-id="fb97b-118">Para establecer el valor predeterminado dirección vertical para conector *todos los* saltos de una página, utilice la celda PageLineJumpDirY en la sección de diseño de página.</span><span class="sxs-lookup"><span data-stu-id="fb97b-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="fb97b-119">Para obtener una referencia a la celda ConLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="fb97b-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb97b-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fb97b-120">Cell name:</span></span>  <br/> | <span data-ttu-id="fb97b-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="fb97b-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="fb97b-122">Para obtener una referencia desde un programa a la celda ConLineJumpDirY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb97b-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb97b-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fb97b-123">Section index:</span></span>  <br/> |<span data-ttu-id="fb97b-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb97b-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb97b-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fb97b-125">Row index:</span></span>  <br/> |<span data-ttu-id="fb97b-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="fb97b-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="fb97b-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fb97b-127">Cell index:</span></span>  <br/> |<span data-ttu-id="fb97b-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="fb97b-128">**visSLOJumpDirY**</span></span> <br/> |
   

