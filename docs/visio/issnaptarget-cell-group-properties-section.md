---
title: Celda IsSnapTarget (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Determina si las formas se ajustan en un grupo o dentro de él.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822380"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="7edd5-103">Celda IsSnapTarget (Sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="7edd5-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="7edd5-104">Determina si las formas se ajustan en un grupo o dentro de él.</span><span class="sxs-lookup"><span data-stu-id="7edd5-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="7edd5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7edd5-105">**Value**</span></span>|<span data-ttu-id="7edd5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7edd5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7edd5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7edd5-107">TRUE</span></span>  <br/> |<span data-ttu-id="7edd5-108">Habilitar el ajuste a las formas dentro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="7edd5-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="7edd5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7edd5-109">FALSE</span></span>  <br/> |<span data-ttu-id="7edd5-110">Ajustar sólo al grupo.</span><span class="sxs-lookup"><span data-stu-id="7edd5-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7edd5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7edd5-111">Remarks</span></span>

<span data-ttu-id="7edd5-112">También puede establecer este valor, seleccione el grupo, hace clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccione la casilla de verificación **se ajusta a las formas pertenecientes** .</span><span class="sxs-lookup"><span data-stu-id="7edd5-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="7edd5-113">Para obtener una referencia a la celda IsSnapTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="7edd5-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7edd5-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7edd5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7edd5-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="7edd5-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="7edd5-116">Para obtener una referencia a la celda IsSnapTarget por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7edd5-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7edd5-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7edd5-117">Section index:</span></span>  <br/> |<span data-ttu-id="7edd5-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7edd5-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7edd5-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7edd5-119">Row index:</span></span>  <br/> |<span data-ttu-id="7edd5-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="7edd5-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="7edd5-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7edd5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7edd5-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="7edd5-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

