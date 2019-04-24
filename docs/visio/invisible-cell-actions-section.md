---
title: Celda Invisible (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indica si la acción está visible en el menú contextual o de etiqueta de acción.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297245"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="00cfa-103">Celda Invisible (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="00cfa-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="00cfa-104">Indica si la acción está visible en el menú contextual o de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="00cfa-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00cfa-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="00cfa-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="00cfa-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="00cfa-106">**Value**</span></span>|<span data-ttu-id="00cfa-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00cfa-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00cfa-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="00cfa-108">TRUE</span></span>  <br/> |<span data-ttu-id="00cfa-109">La acción no está visible en el menú.</span><span class="sxs-lookup"><span data-stu-id="00cfa-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="00cfa-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="00cfa-110">FALSE</span></span>  <br/> |<span data-ttu-id="00cfa-111">La acción está visible en el menú (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="00cfa-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00cfa-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00cfa-112">Remarks</span></span>

<span data-ttu-id="00cfa-113">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="00cfa-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00cfa-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="00cfa-114">Cell name:</span></span>  <br/> |<span data-ttu-id="00cfa-115">Actividades.</span><span class="sxs-lookup"><span data-stu-id="00cfa-115">Actions.</span></span> <span data-ttu-id="00cfa-116">*nombre* . Acciones Invisibledonde.</span><span class="sxs-lookup"><span data-stu-id="00cfa-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="00cfa-117">*nombre* es el nombre de la fila de acciones.</span><span class="sxs-lookup"><span data-stu-id="00cfa-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="00cfa-118">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="00cfa-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00cfa-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="00cfa-119">Section index:</span></span>  <br/> |<span data-ttu-id="00cfa-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="00cfa-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="00cfa-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="00cfa-121">Row index:</span></span>  <br/> |<span data-ttu-id="00cfa-122">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="00cfa-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="00cfa-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="00cfa-123">Cell index:</span></span>  <br/> |<span data-ttu-id="00cfa-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="00cfa-124">**visActionInvisible**</span></span> <br/> |
   

