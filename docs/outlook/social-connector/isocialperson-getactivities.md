---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Este método está en desuso en Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437745"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="79aae-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="79aae-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="79aae-104">Este método está en desuso en Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="79aae-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="79aae-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79aae-105">Remarks</span></span>

<span data-ttu-id="79aae-106">A partir de Outlook Social Connector 2013, el OSC admite sólo la sincronización a petición de actividades y no la sincronización híbrida o la caché de actividades.</span><span class="sxs-lookup"><span data-stu-id="79aae-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="79aae-107">El OSC omite la configuración **cacheActivities** en el XML de capacidades y no llama a este método.</span><span class="sxs-lookup"><span data-stu-id="79aae-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="79aae-108">Para admitir la búsqueda de actividades dinámicas, implemente el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="79aae-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="79aae-109">Establezca **cacheActivities** como **false**, **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="79aae-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="79aae-110">Para obtener más información sobre cómo el OSC obtiene las actividades de amigos, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="79aae-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79aae-111">Ver también</span><span class="sxs-lookup"><span data-stu-id="79aae-111">See also</span></span>

- [<span data-ttu-id="79aae-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79aae-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

