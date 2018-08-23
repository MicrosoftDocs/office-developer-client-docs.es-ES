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
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566890"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="c3d87-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3d87-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="c3d87-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d87-105">El MAPIOFFLINE_NOTIFY_TYPE de una notificación identifica si un cambio en el estado de conexión se va a tener lugar, está produciendo o ha completado.</span><span class="sxs-lookup"><span data-stu-id="c3d87-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c3d87-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c3d87-106">Quick info</span></span>

<span data-ttu-id="c3d87-107">Vea **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="c3d87-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="c3d87-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c3d87-108">See also</span></span>



[<span data-ttu-id="c3d87-109">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="c3d87-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="c3d87-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d87-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c3d87-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="c3d87-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

