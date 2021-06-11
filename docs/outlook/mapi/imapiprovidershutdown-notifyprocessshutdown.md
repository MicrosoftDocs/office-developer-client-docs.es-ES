---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405250"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="8e6cb-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="8e6cb-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="8e6cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e6cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e6cb-105">Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido, de modo que el proveedor puede realizar acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="8e6cb-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e6cb-106">Return value</span></span>

<span data-ttu-id="8e6cb-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e6cb-107">S_OK</span></span>
  
> <span data-ttu-id="8e6cb-108">El proveedor MAPI está llevando a cabo acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e6cb-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e6cb-109">See also</span></span>



[<span data-ttu-id="8e6cb-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e6cb-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="8e6cb-111">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="8e6cb-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

