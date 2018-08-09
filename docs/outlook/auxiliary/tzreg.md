---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el tiempo de horario de verano, cuando se produce la devolución a la hora estándar y es el turno de verano de cuántas horas.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816348"
---
# <a name="tzreg"></a><span data-ttu-id="c6872-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="c6872-103">TZREG</span></span>

<span data-ttu-id="c6872-104">Define cuándo se inicia el tiempo de horario de verano, cuando se produce la devolución a la hora estándar y es el turno de verano de cuántas horas.</span><span class="sxs-lookup"><span data-stu-id="c6872-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c6872-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c6872-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="c6872-106">Members</span><span class="sxs-lookup"><span data-stu-id="c6872-106">Members</span></span>

<span data-ttu-id="c6872-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="c6872-107">_lBias_</span></span>
  
> <span data-ttu-id="c6872-108">El desplazamiento de la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="c6872-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="c6872-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="c6872-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="c6872-110">Especifica el desplazamiento de inclinación durante el horario estándar.</span><span class="sxs-lookup"><span data-stu-id="c6872-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="c6872-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="c6872-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="c6872-112">Especifica el desplazamiento de inclinación durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c6872-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="c6872-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="c6872-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="c6872-114">El tiempo para cambiar a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c6872-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="c6872-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="c6872-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="c6872-116">El tiempo para cambiar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c6872-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6872-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6872-117">Remarks</span></span>

<span data-ttu-id="c6872-118">Esta estructura es similar a **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="c6872-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="c6872-119">Ésta es la estructura usada por los clientes heredados para almacenar la información de zona horaria de reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="c6872-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6872-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6872-120">See also</span></span>

- [<span data-ttu-id="c6872-121">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="c6872-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="c6872-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="c6872-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="c6872-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="c6872-123">TZRULE</span></span>](tzrule.md)

