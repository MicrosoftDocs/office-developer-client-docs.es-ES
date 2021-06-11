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
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421448"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="b9ad3-103">Celda IsSnapTarget (sección de propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="b9ad3-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="b9ad3-104">Determina si las formas se ajustan en un grupo o dentro de él.</span><span class="sxs-lookup"><span data-stu-id="b9ad3-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="b9ad3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b9ad3-105">**Value**</span></span>|<span data-ttu-id="b9ad3-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9ad3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9ad3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9ad3-107">TRUE</span></span>  <br/> |<span data-ttu-id="b9ad3-108">Habilitar el ajuste a las formas dentro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="b9ad3-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="b9ad3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9ad3-109">FALSE</span></span>  <br/> |<span data-ttu-id="b9ad3-110">Ajustar sólo al grupo.</span><span class="sxs-lookup"><span data-stu-id="b9ad3-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9ad3-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9ad3-111">Remarks</span></span>

<span data-ttu-id="b9ad3-112">También puede ajustar este valor si selecciona un grupo, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, activa la casilla **Ajustar a las formas pertenecientes**.</span><span class="sxs-lookup"><span data-stu-id="b9ad3-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="b9ad3-113">Para obtener una referencia a la celda IsSnapTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9ad3-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b9ad3-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="b9ad3-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="b9ad3-116">Para obtener una referencia desde un programa a la celda IsSnapTarget por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9ad3-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-117">Section index:</span></span>  <br/> |<span data-ttu-id="b9ad3-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9ad3-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b9ad3-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-119">Row index:</span></span>  <br/> |<span data-ttu-id="b9ad3-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="b9ad3-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="b9ad3-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b9ad3-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b9ad3-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="b9ad3-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

