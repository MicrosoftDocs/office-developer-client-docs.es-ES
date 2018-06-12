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
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822077"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="31608-103">Celda EventDblClick (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="31608-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="31608-104">Una celda de evento que se evalúa cuando se hace doble clic en una forma.</span><span class="sxs-lookup"><span data-stu-id="31608-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31608-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31608-105">Remarks</span></span>

<span data-ttu-id="31608-106">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="31608-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="31608-107">Para obtener una referencia a la celda EventDblClick por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="31608-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31608-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="31608-108">Cell name:</span></span>  <br/> | <span data-ttu-id="31608-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="31608-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="31608-110">Para obtener una referencia a la celda EventDblClick por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="31608-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31608-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="31608-111">Section index:</span></span>  <br/> |<span data-ttu-id="31608-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31608-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31608-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="31608-113">Row index:</span></span>  <br/> |<span data-ttu-id="31608-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="31608-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="31608-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="31608-115">Cell index:</span></span>  <br/> |<span data-ttu-id="31608-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="31608-116">**visEvtCellDblClick**</span></span> <br/> |
   

