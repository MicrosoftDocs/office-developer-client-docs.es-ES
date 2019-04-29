---
title: Celda TagName (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417913"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="135c7-103">Celda TagName (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="135c7-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="135c7-104">Nombre de la etiqueta de acción empleado como clave para asociarla con sus acciones.</span><span class="sxs-lookup"><span data-stu-id="135c7-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="135c7-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="135c7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="135c7-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="135c7-106">Remarks</span></span>

 <span data-ttu-id="135c7-107">La celda TagName de la sección de etiquetas de acción funciona en conjunción con la celda TagName de la sección de acciones para asociar la etiqueta de acción con sus acciones.</span><span class="sxs-lookup"><span data-stu-id="135c7-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="135c7-108">Las filas de la sección de acciones también tienen una celda TagName y las filas con el mismo valor de celda TagName que esta celda definen las acciones que se deben llevar a cabo para esta etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="135c7-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="135c7-109">Para obtener una referencia a la celda TagName por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="135c7-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="135c7-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="135c7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="135c7-111">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="135c7-111">SmartTags.</span></span>  <span data-ttu-id="135c7-112">*nombre* . TagName donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="135c7-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="135c7-113">*nombre* es el nombre de la fila de la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="135c7-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="135c7-114">Para obtener una referencia a la celda TagName por su índice
 desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="135c7-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="135c7-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="135c7-115">Section index:</span></span>  <br/> |<span data-ttu-id="135c7-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="135c7-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="135c7-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="135c7-117">Row index:</span></span>  <br/> |<span data-ttu-id="135c7-118">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="135c7-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="135c7-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="135c7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="135c7-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="135c7-120">**visSmartTagName**</span></span> <br/> |
   

