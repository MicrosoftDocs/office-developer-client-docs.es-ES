---
title: Celda LineRouteExt (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Determina la apariencia predeterminada para todos los conectores de una página de dibujo.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358985"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="0cc51-103">Celda LineRouteExt (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="0cc51-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="0cc51-104">Determina la apariencia predeterminada para todos los conectores de una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="0cc51-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="0cc51-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="0cc51-105">**Value**</span></span>|<span data-ttu-id="0cc51-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cc51-106">**Description**</span></span>|<span data-ttu-id="0cc51-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="0cc51-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0cc51-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="0cc51-108">0</span></span>  <br/> | <span data-ttu-id="0cc51-109">Valor predeterminado (recta)</span><span class="sxs-lookup"><span data-stu-id="0cc51-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="0cc51-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="0cc51-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="0cc51-111">1</span><span class="sxs-lookup"><span data-stu-id="0cc51-111">1</span></span>  <br/> | <span data-ttu-id="0cc51-112">Directas</span><span class="sxs-lookup"><span data-stu-id="0cc51-112">Straight</span></span>  <br/> |<span data-ttu-id="0cc51-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="0cc51-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="0cc51-114">segundo</span><span class="sxs-lookup"><span data-stu-id="0cc51-114">2</span></span>  <br/> | <span data-ttu-id="0cc51-115">Hacia</span><span class="sxs-lookup"><span data-stu-id="0cc51-115">Curved</span></span>  <br/> |<span data-ttu-id="0cc51-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="0cc51-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cc51-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cc51-117">Remarks</span></span>

<span data-ttu-id="0cc51-118">Para obtener una referencia a la celda LineRouteExt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0cc51-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cc51-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0cc51-119">Cell name:</span></span>  <br/> | <span data-ttu-id="0cc51-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="0cc51-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="0cc51-121">Para obtener una referencia desde un programa a la celda LineRouteExt por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0cc51-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cc51-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0cc51-122">Section index:</span></span>  <br/> |<span data-ttu-id="0cc51-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0cc51-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0cc51-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0cc51-124">Row index:</span></span>  <br/> |<span data-ttu-id="0cc51-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0cc51-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0cc51-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0cc51-126">Cell index:</span></span>  <br/> |<span data-ttu-id="0cc51-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="0cc51-127">**visPLOLineRouteExt**</span></span> <br/> |
   

