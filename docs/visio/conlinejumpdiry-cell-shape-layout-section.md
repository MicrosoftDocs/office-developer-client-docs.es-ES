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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342745"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="3f3e5-103">Celda ConLineJumpDirY (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="3f3e5-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3f3e5-104">Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.</span><span class="sxs-lookup"><span data-stu-id="3f3e5-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="3f3e5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-105">**Value**</span></span>|<span data-ttu-id="3f3e5-106">**Dirección del salto de línea**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-106">**Line Jump Direction**</span></span>|<span data-ttu-id="3f3e5-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3f3e5-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="3f3e5-108">0</span></span>  <br/> | <span data-ttu-id="3f3e5-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="3f3e5-109">Page default</span></span>  <br/> |<span data-ttu-id="3f3e5-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="3f3e5-111">1</span><span class="sxs-lookup"><span data-stu-id="3f3e5-111">1</span></span>  <br/> | <span data-ttu-id="3f3e5-112">Hacia la izquierda</span><span class="sxs-lookup"><span data-stu-id="3f3e5-112">Left</span></span>  <br/> |<span data-ttu-id="3f3e5-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="3f3e5-114">segundo</span><span class="sxs-lookup"><span data-stu-id="3f3e5-114">2</span></span>  <br/> | <span data-ttu-id="3f3e5-115">Derecha</span><span class="sxs-lookup"><span data-stu-id="3f3e5-115">Right</span></span>  <br/> |<span data-ttu-id="3f3e5-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f3e5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f3e5-117">Remarks</span></span>

<span data-ttu-id="3f3e5-118">Para establecer la dirección vertical predeterminada para *todos los* saltos de conector en una página, utilice la celda PageLineJumpDirY en la sección de diseño de página.</span><span class="sxs-lookup"><span data-stu-id="3f3e5-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="3f3e5-119">Para obtener una referencia a la celda ConLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f3e5-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-120">Cell name:</span></span>  <br/> | <span data-ttu-id="3f3e5-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="3f3e5-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="3f3e5-122">Para obtener una referencia desde un programa a la celda ConLineJumpDirY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f3e5-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-123">Section index:</span></span>  <br/> |<span data-ttu-id="3f3e5-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f3e5-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-125">Row index:</span></span>  <br/> |<span data-ttu-id="3f3e5-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="3f3e5-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3f3e5-127">Cell index:</span></span>  <br/> |<span data-ttu-id="3f3e5-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="3f3e5-128">**visSLOJumpDirY**</span></span> <br/> |
   

