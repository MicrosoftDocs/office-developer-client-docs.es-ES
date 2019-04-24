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
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321276"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="ecf24-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ecf24-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="ecf24-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecf24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecf24-105">Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ecf24-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="ecf24-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ecf24-106">Parameters</span></span>

 <span data-ttu-id="ecf24-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="ecf24-107">_pulState_</span></span>
  
> <span data-ttu-id="ecf24-108">contempla Estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ecf24-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="ecf24-109">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="ecf24-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="ecf24-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ecf24-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="ecf24-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ecf24-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="ecf24-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecf24-112">See also</span></span>



[<span data-ttu-id="ecf24-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ecf24-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="ecf24-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ecf24-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="ecf24-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf24-115">MAPI Constants</span></span>](mapi-constants.md)

