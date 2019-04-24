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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342584"
---
# <a name="gender"></a><span data-ttu-id="0b1e2-103">Gender</span><span class="sxs-lookup"><span data-stu-id="0b1e2-103">Gender</span></span>

  
  
<span data-ttu-id="0b1e2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b1e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b1e2-105">Especifica los valores posibles para el género de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0b1e2-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0b1e2-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="0b1e2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b1e2-107">Members</span></span>

 <span data-ttu-id="0b1e2-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-108">_genderMin_</span></span>
  
> <span data-ttu-id="0b1e2-109">El número mínimo de valores diferentes admitidos para el sexo.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="0b1e2-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="0b1e2-111">No se ha especificado el sexo del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="0b1e2-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-112">_genderFemale_</span></span>
  
> <span data-ttu-id="0b1e2-113">El usuario de mensajería es hembra.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="0b1e2-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-114">_genderMale_</span></span>
  
> <span data-ttu-id="0b1e2-115">El usuario de mensajería es macho.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="0b1e2-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-116">_genderCount_</span></span>
  
> <span data-ttu-id="0b1e2-117">El número de valores diferentes admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="0b1e2-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="0b1e2-118">_genderMax_</span></span>
  
> <span data-ttu-id="0b1e2-119">El número máximo de valores diferentes admitidos para el sexo.</span><span class="sxs-lookup"><span data-stu-id="0b1e2-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b1e2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b1e2-120">See also</span></span>



[<span data-ttu-id="0b1e2-121">Propiedad canónica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="0b1e2-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

