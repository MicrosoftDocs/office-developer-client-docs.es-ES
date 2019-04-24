---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Este método está en desuso en OSC 1,1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285458"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="b7cd1-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="b7cd1-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="b7cd1-104">Este método está en desuso en OSC 1,1.</span><span class="sxs-lookup"><span data-stu-id="b7cd1-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="b7cd1-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7cd1-105">Remarks</span></span>

<span data-ttu-id="b7cd1-106">A partir de OSC 1,1, OSC ya no llama a **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="b7cd1-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="b7cd1-107">El OSC omite el valor de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="b7cd1-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="b7cd1-108">Para admitir la búsqueda de actividades dinámicas, implemente el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="b7cd1-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="b7cd1-109">Establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b7cd1-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7cd1-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7cd1-110">See also</span></span>

- [<span data-ttu-id="b7cd1-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7cd1-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

