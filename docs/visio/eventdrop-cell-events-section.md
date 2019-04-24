---
title: Celda EventDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Una celda de evento que se evalúa cuando se coloca una forma en la página de dibujo, ya sea como una instancia o al duplicar o pegar la forma.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351012"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="971a4-103">Celda EventDrop (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="971a4-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="971a4-104">Una celda de evento que se evalúa cuando se coloca una forma en la página de dibujo, ya sea como una instancia o al duplicar o pegar la forma.</span><span class="sxs-lookup"><span data-stu-id="971a4-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="971a4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="971a4-105">Remarks</span></span>

<span data-ttu-id="971a4-106">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="971a4-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="971a4-107">Para obtener una referencia a la celda EventDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="971a4-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="971a4-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="971a4-108">Cell name:</span></span>  <br/> | <span data-ttu-id="971a4-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="971a4-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="971a4-110">Para obtener una referencia desde un programa a la celda EventDrop por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="971a4-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="971a4-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="971a4-111">Section index:</span></span>  <br/> |<span data-ttu-id="971a4-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="971a4-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="971a4-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="971a4-113">Row index:</span></span>  <br/> |<span data-ttu-id="971a4-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="971a4-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="971a4-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="971a4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="971a4-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="971a4-116">**visEvtCellDrop**</span></span> <br/> |
   

