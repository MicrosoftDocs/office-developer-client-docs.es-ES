---
title: Celda EventXFMod (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Una celda de evento que se evalúa cuando se transforma la posición o la orientación de una forma en la página (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418536"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="e2456-103">Celda EventXFMod (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="e2456-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="e2456-104">Una celda de evento que se evalúa cuando se transforma ("XF") la posición u orientación de la página.</span><span class="sxs-lookup"><span data-stu-id="e2456-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2456-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2456-105">Remarks</span></span>

<span data-ttu-id="e2456-106">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="e2456-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="e2456-107">Para obtener una referencia a la celda EventXFMod por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e2456-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2456-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e2456-108">Cell name:</span></span>  <br/> | <span data-ttu-id="e2456-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="e2456-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="e2456-110">Para obtener una referencia desde un programa a la celda EventXFMod por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2456-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2456-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e2456-111">Section index:</span></span>  <br/> |<span data-ttu-id="e2456-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2456-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e2456-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e2456-113">Row index:</span></span>  <br/> |<span data-ttu-id="e2456-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="e2456-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="e2456-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e2456-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e2456-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="e2456-116">**visEvtCellXFMod**</span></span> <br/> |
   

