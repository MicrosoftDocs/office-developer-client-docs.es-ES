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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326393"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="a5046-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="a5046-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="a5046-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5046-105">Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido para que el proveedor pueda emprender acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="a5046-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="a5046-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5046-106">Return value</span></span>

<span data-ttu-id="a5046-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5046-107">S_OK</span></span>
  
> <span data-ttu-id="a5046-108">El proveedor MAPI está realizando acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5046-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5046-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5046-109">See also</span></span>



[<span data-ttu-id="a5046-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5046-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="a5046-111">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="a5046-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

