---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 65ed848907e196c315e8ddb61c4afd2fe03faa18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270290"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="d4253-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="d4253-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="d4253-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4253-105">La MAPIOFFLINE_NOTIFY_TYPE de una notificación identifica si se va a realizar un cambio en el estado de conexión, si se está llevando a cabo o se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d4253-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d4253-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d4253-106">Quick info</span></span>

<span data-ttu-id="d4253-107">Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="d4253-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="d4253-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4253-108">See also</span></span>



[<span data-ttu-id="d4253-109">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="d4253-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="d4253-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d4253-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d4253-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="d4253-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

