---
title: Celda Calendar (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Determina el calendario utilizado cuando una fórmula de celda contiene información de fecha.
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821689"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="99764-103">Celda Calendar (sección Varios)</span><span class="sxs-lookup"><span data-stu-id="99764-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="99764-104">Determina el calendario utilizado cuando una fórmula de celda contiene información de fecha.</span><span class="sxs-lookup"><span data-stu-id="99764-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99764-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99764-105">Remarks</span></span>

<span data-ttu-id="99764-106">Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés).</span><span class="sxs-lookup"><span data-stu-id="99764-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="99764-107">Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="99764-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99764-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="99764-108">Cell name:</span></span>  <br/> | <span data-ttu-id="99764-109">Calendar</span><span class="sxs-lookup"><span data-stu-id="99764-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="99764-110">Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="99764-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99764-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="99764-111">Section index:</span></span>  <br/> |<span data-ttu-id="99764-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99764-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="99764-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="99764-113">Row index:</span></span>  <br/> |<span data-ttu-id="99764-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="99764-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="99764-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="99764-115">Cell index:</span></span>  <br/> |<span data-ttu-id="99764-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="99764-116">**visObjCalendar**</span></span> <br/> |
   

