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
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337502"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="0a73a-103">Celda Calendar (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="0a73a-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="0a73a-104">Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.</span><span class="sxs-lookup"><span data-stu-id="0a73a-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a73a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a73a-105">Remarks</span></span>

<span data-ttu-id="0a73a-106">Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés).</span><span class="sxs-lookup"><span data-stu-id="0a73a-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="0a73a-107">Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0a73a-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a73a-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0a73a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="0a73a-109">Fields. Calendar [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0a73a-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0a73a-110">Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a73a-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a73a-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0a73a-111">Section index:</span></span>  <br/> |<span data-ttu-id="0a73a-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0a73a-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="0a73a-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0a73a-113">Row index:</span></span>  <br/> |<span data-ttu-id="0a73a-114">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0a73a-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0a73a-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0a73a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0a73a-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="0a73a-116">**visFieldCalendar**</span></span> <br/> |
   

