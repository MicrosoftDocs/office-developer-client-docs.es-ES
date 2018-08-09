---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Este método ha quedado obsoleto en OSC 1.1.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821115"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="5f789-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="5f789-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="5f789-104">Este método ha quedado obsoleto en OSC 1.1.</span><span class="sxs-lookup"><span data-stu-id="5f789-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="5f789-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f789-105">Remarks</span></span>

<span data-ttu-id="5f789-106">A partir de OSC 1.1, el OSC ya no llama a **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="5f789-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="5f789-107">El OSC ignora el valor de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="5f789-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="5f789-108">Para admitir la búsqueda de actividades dinámico, implemente el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="5f789-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="5f789-109">Establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5f789-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f789-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f789-110">See also</span></span>

- [<span data-ttu-id="5f789-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f789-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

