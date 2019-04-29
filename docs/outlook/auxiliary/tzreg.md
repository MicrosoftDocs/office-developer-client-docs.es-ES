---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el horario de verano, Cuándo se produce el cambio de hora estándar y cuántas horas tiene el horario de verano.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419369"
---
# <a name="tzreg"></a><span data-ttu-id="63be9-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="63be9-103">TZREG</span></span>

<span data-ttu-id="63be9-104">Define cuándo se inicia el horario de verano, Cuándo se produce el cambio de hora estándar y cuántas horas tiene el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="63be9-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="63be9-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="63be9-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="63be9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="63be9-106">Members</span></span>

<span data-ttu-id="63be9-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="63be9-107">_lBias_</span></span>
  
> <span data-ttu-id="63be9-108">El desplazamiento de la hora media de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="63be9-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="63be9-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="63be9-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="63be9-110">Desplazamiento respecto a la inclinación en el horario estándar.</span><span class="sxs-lookup"><span data-stu-id="63be9-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="63be9-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="63be9-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="63be9-112">Desplazamiento respecto a bias durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="63be9-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="63be9-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="63be9-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="63be9-114">Hora a la que se va a cambiar a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="63be9-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="63be9-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="63be9-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="63be9-116">Hora para cambiar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="63be9-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63be9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63be9-117">Remarks</span></span>

<span data-ttu-id="63be9-118">Esta estructura es similar a **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="63be9-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="63be9-119">Esta es la estructura que usan los clientes heredados para almacenar la información de zona horaria de las reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="63be9-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63be9-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="63be9-120">See also</span></span>

- [<span data-ttu-id="63be9-121">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="63be9-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="63be9-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="63be9-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="63be9-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="63be9-123">TZRULE</span></span>](tzrule.md)

