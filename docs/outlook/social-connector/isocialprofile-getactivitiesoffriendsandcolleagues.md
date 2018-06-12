---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método ha quedado obsoleto en Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821132"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="edcf1-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="edcf1-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="edcf1-104">Este método ha quedado obsoleto en Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="edcf1-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="edcf1-105">Notas</span><span class="sxs-lookup"><span data-stu-id="edcf1-105">Remarks</span></span>

<span data-ttu-id="edcf1-106">Inicio en Outlook Social Connector 2013, el OSC admite la sincronización de sólo a petición de actividades y no en caché o sincronización híbrido de actividades.</span><span class="sxs-lookup"><span data-stu-id="edcf1-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="edcf1-107">El OSC pasa por alto la configuración de **cacheActivities** en el XML de las capacidades y ya no se llama a este método.</span><span class="sxs-lookup"><span data-stu-id="edcf1-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="edcf1-108">Para admitir la búsqueda de actividades dinámico, implemente el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="edcf1-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="edcf1-109">Establecer **getActivities** y **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="edcf1-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="edcf1-110">Para obtener más información acerca de cómo el OSC Obtiene las actividades de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="edcf1-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="edcf1-111">Ver también</span><span class="sxs-lookup"><span data-stu-id="edcf1-111">See also</span></span>

- [<span data-ttu-id="edcf1-112">ISocialProfile: ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="edcf1-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

