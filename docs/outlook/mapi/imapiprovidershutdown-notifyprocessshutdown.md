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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817429"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="81f09-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="81f09-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="81f09-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81f09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81f09-105">Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="81f09-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="81f09-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81f09-106">Return value</span></span>

<span data-ttu-id="81f09-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="81f09-107">S_OK</span></span>
  
> <span data-ttu-id="81f09-108">El proveedor MAPI está realizando acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="81f09-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81f09-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="81f09-109">See also</span></span>



[<span data-ttu-id="81f09-110">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="81f09-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="81f09-111">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="81f09-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

