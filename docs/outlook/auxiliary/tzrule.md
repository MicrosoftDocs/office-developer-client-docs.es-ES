---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica la información de una regla de zona horaria acerca de cuándo se inicia el horario de verano y el año en el que dicha regla de zona horaria en primer lugar en vigor.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392700"
---
# <a name="tzrule"></a><span data-ttu-id="690f8-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="690f8-103">TZRULE</span></span>

<span data-ttu-id="690f8-104">Especifica la información de una regla de zona horaria acerca de cuándo se inicia el horario de verano y el año en el que dicha regla de zona horaria en primer lugar en vigor.</span><span class="sxs-lookup"><span data-stu-id="690f8-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="690f8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="690f8-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="690f8-106">Members</span><span class="sxs-lookup"><span data-stu-id="690f8-106">Members</span></span>

<span data-ttu-id="690f8-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="690f8-107">_wFlags_</span></span>
  
> <span data-ttu-id="690f8-108">Los indicadores establecidos para este miembro identifican detalles específicos para esta regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="690f8-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="690f8-109">Los indicadores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="690f8-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="690f8-110">**TZRULE_FLAG_EFFECTIVE_TZREG** : identifica la regla que el que se debe usar actualmente.</span><span class="sxs-lookup"><span data-stu-id="690f8-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="690f8-111">Sólo una regla puede estar marcada como la regla eficaz.</span><span class="sxs-lookup"><span data-stu-id="690f8-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="690f8-112">Todas las demás reglas son únicamente con fines de comparación.</span><span class="sxs-lookup"><span data-stu-id="690f8-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="690f8-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** : en las reuniones periódicas, identifica la regla como que coincidan con la regla en [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="690f8-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="690f8-114">Esto puede usarse para detectar si se ha modificado considerablemente **PidLidTimeZoneStruct** por un cliente heredado, lo que sería en caso contrario, sin ser conscientes de la propiedad nuevo, más completa.</span><span class="sxs-lookup"><span data-stu-id="690f8-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="690f8-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="690f8-115">_stStart_</span></span>
  
> <span data-ttu-id="690f8-116">El tiempo en hora Universal coordinada (UTC) que inician la regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="690f8-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="690f8-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="690f8-117">_TZReg_</span></span>
  
> <span data-ttu-id="690f8-118">La información de zona horaria para la regla de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="690f8-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="690f8-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="690f8-119">Remarks</span></span>

<span data-ttu-id="690f8-120">Esta estructura aumenta [TZREG](tzreg.md) proporcionando información adicional que indica si las reglas de zona horaria surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="690f8-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="690f8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="690f8-121">See also</span></span>

- [<span data-ttu-id="690f8-122">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="690f8-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="690f8-123">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="690f8-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="690f8-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="690f8-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="690f8-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="690f8-125">TZDEFINITION</span></span>](tzdefinition.md)

