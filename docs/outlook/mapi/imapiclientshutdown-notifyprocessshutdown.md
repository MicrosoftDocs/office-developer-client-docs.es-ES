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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568269"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="004fb-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="004fb-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="004fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="004fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="004fb-105">Indica la intención de continuar con la del cliente MAPI cerrado.</span><span class="sxs-lookup"><span data-stu-id="004fb-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="004fb-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="004fb-106">Return value</span></span>

<span data-ttu-id="004fb-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="004fb-107">S_OK</span></span>
  
> <span data-ttu-id="004fb-108">Ha intentado el subsistema MAPI notificar a los proveedores MAPI cargados que el cliente MAPI se va a realizar un cierre rápido.</span><span class="sxs-lookup"><span data-stu-id="004fb-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="004fb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="004fb-109">Remarks</span></span>

<span data-ttu-id="004fb-110">Para evitar la pérdida de datos desde el apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos **IMAPIClientShutdown::NotifyProcessShutdown** y [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) según el resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="004fb-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="004fb-111">Para obtener más información, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="004fb-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="004fb-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="004fb-112">See also</span></span>



[<span data-ttu-id="004fb-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="004fb-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="004fb-114">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="004fb-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

