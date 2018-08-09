---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa una zona horaria toda incluidas todas las reglas de MAYÚS históricas, actuales y futuros zona horaria para el horario de verano.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816358"
---
# <a name="tzdefinition"></a><span data-ttu-id="44531-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="44531-103">TZDEFINITION</span></span>

<span data-ttu-id="44531-104">Representa una zona horaria toda incluidas todas las reglas de MAYÚS históricas, actuales y futuros zona horaria para el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="44531-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="44531-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="44531-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="44531-106">Members</span><span class="sxs-lookup"><span data-stu-id="44531-106">Members</span></span>

<span data-ttu-id="44531-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="44531-107">_wFlags_</span></span>
  
> <span data-ttu-id="44531-108">Indica que el nombre de la clave que representa la zona horaria en el registro de Windows es válido.</span><span class="sxs-lookup"><span data-stu-id="44531-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="44531-109">Debido a que cada zona horaria siempre debe identificarse mediante un nombre de clave, este miembro siempre debe tener el valor **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="44531-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="44531-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="44531-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="44531-111">El nombre de la clave de esta zona horaria en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="44531-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="44531-112">Este nombre no debe localizarse.</span><span class="sxs-lookup"><span data-stu-id="44531-112">This name must not be localized.</span></span> <span data-ttu-id="44531-113">Tiene un tamaño máximo de **MAX_PATH**, que se define en el windows.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="44531-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="44531-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="44531-114">_cRules_</span></span>
  
> <span data-ttu-id="44531-115">El número de reglas de zona horaria para esta definición.</span><span class="sxs-lookup"><span data-stu-id="44531-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="44531-116">El número máximo de reglas es **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="44531-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="44531-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="44531-117">_rgRules_</span></span>
  
> <span data-ttu-id="44531-118">Una matriz de reglas que describen cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="44531-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44531-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44531-119">Remarks</span></span>

<span data-ttu-id="44531-120">Debe haber al menos una regla en *rgRules* .</span><span class="sxs-lookup"><span data-stu-id="44531-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="44531-121">La primera regla en *rgRules* es considerado como la regla para utilizar hasta que se inicia la segunda regla, independientemente de la *stStart* en la primera regla.</span><span class="sxs-lookup"><span data-stu-id="44531-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="44531-122">Las reglas se deben ordenar de más antiguo a más reciente.</span><span class="sxs-lookup"><span data-stu-id="44531-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="44531-123">No hay ninguna superposición permitida entre las reglas, por lo que se considera una regla anterior para finalizar cuando se inicia una nueva regla.</span><span class="sxs-lookup"><span data-stu-id="44531-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44531-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="44531-124">See also</span></span>

- [<span data-ttu-id="44531-125">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="44531-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="44531-126">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="44531-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="44531-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="44531-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

