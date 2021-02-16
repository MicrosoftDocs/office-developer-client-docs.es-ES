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
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422351"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="c68e7-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="c68e7-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="c68e7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c68e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c68e7-105">Informa a Microsoft Outlook de que la sincronización se ha completado.</span><span class="sxs-lookup"><span data-stu-id="c68e7-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="c68e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c68e7-106">Parameters</span></span>

 <span data-ttu-id="c68e7-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="c68e7-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="c68e7-108">Evento que se pasa para permitir que Microsoft Outlook cierre el identificador.</span><span class="sxs-lookup"><span data-stu-id="c68e7-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="c68e7-109">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c68e7-109">It can be NULL.</span></span>
    
 <span data-ttu-id="c68e7-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="c68e7-110">**hResult**</span></span>
  
> <span data-ttu-id="c68e7-111">HRESULT que indica el estado final del progreso.</span><span class="sxs-lookup"><span data-stu-id="c68e7-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c68e7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c68e7-112">Return value</span></span>

<span data-ttu-id="c68e7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c68e7-113">S_OK</span></span> 
  
> <span data-ttu-id="c68e7-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c68e7-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c68e7-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c68e7-115">See also</span></span>



[<span data-ttu-id="c68e7-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c68e7-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

