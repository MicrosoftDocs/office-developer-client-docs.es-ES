---
title: Celda ConLineJumpDirX (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico horizontal de una forma.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342752"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="40e72-103">Celda ConLineJumpDirX (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="40e72-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="40e72-104">Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico horizontal de una forma.</span><span class="sxs-lookup"><span data-stu-id="40e72-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="40e72-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="40e72-105">**Value**</span></span>|<span data-ttu-id="40e72-106">**Dirección del salto de línea**</span><span class="sxs-lookup"><span data-stu-id="40e72-106">**Line jump direction**</span></span>|<span data-ttu-id="40e72-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="40e72-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="40e72-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="40e72-108">0</span></span>  <br/> | <span data-ttu-id="40e72-109">Valor predeterminado de página</span><span class="sxs-lookup"><span data-stu-id="40e72-109">Page default</span></span>  <br/> |<span data-ttu-id="40e72-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="40e72-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="40e72-111">1</span><span class="sxs-lookup"><span data-stu-id="40e72-111">1</span></span>  <br/> | <span data-ttu-id="40e72-112">Arriba</span><span class="sxs-lookup"><span data-stu-id="40e72-112">Up</span></span>  <br/> |<span data-ttu-id="40e72-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="40e72-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="40e72-114">segundo</span><span class="sxs-lookup"><span data-stu-id="40e72-114">2</span></span>  <br/> | <span data-ttu-id="40e72-115">Abajo</span><span class="sxs-lookup"><span data-stu-id="40e72-115">Down</span></span>  <br/> |<span data-ttu-id="40e72-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="40e72-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40e72-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40e72-117">Remarks</span></span>

<span data-ttu-id="40e72-118">Para establecer la dirección horizontal predeterminada de *todos los* saltos de conector en una página, utilice la celda PageLineJumpDirX en la sección de diseño de página.</span><span class="sxs-lookup"><span data-stu-id="40e72-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="40e72-119">Para obtener una referencia a la celda ConLineJumpDirX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="40e72-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40e72-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="40e72-120">Cell name:</span></span>  <br/> | <span data-ttu-id="40e72-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="40e72-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="40e72-122">Para obtener una referencia desde un programa a la celda ConLineJumpDirX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="40e72-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40e72-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="40e72-123">Section index:</span></span>  <br/> |<span data-ttu-id="40e72-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40e72-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40e72-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="40e72-125">Row index:</span></span>  <br/> |<span data-ttu-id="40e72-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="40e72-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="40e72-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="40e72-127">Cell index:</span></span>  <br/> |<span data-ttu-id="40e72-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="40e72-128">**visSLOJumpDirX**</span></span> <br/> |
   

