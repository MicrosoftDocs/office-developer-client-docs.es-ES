---
title: Celda SortKey (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823316"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="dcdb5-103">Celda SortKey (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="dcdb5-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="dcdb5-104">Un número que determina el orden de las acciones que aparecen en un menú contextual o de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="dcdb5-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dcdb5-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="dcdb5-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dcdb5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcdb5-106">Remarks</span></span>

<span data-ttu-id="dcdb5-p101">Las acciones aparecen en un menú contextual o de etiqueta de acción ordenadas de menor a mayor, con los números menores en la parte superior del menú. Si dos filas de acciones tienen el mismo valor para la celda SortKey, el orden queda determinado por el orden físico de la fila. El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="dcdb5-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="dcdb5-110">Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcdb5-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-111">Cell name:</span></span>  <br/> |<span data-ttu-id="dcdb5-112">Acciones.</span><span class="sxs-lookup"><span data-stu-id="dcdb5-112">Actions.</span></span> <span data-ttu-id="dcdb5-113">*nombre* . Acciones de SortKeywhere.</span><span class="sxs-lookup"><span data-stu-id="dcdb5-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="dcdb5-114">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="dcdb5-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dcdb5-115">Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcdb5-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-116">Section index:</span></span>  <br/> |<span data-ttu-id="dcdb5-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dcdb5-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dcdb5-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-118">Row index:</span></span>  <br/> |<span data-ttu-id="dcdb5-119">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dcdb5-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dcdb5-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dcdb5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dcdb5-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="dcdb5-121">**visActionSortKey**</span></span> <br/> |
   

