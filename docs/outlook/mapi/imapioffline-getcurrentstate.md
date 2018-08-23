---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568206"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="8aea8-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8aea8-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="8aea8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aea8-105">Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8aea8-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="8aea8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aea8-106">Parameters</span></span>

 <span data-ttu-id="8aea8-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="8aea8-107">_pulState_</span></span>
  
> <span data-ttu-id="8aea8-108">[out] El estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8aea8-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="8aea8-109">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="8aea8-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="8aea8-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="8aea8-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="8aea8-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="8aea8-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="8aea8-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8aea8-112">See also</span></span>



[<span data-ttu-id="8aea8-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="8aea8-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="8aea8-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8aea8-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="8aea8-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8aea8-115">MAPI Constants</span></span>](mapi-constants.md)

