---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573211"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="94874-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="94874-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="94874-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="94874-105">Informa a Microsoft Outlook que la sincronización es completa.</span><span class="sxs-lookup"><span data-stu-id="94874-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="94874-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94874-106">Parameters</span></span>

 <span data-ttu-id="94874-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="94874-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="94874-108">Un evento que se pasa atrás para permitir que Microsoft Outlook cerrar el identificador.</span><span class="sxs-lookup"><span data-stu-id="94874-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="94874-109">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="94874-109">It can be NULL.</span></span>
    
 <span data-ttu-id="94874-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="94874-110">**hResult**</span></span>
  
> <span data-ttu-id="94874-111">Un HRESULT que indica el estado final del progreso.</span><span class="sxs-lookup"><span data-stu-id="94874-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94874-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94874-112">Return value</span></span>

<span data-ttu-id="94874-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="94874-113">S_OK</span></span> 
  
> <span data-ttu-id="94874-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="94874-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94874-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="94874-115">See also</span></span>



[<span data-ttu-id="94874-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94874-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

