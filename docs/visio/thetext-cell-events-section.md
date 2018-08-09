---
title: Celda TheText (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Celda de evento que se evalúa cuando cambia el texto o la composición del texto de una forma.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823402"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="ad192-103">Celda TheText (sección Eventos)</span><span class="sxs-lookup"><span data-stu-id="ad192-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="ad192-104">Celda de evento que se evalúa cuando cambia el texto o la composición del texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="ad192-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad192-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad192-105">Remarks</span></span>

<span data-ttu-id="ad192-p101">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula. Puede utilizar la celda TheText para activar cálculos, por ejemplo, para volver a calcular el ancho y el alto del texto con las funciones TEXTWIDTH( ) y TEXTHEIGHT( ).</span><span class="sxs-lookup"><span data-stu-id="ad192-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="ad192-108">Para obtener una referencia a la celda TheText por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ad192-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad192-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ad192-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ad192-110">TheText</span><span class="sxs-lookup"><span data-stu-id="ad192-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="ad192-111">Para obtener una referencia desde un programa a la celda TheText por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad192-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad192-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ad192-112">Section index:</span></span>  <br/> |<span data-ttu-id="ad192-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad192-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad192-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ad192-114">Row index:</span></span>  <br/> |<span data-ttu-id="ad192-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="ad192-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="ad192-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ad192-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ad192-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="ad192-117">**visEvtCellTheText**</span></span> <br/> |
   

