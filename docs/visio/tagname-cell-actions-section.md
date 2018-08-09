---
title: Celda TagName (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823373"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="3fdd7-103">Celda TagName (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="3fdd7-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="3fdd7-104">Contiene el nombre de la etiqueta de acción a la que está asociada esta acción.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3fdd7-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3fdd7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fdd7-106">Remarks</span></span>

<span data-ttu-id="3fdd7-107">Mediante la celda TagName de la sección de acciones y la celda TagName de la sección de etiquetas de acción se asocian etiquetas de acción y acciones.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="3fdd7-108">Si la celda TagName de una fila de acciones está en blanco, la acción aparece en un menú contextual, no en un menú de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="3fdd7-109">Si un valor de la celda TagName de la fila de acciones coincide con el valor de la celda TagName de una fila de etiquetas inteligentes, la acción aparece en el menú de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="3fdd7-110">Si la celda TagName de una acción tiene un valor, pero no coincide con el valor de TagName de ninguna fila de etiqueta, esa acción no aparecen en los menús de etiqueta de acción o los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="3fdd7-111">Si varias filas de etiquetas inteligentes tienen el mismo valor de TagName, todas mostrarán las mismas acciones.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="3fdd7-112">Para obtener una referencia a la celda TagName por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fdd7-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3fdd7-114">Acciones.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-114">Actions.</span></span> <span data-ttu-id="3fdd7-115">*nombre* . Acciones de TagNamewhere.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="3fdd7-116">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="3fdd7-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="3fdd7-117">Para obtener una referencia desde un programa a la celda TagName por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fdd7-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-118">Section index:</span></span>  <br/> |<span data-ttu-id="3fdd7-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="3fdd7-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="3fdd7-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-120">Row index:</span></span>  <br/> |<span data-ttu-id="3fdd7-121">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3fdd7-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3fdd7-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3fdd7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3fdd7-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="3fdd7-123">**visActionTagName**</span></span> <br/> |
   

