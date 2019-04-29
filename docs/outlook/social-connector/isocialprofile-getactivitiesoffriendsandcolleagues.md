---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método está en desuso en Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406895"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="4d7e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="4d7e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="4d7e8-104">Este método está en desuso en Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="4d7e8-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d7e8-105">Remarks</span></span>

<span data-ttu-id="4d7e8-106">A partir de Outlook Social Connector 2013, el OSC admite sólo la sincronización a petición de actividades y no la sincronización híbrida o la caché de actividades.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="4d7e8-107">El OSC omite la configuración **cacheActivities** en el XML de capacidades y ya no llama a este método.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="4d7e8-108">Para admitir la búsqueda de actividades dinámicas, implemente el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="4d7e8-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="4d7e8-109">Establezca **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que indicará al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="4d7e8-110">Para obtener más información sobre cómo el OSC obtiene las actividades de amigos, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="4d7e8-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d7e8-111">Ver también</span><span class="sxs-lookup"><span data-stu-id="4d7e8-111">See also</span></span>

- [<span data-ttu-id="4d7e8-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="4d7e8-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

