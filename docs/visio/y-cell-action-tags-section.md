---
title: Celda Y (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: La posición de la coordenada y de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.
ms.openlocfilehash: 02797a849a262cb506f4617aadaccedabccdab77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430227"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="1ebf3-103">Celda Y (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="1ebf3-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="1ebf3-104">La posición de la coordenada *y* de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1ebf3-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1ebf3-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ebf3-106">Remarks</span></span>

<span data-ttu-id="1ebf3-107">Las celdas X e Y definen un punto en las coordenadas locales de la forma, y las celdas X Justify e Y Justify definen dónde se coloca el botón de etiqueta de acción en relación con ese punto.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="1ebf3-108">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ebf3-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1ebf3-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-110">SmartTags.</span></span>  <span data-ttu-id="1ebf3-111">*nombre* . Y donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="1ebf3-112">*nombre* es el nombre de la fila de la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="1ebf3-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="1ebf3-113">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ebf3-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-114">Section index:</span></span>  <br/> |<span data-ttu-id="1ebf3-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="1ebf3-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="1ebf3-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-116">Row index:</span></span>  <br/> |<span data-ttu-id="1ebf3-117">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1ebf3-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1ebf3-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1ebf3-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1ebf3-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="1ebf3-119">**visSmartTagY**</span></span> <br/> |
   

