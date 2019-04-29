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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439299"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="cbb89-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="cbb89-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="cbb89-104">Este método está en desuso en OSC 1,1.</span><span class="sxs-lookup"><span data-stu-id="cbb89-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="cbb89-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cbb89-105">Remarks</span></span>

<span data-ttu-id="cbb89-106">A partir de OSC 1,1, OSC ya no llama a **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="cbb89-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="cbb89-107">El OSC omite el valor de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="cbb89-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="cbb89-108">Para admitir la búsqueda de actividades dinámicas, implemente el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb89-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="cbb89-109">Establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cbb89-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbb89-110">Ver también</span><span class="sxs-lookup"><span data-stu-id="cbb89-110">See also</span></span>

- [<span data-ttu-id="cbb89-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb89-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

