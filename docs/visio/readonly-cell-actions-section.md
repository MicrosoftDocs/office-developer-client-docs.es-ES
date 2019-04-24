---
title: Celda ReadOnly (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359993"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="77976-103">Celda ReadOnly (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="77976-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="77976-104">Controla si la acción de un menú contextual o de etiqueta de acción es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="77976-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="77976-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="77976-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="77976-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="77976-106">**Value**</span></span>|<span data-ttu-id="77976-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77976-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77976-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="77976-108">TRUE</span></span>  <br/> |<span data-ttu-id="77976-109">La acción aparece en el menú pero es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="77976-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="77976-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="77976-110">FALSE</span></span>  <br/> |<span data-ttu-id="77976-111">La acción aparece en el menú y se puede seleccionar (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="77976-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77976-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77976-112">Remarks</span></span>

<span data-ttu-id="77976-113">Cuando una acción es de sólo lectura, aparece en el menú contextual o de etiqueta de acción pero no se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="77976-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="77976-114">No está atenuada, sino que aparece sobre un fondo coloreado, como una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="77976-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="77976-115">Para hacer que el elemento del menú aparezca atenuado, utilice la celda Disabled.</span><span class="sxs-lookup"><span data-stu-id="77976-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="77976-116">Para obtener una referencia a la celda ReadOnly por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="77976-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77976-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="77976-117">Cell name:</span></span>  <br/> |<span data-ttu-id="77976-118">Actividades.</span><span class="sxs-lookup"><span data-stu-id="77976-118">Actions.</span></span> <span data-ttu-id="77976-119">*nombre* . Acciones Readonlydonde.</span><span class="sxs-lookup"><span data-stu-id="77976-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="77976-120">*nombre* es el nombre de la fila de acciones.</span><span class="sxs-lookup"><span data-stu-id="77976-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="77976-121">Para obtener una referencia desde un programa a la celda ReadOnly por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="77976-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77976-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="77976-122">Section index:</span></span>  <br/> |<span data-ttu-id="77976-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="77976-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="77976-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="77976-124">Row index:</span></span>  <br/> |<span data-ttu-id="77976-125">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="77976-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="77976-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="77976-126">Cell index:</span></span>  <br/> |<span data-ttu-id="77976-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="77976-127">**visActionReadOnly**</span></span> <br/> |
   

