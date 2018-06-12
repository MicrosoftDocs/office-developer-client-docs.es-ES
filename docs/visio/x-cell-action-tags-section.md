---
title: Celda X (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: El x - coordenadas de posición en las coordenadas locales de la forma alrededor del cual se sitúa el botón de etiqueta de acción.
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823555"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="5bb3f-103">Celda X (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="5bb3f-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="5bb3f-104">La *x* -posición en coordenadas locales de la forma alrededor del cual se sitúa el botón de etiqueta de acción de la coordenada.</span><span class="sxs-lookup"><span data-stu-id="5bb3f-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bb3f-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5bb3f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5bb3f-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bb3f-106">Remarks</span></span>

<span data-ttu-id="5bb3f-107">Las celdas X e Y definen un punto en las coordenadas locales de la forma, y las celdas X Justify e Y Justify definen dónde se coloca el botón de etiqueta de acción en relación con ese punto.</span><span class="sxs-lookup"><span data-stu-id="5bb3f-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="5bb3f-108">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bb3f-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-109">Cell name:</span></span>  <br/> |<span data-ttu-id="5bb3f-110">Etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5bb3f-110">SmartTags.</span></span> <span data-ttu-id="5bb3f-111">*nombre* . X donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="5bb3f-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="5bb3f-112">*nombre* es el nombre de la fila de etiquetas de acción</span><span class="sxs-lookup"><span data-stu-id="5bb3f-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="5bb3f-113">Para obtener una referencia a la celda X por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bb3f-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-114">Section index:</span></span>  <br/> |<span data-ttu-id="5bb3f-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="5bb3f-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="5bb3f-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-116">Row index:</span></span>  <br/> |<span data-ttu-id="5bb3f-117">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5bb3f-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5bb3f-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5bb3f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5bb3f-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="5bb3f-119">**visSmartTagX**</span></span> <br/> |
   

