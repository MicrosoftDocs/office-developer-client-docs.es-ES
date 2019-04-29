---
title: Celda DisplayMode (Sección de propiedades del grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Determina cómo se muestran la forma de grupo y sus miembros.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413188"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="8da86-103">Celda DisplayMode (Sección de propiedades del grupo)</span><span class="sxs-lookup"><span data-stu-id="8da86-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="8da86-104">Determina cómo se muestran la forma de grupo y sus miembros.</span><span class="sxs-lookup"><span data-stu-id="8da86-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="8da86-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8da86-105">**Value**</span></span>|<span data-ttu-id="8da86-106">**Modo de presentación**</span><span class="sxs-lookup"><span data-stu-id="8da86-106">**Display Mode**</span></span>|<span data-ttu-id="8da86-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8da86-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8da86-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="8da86-108">0</span></span>  <br/> |<span data-ttu-id="8da86-109">Oculta la forma de grupo y el texto.</span><span class="sxs-lookup"><span data-stu-id="8da86-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="8da86-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="8da86-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="8da86-111">1</span><span class="sxs-lookup"><span data-stu-id="8da86-111">1</span></span>  <br/> |<span data-ttu-id="8da86-112">Muestra la forma de grupo detrás de las formas pertenecientes.</span><span class="sxs-lookup"><span data-stu-id="8da86-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="8da86-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="8da86-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="8da86-114">segundo</span><span class="sxs-lookup"><span data-stu-id="8da86-114">2</span></span>  <br/> |<span data-ttu-id="8da86-115">Muestra la forma de grupo delante de las formas pertenecientes.</span><span class="sxs-lookup"><span data-stu-id="8da86-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="8da86-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="8da86-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8da86-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8da86-117">Remarks</span></span>

<span data-ttu-id="8da86-118">Para establecer este valor, también puede seleccionar el grupo, hacer clic en **comportamiento** en el grupo **diseño de formas** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccionar un modo de presentación de la lista **datos del grupo** .</span><span class="sxs-lookup"><span data-stu-id="8da86-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="8da86-119">Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="8da86-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8da86-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8da86-120">Cell name:</span></span>  <br/> |<span data-ttu-id="8da86-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="8da86-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="8da86-122">Para obtener una referencia a la celda DisplayMode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8da86-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8da86-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8da86-123">Section index:</span></span>  <br/> |<span data-ttu-id="8da86-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8da86-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8da86-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8da86-125">Row index:</span></span>  <br/> |<span data-ttu-id="8da86-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="8da86-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="8da86-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8da86-127">Cell index:</span></span>  <br/> |<span data-ttu-id="8da86-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="8da86-128">**visGroupDisplayMode**</span></span> <br/> |
   

