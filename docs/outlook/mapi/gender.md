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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428651"
---
# <a name="gender"></a><span data-ttu-id="71d95-103">Gender</span><span class="sxs-lookup"><span data-stu-id="71d95-103">Gender</span></span>

  
  
<span data-ttu-id="71d95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71d95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71d95-105">Especifica los valores posibles para el género de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="71d95-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="71d95-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="71d95-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="71d95-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="71d95-107">Members</span></span>

 <span data-ttu-id="71d95-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="71d95-108">_genderMin_</span></span>
  
> <span data-ttu-id="71d95-109">Número mínimo de valores diferentes admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="71d95-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="71d95-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="71d95-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="71d95-111">El género no se especifica para el usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="71d95-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="71d95-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="71d95-112">_genderFemale_</span></span>
  
> <span data-ttu-id="71d95-113">El usuario de mensajería es mujer.</span><span class="sxs-lookup"><span data-stu-id="71d95-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="71d95-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="71d95-114">_genderMale_</span></span>
  
> <span data-ttu-id="71d95-115">El usuario de mensajería es varón.</span><span class="sxs-lookup"><span data-stu-id="71d95-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="71d95-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="71d95-116">_genderCount_</span></span>
  
> <span data-ttu-id="71d95-117">Número de valores diferentes admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="71d95-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="71d95-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="71d95-118">_genderMax_</span></span>
  
> <span data-ttu-id="71d95-119">El número máximo de valores diferentes admitidos para el género.</span><span class="sxs-lookup"><span data-stu-id="71d95-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71d95-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="71d95-120">See also</span></span>



[<span data-ttu-id="71d95-121">Propiedad canónica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="71d95-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

