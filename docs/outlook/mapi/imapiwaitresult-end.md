---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062035"
---
# <a name="imapiwaitresultend"></a><span data-ttu-id="0f5a1-103">IMAPIWaitResult::End</span><span class="sxs-lookup"><span data-stu-id="0f5a1-103">IMAPIWaitResult::End</span></span>
  
<span data-ttu-id="0f5a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="0f5a1-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>

<span data-ttu-id="0f5a1-105">Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="0f5a1-106">INFINITE se puede usar para una espera infinita.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="0f5a1-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0f5a1-107">Parameters</span></span>

<span data-ttu-id="0f5a1-108">_tiempo de espera_</span><span class="sxs-lookup"><span data-stu-id="0f5a1-108">_timeout_</span></span>
> <span data-ttu-id="0f5a1-109">[in] El número de milisegundos para esperar a que se inicialice MAPI, puede pasar INFINITE (0xFFFFFFFF) para esperar para siempre.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-109">[in] The number of millisecond to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f5a1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f5a1-110">Return value</span></span>

<span data-ttu-id="0f5a1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f5a1-111">S_OK</span></span>
> <span data-ttu-id="0f5a1-112">MAPI se ha inicializado correctamente</span><span class="sxs-lookup"><span data-stu-id="0f5a1-112">MAPI has been initialized successfully</span></span>

<span data-ttu-id="0f5a1-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="0f5a1-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="0f5a1-114">Cuando se le da un tiempo de espera no infinito, esto indica que MAPI no se inicializó durante ese período.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5a1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f5a1-115">Remarks</span></span>
<span data-ttu-id="0f5a1-116">Esta API se comporta exactamente igual que [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span><span class="sxs-lookup"><span data-stu-id="0f5a1-116">This API behaves exactly the same as [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0f5a1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f5a1-117">See also</span></span>

[<span data-ttu-id="0f5a1-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="0f5a1-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="0f5a1-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="0f5a1-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="0f5a1-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="0f5a1-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="0f5a1-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="0f5a1-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
