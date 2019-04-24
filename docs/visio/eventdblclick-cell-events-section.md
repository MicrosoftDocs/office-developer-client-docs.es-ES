---
title: Celda EventDblClick (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Una celda de evento que se evalúa cuando se hace doble clic en una forma.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337173"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="12a0d-103">Celda EventDblClick (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="12a0d-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="12a0d-104">Una celda de evento que se evalúa cuando se hace doble clic en una forma.</span><span class="sxs-lookup"><span data-stu-id="12a0d-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12a0d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12a0d-105">Remarks</span></span>

<span data-ttu-id="12a0d-106">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="12a0d-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="12a0d-107">Para obtener una referencia a la celda EventDblClick por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="12a0d-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12a0d-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="12a0d-108">Cell name:</span></span>  <br/> | <span data-ttu-id="12a0d-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="12a0d-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="12a0d-110">Para obtener una referencia desde un programa a la celda EventDblClick por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="12a0d-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12a0d-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="12a0d-111">Section index:</span></span>  <br/> |<span data-ttu-id="12a0d-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="12a0d-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="12a0d-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="12a0d-113">Row index:</span></span>  <br/> |<span data-ttu-id="12a0d-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="12a0d-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="12a0d-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="12a0d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="12a0d-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="12a0d-116">**visEvtCellDblClick**</span></span> <br/> |
   

