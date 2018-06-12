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
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821985"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="1a5e6-103">Celda DisplayMode (Sección de propiedades del grupo)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="1a5e6-104">Determina cómo se muestran la forma de grupo y sus miembros.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="1a5e6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-105">**Value**</span></span>|<span data-ttu-id="1a5e6-106">**Modo de presentación**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-106">**Display Mode**</span></span>|<span data-ttu-id="1a5e6-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a5e6-108">0</span><span class="sxs-lookup"><span data-stu-id="1a5e6-108">0</span></span>  <br/> |<span data-ttu-id="1a5e6-109">Oculta la forma de grupo y el texto.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="1a5e6-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="1a5e6-111">1</span><span class="sxs-lookup"><span data-stu-id="1a5e6-111">1</span></span>  <br/> |<span data-ttu-id="1a5e6-112">Muestra la forma de grupo detrás de las formas pertenecientes.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="1a5e6-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="1a5e6-114">2</span><span class="sxs-lookup"><span data-stu-id="1a5e6-114">2</span></span>  <br/> |<span data-ttu-id="1a5e6-115">Muestra la forma de grupo delante de las formas pertenecientes.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="1a5e6-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a5e6-117">Notas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-117">Remarks</span></span>

<span data-ttu-id="1a5e6-118">También puede establecer este valor seleccionar el grupo, haciendo clic en **comportamiento** en el grupo **Diseño de formas** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccionar un modo de presentación de la lista de **datos de grupo** .</span><span class="sxs-lookup"><span data-stu-id="1a5e6-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="1a5e6-119">Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a5e6-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-120">Cell name:</span></span>  <br/> |<span data-ttu-id="1a5e6-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="1a5e6-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="1a5e6-122">Para obtener una referencia a la celda DisplayMode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a5e6-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-123">Section index:</span></span>  <br/> |<span data-ttu-id="1a5e6-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1a5e6-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-125">Row index:</span></span>  <br/> |<span data-ttu-id="1a5e6-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="1a5e6-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1a5e6-127">Cell index:</span></span>  <br/> |<span data-ttu-id="1a5e6-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="1a5e6-128">**visGroupDisplayMode**</span></span> <br/> |
   

