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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419873"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="c4387-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="c4387-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="c4387-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4387-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4387-105">Obtiene el estado actual en línea o sin conexión de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c4387-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="c4387-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4387-106">Parameters</span></span>

 <span data-ttu-id="c4387-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="c4387-107">_pulState_</span></span>
  
> <span data-ttu-id="c4387-108">[salida] Estado actual en línea o sin conexión de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c4387-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="c4387-109">Debe ser uno de estos dos valores:</span><span class="sxs-lookup"><span data-stu-id="c4387-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="c4387-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="c4387-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="c4387-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="c4387-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="c4387-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c4387-112">See also</span></span>



[<span data-ttu-id="c4387-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c4387-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="c4387-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="c4387-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="c4387-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c4387-115">MAPI Constants</span></span>](mapi-constants.md)

