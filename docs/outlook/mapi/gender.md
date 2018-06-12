---
title: Género
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816908"
---
# <a name="gender"></a><span data-ttu-id="0a22c-103">Género</span><span class="sxs-lookup"><span data-stu-id="0a22c-103">Gender</span></span>

  
  
<span data-ttu-id="0a22c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a22c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a22c-105">Especifica los valores posibles para el género de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0a22c-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0a22c-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0a22c-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="0a22c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0a22c-107">Members</span></span>

 <span data-ttu-id="0a22c-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="0a22c-108">_genderMin_</span></span>
  
> <span data-ttu-id="0a22c-109">El número mínimo de diferentes valores admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="0a22c-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="0a22c-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="0a22c-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="0a22c-111">No se especifica el género para el usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0a22c-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="0a22c-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="0a22c-112">_genderFemale_</span></span>
  
> <span data-ttu-id="0a22c-113">El usuario de mensajería es femenino.</span><span class="sxs-lookup"><span data-stu-id="0a22c-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="0a22c-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="0a22c-114">_genderMale_</span></span>
  
> <span data-ttu-id="0a22c-115">El usuario de mensajería es masculino.</span><span class="sxs-lookup"><span data-stu-id="0a22c-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="0a22c-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="0a22c-116">_genderCount_</span></span>
  
> <span data-ttu-id="0a22c-117">El número de valores diferentes compatibles para el género.</span><span class="sxs-lookup"><span data-stu-id="0a22c-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="0a22c-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="0a22c-118">_genderMax_</span></span>
  
> <span data-ttu-id="0a22c-119">El número máximo de diferentes valores admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="0a22c-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a22c-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="0a22c-120">See also</span></span>



[<span data-ttu-id="0a22c-121">Propiedad canónico PidTagGender</span><span class="sxs-lookup"><span data-stu-id="0a22c-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

