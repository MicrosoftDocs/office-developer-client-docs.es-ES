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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423877"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="25276-103">Celda Invisible (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="25276-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="25276-104">Indica si la acción está visible en el menú contextual o de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="25276-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="25276-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="25276-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="25276-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="25276-106">**Value**</span></span>|<span data-ttu-id="25276-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25276-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25276-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="25276-108">TRUE</span></span>  <br/> |<span data-ttu-id="25276-109">La acción no está visible en el menú.</span><span class="sxs-lookup"><span data-stu-id="25276-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="25276-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="25276-110">FALSE</span></span>  <br/> |<span data-ttu-id="25276-111">La acción está visible en el menú (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="25276-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25276-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25276-112">Remarks</span></span>

<span data-ttu-id="25276-113">Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="25276-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25276-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="25276-114">Cell name:</span></span>  <br/> |<span data-ttu-id="25276-115">Acciones.</span><span class="sxs-lookup"><span data-stu-id="25276-115">Actions.</span></span> <span data-ttu-id="25276-116">*nombre*  . Invisiblewhere Actions.</span><span class="sxs-lookup"><span data-stu-id="25276-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="25276-117">*es*  el nombre de la fila Actions</span><span class="sxs-lookup"><span data-stu-id="25276-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="25276-118">Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="25276-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25276-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="25276-119">Section index:</span></span>  <br/> |<span data-ttu-id="25276-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="25276-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="25276-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="25276-121">Row index:</span></span>  <br/> |<span data-ttu-id="25276-122">**visRowAction**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="25276-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="25276-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="25276-123">Cell index:</span></span>  <br/> |<span data-ttu-id="25276-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="25276-124">**visActionInvisible**</span></span> <br/> |
   

