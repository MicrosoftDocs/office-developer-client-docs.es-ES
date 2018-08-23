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
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592055"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="f2356-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="f2356-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="f2356-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2356-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2356-105">Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="f2356-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="f2356-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2356-106">Return value</span></span>

<span data-ttu-id="f2356-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2356-107">S_OK</span></span>
  
> <span data-ttu-id="f2356-108">El proveedor MAPI está realizando acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2356-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2356-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f2356-109">See also</span></span>



[<span data-ttu-id="f2356-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2356-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="f2356-111">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="f2356-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

