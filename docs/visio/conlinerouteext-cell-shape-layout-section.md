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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327107"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="0e6b5-103">Celda ConLineRouteExt (Sección de diseño de la forma)</span><span class="sxs-lookup"><span data-stu-id="0e6b5-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="0e6b5-104">Determina la apariencia de un conector.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="0e6b5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-105">**Value**</span></span>|<span data-ttu-id="0e6b5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-106">**Description**</span></span>|<span data-ttu-id="0e6b5-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0e6b5-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="0e6b5-108">0</span></span>  <br/> | <span data-ttu-id="0e6b5-109">Valor predeterminado (se usa la configuración de página)</span><span class="sxs-lookup"><span data-stu-id="0e6b5-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="0e6b5-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="0e6b5-111">1</span><span class="sxs-lookup"><span data-stu-id="0e6b5-111">1</span></span>  <br/> | <span data-ttu-id="0e6b5-112">Directas</span><span class="sxs-lookup"><span data-stu-id="0e6b5-112">Straight</span></span>  <br/> |<span data-ttu-id="0e6b5-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="0e6b5-114">segundo</span><span class="sxs-lookup"><span data-stu-id="0e6b5-114">2</span></span>  <br/> | <span data-ttu-id="0e6b5-115">Hacia</span><span class="sxs-lookup"><span data-stu-id="0e6b5-115">Curved</span></span>  <br/> |<span data-ttu-id="0e6b5-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e6b5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e6b5-117">Remarks</span></span>

<span data-ttu-id="0e6b5-118">Para obtener una referencia a la celda ConLineRouteExt por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e6b5-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-119">Cell name:</span></span>  <br/> | <span data-ttu-id="0e6b5-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="0e6b5-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="0e6b5-121">Para obtener una referencia desde un programa a la celda ConLineRouteExt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e6b5-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-122">Section index:</span></span>  <br/> |<span data-ttu-id="0e6b5-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0e6b5-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-124">Row index:</span></span>  <br/> |<span data-ttu-id="0e6b5-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="0e6b5-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0e6b5-126">Cell index:</span></span>  <br/> |<span data-ttu-id="0e6b5-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-127">**visSLOLineRouteExt**</span></span> <br/> |
   

