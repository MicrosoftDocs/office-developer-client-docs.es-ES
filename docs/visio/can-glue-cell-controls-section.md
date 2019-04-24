---
title: Celda Can Glue (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Determina si un controlador puede pegarse a otras formas.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337257"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="f2ff6-103">Celda Can Glue (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="f2ff6-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="f2ff6-104">Determina si un controlador puede pegarse a otras formas.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="f2ff6-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="f2ff6-105">**Value**</span></span>|<span data-ttu-id="f2ff6-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2ff6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f2ff6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2ff6-107">TRUE</span></span>  <br/> | <span data-ttu-id="f2ff6-108">El controlador puede pegarse.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="f2ff6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f2ff6-109">FALSE</span></span>  <br/> | <span data-ttu-id="f2ff6-110">El controlador no puede pegarse.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2ff6-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2ff6-111">Remarks</span></span>

<span data-ttu-id="f2ff6-112">Para obtener una referencia a la celda Can Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2ff6-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f2ff6-114">Mando.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-114">Controls.</span></span>  <span data-ttu-id="f2ff6-115">*nombre* . Controles CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="f2ff6-116">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f2ff6-117">Para obtener una referencia desde un programa a la celda Can Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2ff6-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-118">Section index:</span></span>  <br/> |<span data-ttu-id="f2ff6-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f2ff6-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f2ff6-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-120">Row index:</span></span>  <br/> |<span data-ttu-id="f2ff6-121">**visRowControl** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f2ff6-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="f2ff6-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f2ff6-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="f2ff6-123">**visCtlGlue**</span></span> <br/> |
   

