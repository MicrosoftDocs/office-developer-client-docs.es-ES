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
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817562"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="26f2a-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="26f2a-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="26f2a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26f2a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="26f2a-105">Informa a Microsoft Outlook que la sincronización es completa.</span><span class="sxs-lookup"><span data-stu-id="26f2a-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="26f2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f2a-106">Parameters</span></span>

 <span data-ttu-id="26f2a-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="26f2a-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="26f2a-108">Un evento que se pasa atrás para permitir que Microsoft Outlook cerrar el identificador.</span><span class="sxs-lookup"><span data-stu-id="26f2a-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="26f2a-109">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="26f2a-109">It can be NULL.</span></span>
    
 <span data-ttu-id="26f2a-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="26f2a-110">**hResult**</span></span>
  
> <span data-ttu-id="26f2a-111">Un HRESULT que indica el estado final del progreso.</span><span class="sxs-lookup"><span data-stu-id="26f2a-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26f2a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f2a-112">Return value</span></span>

<span data-ttu-id="26f2a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="26f2a-113">S_OK</span></span> 
  
> <span data-ttu-id="26f2a-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="26f2a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26f2a-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f2a-115">See also</span></span>



[<span data-ttu-id="26f2a-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26f2a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

