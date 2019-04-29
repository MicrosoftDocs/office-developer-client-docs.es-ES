---
title: Celda EventMultiDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416723"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="8c879-102">Celda EventMultiDrop (Sección de eventos)</span><span class="sxs-lookup"><span data-stu-id="8c879-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="8c879-103">Una celda de evento que se evalúa cuando se colocan varias formas en la página de dibujo, ya sea como instancias o cuando se duplican o se pegan formas.</span><span class="sxs-lookup"><span data-stu-id="8c879-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="8c879-104">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="8c879-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="8c879-105">Para hacer referencia a la celda EventMultiDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8c879-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c879-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8c879-106">Cell name:</span></span>  <br/> |<span data-ttu-id="8c879-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="8c879-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="8c879-108">Para hacer referencia desde un programa a la celda EventMultiDrop según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8c879-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c879-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8c879-109">Section index:</span></span>  <br/> |<span data-ttu-id="8c879-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c879-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8c879-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8c879-111">Row index:</span></span>  <br/> |<span data-ttu-id="8c879-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="8c879-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="8c879-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8c879-113">Cell index:</span></span>  <br/> |<span data-ttu-id="8c879-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="8c879-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

