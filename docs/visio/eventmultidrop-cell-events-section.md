---
title: Celda EventMultiDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822092"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="c9523-102">Celda EventMultiDrop (sección Eventos)</span><span class="sxs-lookup"><span data-stu-id="c9523-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="c9523-103">Una celda de evento que se evalúa cuando se colocan varias formas en la página de dibujo, como instancias o cuando se duplicar o pegar formas.</span><span class="sxs-lookup"><span data-stu-id="c9523-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="c9523-104">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="c9523-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="c9523-105">Para hacer referencia a la celda EventMultiDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

</span><span class="sxs-lookup"><span data-stu-id="c9523-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9523-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c9523-106">Cell name:</span></span>  <br/> |<span data-ttu-id="c9523-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="c9523-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="c9523-108">Para hacer referencia desde un programa a la celda EventMultiDrop según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:

</span><span class="sxs-lookup"><span data-stu-id="c9523-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9523-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c9523-109">Section index:</span></span>  <br/> |<span data-ttu-id="c9523-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9523-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9523-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c9523-111">Row index:</span></span>  <br/> |<span data-ttu-id="c9523-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="c9523-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="c9523-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c9523-113">Cell index:</span></span>  <br/> |<span data-ttu-id="c9523-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="c9523-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

