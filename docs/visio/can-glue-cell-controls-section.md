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
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821684"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="b2dd5-103">Celda Can Glue (sección Controles)</span><span class="sxs-lookup"><span data-stu-id="b2dd5-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="b2dd5-104">Determina si un controlador puede pegarse a otras formas.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="b2dd5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b2dd5-105">**Value**</span></span>|<span data-ttu-id="b2dd5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b2dd5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b2dd5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2dd5-107">TRUE</span></span>  <br/> | <span data-ttu-id="b2dd5-108">El controlador puede pegarse.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="b2dd5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2dd5-109">FALSE</span></span>  <br/> | <span data-ttu-id="b2dd5-110">El controlador no puede pegarse.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2dd5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2dd5-111">Remarks</span></span>

<span data-ttu-id="b2dd5-112">Para obtener una referencia a la celda Can Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2dd5-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b2dd5-114">Controles.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-114">Controls.</span></span>  <span data-ttu-id="b2dd5-115">*nombre* . Controles de CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="b2dd5-116">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="b2dd5-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="b2dd5-117">Para obtener una referencia desde un programa a la celda Can Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2dd5-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-118">Section index:</span></span>  <br/> |<span data-ttu-id="b2dd5-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="b2dd5-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="b2dd5-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-120">Row index:</span></span>  <br/> |<span data-ttu-id="b2dd5-121">**visRowControl** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="b2dd5-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="b2dd5-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b2dd5-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b2dd5-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="b2dd5-123">**visCtlGlue**</span></span> <br/> |
   

