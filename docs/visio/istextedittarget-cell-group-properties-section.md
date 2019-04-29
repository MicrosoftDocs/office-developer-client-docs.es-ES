---
title: Celda IsTextEditTarget (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Determina las asignaciones de texto para un grupo.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432649"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="a1091-103">Celda IsTextEditTarget (Sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="a1091-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="a1091-104">Determina las asignaciones de texto para un grupo.</span><span class="sxs-lookup"><span data-stu-id="a1091-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="a1091-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a1091-105">**Value**</span></span>|<span data-ttu-id="a1091-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1091-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1091-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1091-107">TRUE</span></span>  <br/> |<span data-ttu-id="a1091-108">El texto se agrega a la forma del grupo.</span><span class="sxs-lookup"><span data-stu-id="a1091-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="a1091-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1091-109">FALSE</span></span>  <br/> |<span data-ttu-id="a1091-110">El texto se agrega a la forma en el grupo en la parte superior del orden de apilamiento.</span><span class="sxs-lookup"><span data-stu-id="a1091-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1091-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1091-111">Remarks</span></span>

<span data-ttu-id="a1091-112">También puede ajustar este valor si selecciona un grupo, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, activa la casilla **Modificar el texto del grupo**.</span><span class="sxs-lookup"><span data-stu-id="a1091-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="a1091-p101">Los grupos creados con versiones anteriores a Visio 2000 tienen el valor predeterminado FALSE. A partir de la versión 2000 de Visio, el valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="a1091-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="a1091-115">Para obtener una referencia a la celda IsTextEditTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a1091-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1091-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a1091-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a1091-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="a1091-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="a1091-118">Para obtener una referencia desde un programa a la celda IsTextEditTarget por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1091-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1091-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a1091-119">Section index:</span></span>  <br/> |<span data-ttu-id="a1091-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1091-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a1091-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a1091-121">Row index:</span></span>  <br/> |<span data-ttu-id="a1091-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="a1091-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="a1091-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a1091-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a1091-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="a1091-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

