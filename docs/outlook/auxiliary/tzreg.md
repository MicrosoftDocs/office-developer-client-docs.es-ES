---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el horario de verano, cuándo se produce la vuelta a la hora estándar y cuántas horas es el turno de verano.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419369"
---
# <a name="tzreg"></a><span data-ttu-id="c2398-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="c2398-103">TZREG</span></span>

<span data-ttu-id="c2398-104">Define cuándo se inicia el horario de verano, cuándo se produce la vuelta al horario estándar y cuántas horas es el turno de verano.</span><span class="sxs-lookup"><span data-stu-id="c2398-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c2398-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c2398-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="c2398-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2398-106">Members</span></span>

<span data-ttu-id="c2398-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="c2398-107">_lBias_</span></span>
  
> <span data-ttu-id="c2398-108">Desplazamiento de la hora media de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="c2398-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="c2398-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="c2398-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="c2398-110">Desplazamiento de la inclinación durante el tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="c2398-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="c2398-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="c2398-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="c2398-112">Desplazamiento de la diferencia durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c2398-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="c2398-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="c2398-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="c2398-114">Tiempo para cambiar a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c2398-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="c2398-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="c2398-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="c2398-116">Hora para cambiar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c2398-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2398-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2398-117">Remarks</span></span>

<span data-ttu-id="c2398-118">Esta estructura es similar a **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="c2398-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="c2398-119">Esta es la estructura que usan los clientes heredados para almacenar información de zona horaria para reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="c2398-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2398-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2398-120">See also</span></span>

- [<span data-ttu-id="c2398-121">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="c2398-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="c2398-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="c2398-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="c2398-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="c2398-123">TZRULE</span></span>](tzrule.md)

