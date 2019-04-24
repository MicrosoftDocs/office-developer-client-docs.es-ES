---
title: Celda DisplayMode (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o siempre.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332735"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="118ef-103">Celda DisplayMode (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="118ef-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="118ef-104">Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o siempre.</span><span class="sxs-lookup"><span data-stu-id="118ef-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="118ef-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="118ef-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="118ef-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="118ef-106">**Value**</span></span>|<span data-ttu-id="118ef-107">**Modo de presentación**</span><span class="sxs-lookup"><span data-stu-id="118ef-107">**Display Mode**</span></span>|<span data-ttu-id="118ef-108">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="118ef-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="118ef-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="118ef-109">0</span></span>  <br/> | <span data-ttu-id="118ef-110">Aparece cuando se pausa el mouse sobre la etiqueta (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="118ef-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="118ef-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="118ef-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="118ef-112">1</span><span class="sxs-lookup"><span data-stu-id="118ef-112">1</span></span>  <br/> | <span data-ttu-id="118ef-113">Aparece mientras está seleccionada la forma.</span><span class="sxs-lookup"><span data-stu-id="118ef-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="118ef-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="118ef-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="118ef-115">segundo</span><span class="sxs-lookup"><span data-stu-id="118ef-115">2</span></span>  <br/> | <span data-ttu-id="118ef-116">Aparece siempre.</span><span class="sxs-lookup"><span data-stu-id="118ef-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="118ef-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="118ef-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="118ef-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="118ef-118">Remarks</span></span>

<span data-ttu-id="118ef-119">Las etiquetas de acción no aparecen en las versiones impresas ni en las publicaciones.</span><span class="sxs-lookup"><span data-stu-id="118ef-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="118ef-120">Si se define una etiqueta de acción para una página y esta celda contiene el valor 1, la etiqueta no aparecerá nunca, ya que no se puede seleccionar una página.</span><span class="sxs-lookup"><span data-stu-id="118ef-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="118ef-121">Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="118ef-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="118ef-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="118ef-122">Cell name:</span></span>  <br/> | <span data-ttu-id="118ef-123">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="118ef-123">SmartTags.</span></span>  <span data-ttu-id="118ef-124">*nombre* . DisplayMode donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="118ef-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="118ef-125">*nombre* es el nombre de la fila de la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="118ef-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="118ef-126">Para obtener una referencia a la celda DisplayMode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="118ef-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="118ef-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="118ef-127">Section index:</span></span>  <br/> |<span data-ttu-id="118ef-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="118ef-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="118ef-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="118ef-129">Row index:</span></span>  <br/> |<span data-ttu-id="118ef-130">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="118ef-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="118ef-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="118ef-131">Cell index:</span></span>  <br/> |<span data-ttu-id="118ef-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="118ef-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

