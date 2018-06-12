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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817373"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="73d7c-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="73d7c-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="73d7c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73d7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73d7c-105">Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="73d7c-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="73d7c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73d7c-106">Parameters</span></span>

 <span data-ttu-id="73d7c-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="73d7c-107">_pulState_</span></span>
  
> <span data-ttu-id="73d7c-108">[out] El estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="73d7c-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="73d7c-109">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="73d7c-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="73d7c-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="73d7c-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="73d7c-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="73d7c-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="73d7c-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="73d7c-112">See also</span></span>



[<span data-ttu-id="73d7c-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="73d7c-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="73d7c-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="73d7c-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="73d7c-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="73d7c-115">MAPI Constants</span></span>](mapi-constants.md)

