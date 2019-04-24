---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa una zona horaria completa que incluye todas las reglas de turno de zona horaria histórica, actual y futura para el horario de verano.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328297"
---
# <a name="tzdefinition"></a><span data-ttu-id="73be2-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="73be2-103">TZDEFINITION</span></span>

<span data-ttu-id="73be2-104">Representa una zona horaria completa que incluye todas las reglas de turno de zona horaria histórica, actual y futura para el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="73be2-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="73be2-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="73be2-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="73be2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="73be2-106">Members</span></span>

<span data-ttu-id="73be2-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="73be2-107">_wFlags_</span></span>
  
> <span data-ttu-id="73be2-108">Indica que el nombre de clave que representa la zona horaria en el registro de Windows es válido.</span><span class="sxs-lookup"><span data-stu-id="73be2-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="73be2-109">Como cada zona horaria debe identificarse siempre mediante un nombre de clave, este miembro siempre debe tener el valor **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="73be2-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="73be2-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="73be2-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="73be2-111">El nombre de la clave de esta zona horaria en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="73be2-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="73be2-112">Este nombre no debe estar localizado.</span><span class="sxs-lookup"><span data-stu-id="73be2-112">This name must not be localized.</span></span> <span data-ttu-id="73be2-113">Tiene un tamaño máximo de **MAX_PATH**, que se define en el archivo de encabezado Windows. h del kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="73be2-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="73be2-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="73be2-114">_cRules_</span></span>
  
> <span data-ttu-id="73be2-115">Número de reglas de zona horaria para esta definición.</span><span class="sxs-lookup"><span data-stu-id="73be2-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="73be2-116">El número máximo de reglas es **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="73be2-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="73be2-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="73be2-117">_rgRules_</span></span>
  
> <span data-ttu-id="73be2-118">Una matriz de reglas que describen Cuándo se producen los turnos.</span><span class="sxs-lookup"><span data-stu-id="73be2-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73be2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73be2-119">Remarks</span></span>

<span data-ttu-id="73be2-120">Debe haber al menos una regla en *rgRules* .</span><span class="sxs-lookup"><span data-stu-id="73be2-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="73be2-121">Se considera que la primera regla de *rgRules* es la regla que se va a usar hasta que se inicie la segunda regla, independientemente de la *stStart* de la primera regla.</span><span class="sxs-lookup"><span data-stu-id="73be2-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="73be2-122">Las reglas deben ordenarse de más antigua a más reciente.</span><span class="sxs-lookup"><span data-stu-id="73be2-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="73be2-123">No se permite la superposición entre las reglas, por lo que se considera que una regla anterior finaliza cuando se inicia una nueva regla.</span><span class="sxs-lookup"><span data-stu-id="73be2-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73be2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="73be2-124">See also</span></span>

- [<span data-ttu-id="73be2-125">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="73be2-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="73be2-126">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="73be2-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="73be2-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="73be2-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

