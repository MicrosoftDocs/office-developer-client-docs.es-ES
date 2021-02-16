---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica información para una regla de zona horaria sobre cuándo se inicia el horario de verano y el año en que esa regla de zona horaria primero surte efecto.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328619"
---
# <a name="tzrule"></a><span data-ttu-id="b5df0-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="b5df0-103">TZRULE</span></span>

<span data-ttu-id="b5df0-104">Especifica información para una regla de zona horaria sobre cuándo se inicia el horario de verano y el año en que esa regla de zona horaria primero surte efecto.</span><span class="sxs-lookup"><span data-stu-id="b5df0-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b5df0-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b5df0-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="b5df0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5df0-106">Members</span></span>

<span data-ttu-id="b5df0-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="b5df0-107">_wFlags_</span></span>
  
> <span data-ttu-id="b5df0-108">Las marcas establecidas para este miembro identifican detalles específicos para esta regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b5df0-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="b5df0-109">Las marcas posibles son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5df0-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="b5df0-110">**TZRULE_FLAG_EFFECTIVE_TZREG:** identifica la regla como la que debe usarse actualmente.</span><span class="sxs-lookup"><span data-stu-id="b5df0-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="b5df0-111">Solo se puede marcar una regla como la regla efectiva.</span><span class="sxs-lookup"><span data-stu-id="b5df0-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="b5df0-112">Todas las demás reglas son solo para fines de comparación.</span><span class="sxs-lookup"><span data-stu-id="b5df0-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="b5df0-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG:** en reuniones periódicas, identifica la regla como que coincide con la regla en [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5df0-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="b5df0-114">Esto se puede usar para detectar si un cliente heredado ha modificado significativamente **PidLidTimeZoneStruct,** lo que de lo contrario no sería consciente de la nueva propiedad más completa.</span><span class="sxs-lookup"><span data-stu-id="b5df0-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="b5df0-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="b5df0-115">_stStart_</span></span>
  
> <span data-ttu-id="b5df0-116">La hora en hora universal coordinada (UTC) que inició la regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b5df0-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="b5df0-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="b5df0-117">_TZReg_</span></span>
  
> <span data-ttu-id="b5df0-118">La información de zona horaria de la regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b5df0-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5df0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5df0-119">Remarks</span></span>

<span data-ttu-id="b5df0-120">Esta estructura aumenta [TZREG](tzreg.md) proporcionando información adicional que indica cuándo surte efecto la regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b5df0-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5df0-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5df0-121">See also</span></span>

- [<span data-ttu-id="b5df0-122">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="b5df0-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="b5df0-123">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="b5df0-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="b5df0-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="b5df0-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="b5df0-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b5df0-125">TZDEFINITION</span></span>](tzdefinition.md)

