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
description: Una celda de evento que se evalúa cuando una posición u orientación de la página transforma (XF).
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822104"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="f76e3-103">Celda EventXFMod (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="f76e3-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="f76e3-104">Una celda de evento que se evalúa cuando se transforma ("XF") la posición u orientación de la página.</span><span class="sxs-lookup"><span data-stu-id="f76e3-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f76e3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f76e3-105">Remarks</span></span>

<span data-ttu-id="f76e3-106">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="f76e3-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="f76e3-107">Para obtener una referencia a la celda EventXFMod por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="f76e3-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f76e3-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f76e3-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f76e3-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="f76e3-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="f76e3-110">Para obtener una referencia a la celda EventXFMod por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f76e3-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f76e3-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f76e3-111">Section index:</span></span>  <br/> |<span data-ttu-id="f76e3-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f76e3-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f76e3-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f76e3-113">Row index:</span></span>  <br/> |<span data-ttu-id="f76e3-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="f76e3-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="f76e3-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f76e3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="f76e3-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="f76e3-116">**visEvtCellXFMod**</span></span> <br/> |
   

