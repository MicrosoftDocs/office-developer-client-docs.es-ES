---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588457"
---
# <a name="gender"></a><span data-ttu-id="1df9a-103">Gender</span><span class="sxs-lookup"><span data-stu-id="1df9a-103">Gender</span></span>

  
  
<span data-ttu-id="1df9a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1df9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1df9a-105">Especifica los valores posibles para el género de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1df9a-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1df9a-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1df9a-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="1df9a-107">Members</span><span class="sxs-lookup"><span data-stu-id="1df9a-107">Members</span></span>

 <span data-ttu-id="1df9a-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="1df9a-108">_genderMin_</span></span>
  
> <span data-ttu-id="1df9a-109">El número mínimo de diferentes valores admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="1df9a-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1df9a-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="1df9a-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="1df9a-111">No se especifica el género para el usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1df9a-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="1df9a-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="1df9a-112">_genderFemale_</span></span>
  
> <span data-ttu-id="1df9a-113">El usuario de mensajería es femenino.</span><span class="sxs-lookup"><span data-stu-id="1df9a-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="1df9a-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="1df9a-114">_genderMale_</span></span>
  
> <span data-ttu-id="1df9a-115">El usuario de mensajería es masculino.</span><span class="sxs-lookup"><span data-stu-id="1df9a-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="1df9a-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="1df9a-116">_genderCount_</span></span>
  
> <span data-ttu-id="1df9a-117">El número de valores diferentes compatibles para el género.</span><span class="sxs-lookup"><span data-stu-id="1df9a-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1df9a-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="1df9a-118">_genderMax_</span></span>
  
> <span data-ttu-id="1df9a-119">El número máximo de diferentes valores admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="1df9a-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1df9a-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1df9a-120">See also</span></span>



[<span data-ttu-id="1df9a-121">Propiedad canónica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="1df9a-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

