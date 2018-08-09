---
title: Celda Calendar (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821679"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="6c569-103">Celda Calendar (sección Campos de texto)</span><span class="sxs-lookup"><span data-stu-id="6c569-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="6c569-104">Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.</span><span class="sxs-lookup"><span data-stu-id="6c569-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c569-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c569-105">Remarks</span></span>

<span data-ttu-id="6c569-106">Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés).</span><span class="sxs-lookup"><span data-stu-id="6c569-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="6c569-107">Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6c569-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c569-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6c569-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6c569-109">Fields.Calendar [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6c569-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6c569-110">Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c569-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c569-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6c569-111">Section index:</span></span>  <br/> |<span data-ttu-id="6c569-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="6c569-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="6c569-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6c569-113">Row index:</span></span>  <br/> |<span data-ttu-id="6c569-114">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6c569-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6c569-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6c569-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6c569-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="6c569-116">**visFieldCalendar**</span></span> <br/> |
   

