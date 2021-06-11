---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438872"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="191b2-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="191b2-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="191b2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="191b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="191b2-105">Indica la intención del cliente MAPI de continuar con el apagado.</span><span class="sxs-lookup"><span data-stu-id="191b2-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="191b2-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="191b2-106">Return value</span></span>

<span data-ttu-id="191b2-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="191b2-107">S_OK</span></span>
  
> <span data-ttu-id="191b2-108">El subsistema MAPI ha intentado notificar a los proveedores MAPI cargados que el cliente MAPI va a realizar un apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="191b2-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="191b2-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="191b2-109">Remarks</span></span>

<span data-ttu-id="191b2-110">Para evitar la pérdida de datos por el apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos **IMAPIClientShutdown::NotifyProcessShutdown** [e IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) en función del resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="191b2-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="191b2-111">Para obtener más información, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="191b2-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="191b2-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="191b2-112">See also</span></span>



[<span data-ttu-id="191b2-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="191b2-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="191b2-114">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="191b2-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

