---
title: Celda Disabled (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indica si la etiqueta de acción aparece en la ventana de dibujo.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821980"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="69392-103">Celda Disabled (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="69392-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="69392-104">Indica si la etiqueta de acción aparece en la ventana de dibujo.</span><span class="sxs-lookup"><span data-stu-id="69392-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="69392-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="69392-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="69392-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69392-106">**Value**</span></span>|<span data-ttu-id="69392-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69392-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="69392-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="69392-108">TRUE</span></span>  <br/> | <span data-ttu-id="69392-109">Se deshabilita la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="69392-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="69392-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="69392-110">FALSE</span></span>  <br/> | <span data-ttu-id="69392-111">Se habilita la etiqueta de acción (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="69392-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69392-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69392-112">Remarks</span></span>

<span data-ttu-id="69392-113">Cuando se deshabilita una etiqueta de acción, ésta no aparece en absoluto hasta que se vuelva a habilitar.</span><span class="sxs-lookup"><span data-stu-id="69392-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="69392-114">Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="69392-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69392-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="69392-115">Cell name:</span></span>  <br/> | <span data-ttu-id="69392-116">Etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="69392-116">SmartTags.</span></span>  <span data-ttu-id="69392-117">*nombre* . Deshabilitado donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="69392-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="69392-118">*nombre* es el nombre de la fila de etiquetas de acción</span><span class="sxs-lookup"><span data-stu-id="69392-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="69392-119">Para obtener una referencia a la celda Disabled por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="69392-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69392-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="69392-120">Section index:</span></span>  <br/> |<span data-ttu-id="69392-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="69392-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="69392-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="69392-122">Row index:</span></span>  <br/> |<span data-ttu-id="69392-123">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="69392-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="69392-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="69392-124">Cell index:</span></span>  <br/> |<span data-ttu-id="69392-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="69392-125">**visSmartTagDisabled**</span></span> <br/> |
   

