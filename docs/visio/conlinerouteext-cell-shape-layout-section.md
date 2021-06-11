---
title: Celda ConLineRouteExt (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Determina la apariencia de un conector.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434616"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="1a44a-103">Celda ConLineRouteExt (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="1a44a-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="1a44a-104">Determina la apariencia de un conector.</span><span class="sxs-lookup"><span data-stu-id="1a44a-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="1a44a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1a44a-105">**Value**</span></span>|<span data-ttu-id="1a44a-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a44a-106">**Description**</span></span>|<span data-ttu-id="1a44a-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="1a44a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1a44a-108">0</span><span class="sxs-lookup"><span data-stu-id="1a44a-108">0</span></span>  <br/> | <span data-ttu-id="1a44a-109">Valor predeterminado (se usa la configuración de página)</span><span class="sxs-lookup"><span data-stu-id="1a44a-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="1a44a-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="1a44a-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="1a44a-111">1</span><span class="sxs-lookup"><span data-stu-id="1a44a-111">1</span></span>  <br/> | <span data-ttu-id="1a44a-112">Recto</span><span class="sxs-lookup"><span data-stu-id="1a44a-112">Straight</span></span>  <br/> |<span data-ttu-id="1a44a-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="1a44a-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="1a44a-114">2</span><span class="sxs-lookup"><span data-stu-id="1a44a-114">2</span></span>  <br/> | <span data-ttu-id="1a44a-115">Curvado</span><span class="sxs-lookup"><span data-stu-id="1a44a-115">Curved</span></span>  <br/> |<span data-ttu-id="1a44a-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="1a44a-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a44a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a44a-117">Remarks</span></span>

<span data-ttu-id="1a44a-118">Para obtener una referencia a la celda ConLineRouteExt por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1a44a-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1a44a-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1a44a-119">Cell name:</span></span>  <br/> | <span data-ttu-id="1a44a-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="1a44a-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="1a44a-121">Para obtener una referencia desde un programa a la celda ConLineRouteExt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a44a-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1a44a-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1a44a-122">Section index:</span></span>  <br/> |<span data-ttu-id="1a44a-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1a44a-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1a44a-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1a44a-124">Row index:</span></span>  <br/> |<span data-ttu-id="1a44a-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="1a44a-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="1a44a-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1a44a-126">Cell index:</span></span>  <br/> |<span data-ttu-id="1a44a-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="1a44a-127">**visSLOLineRouteExt**</span></span> <br/> |
   

