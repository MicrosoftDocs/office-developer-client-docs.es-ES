---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350907"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="fd30d-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="fd30d-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="fd30d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd30d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd30d-105">Indica la intención del cliente MAPI de salir inmediatamente del proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd30d-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="fd30d-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd30d-106">Return value</span></span>

<span data-ttu-id="fd30d-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd30d-107">S_OK</span></span>
  
> <span data-ttu-id="fd30d-108">El subsistema MAPI indicó a los proveedores MAPI cargados que el cliente MAPI está saliendo inmediatamente y los proveedores MAPI están listos para la salida del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd30d-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="fd30d-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fd30d-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="fd30d-110">El subsistema MAPI no es compatible con el apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd30d-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd30d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd30d-111">Remarks</span></span>

<span data-ttu-id="fd30d-112">Para evitar la pérdida de datos del apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) y **IMAPIClientShutdown::D ofastshutdown** basándose en el resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="fd30d-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="fd30d-113">Para obtener más información, vea [procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd30d-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd30d-114">See also</span></span>



[<span data-ttu-id="fd30d-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd30d-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="fd30d-116">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="fd30d-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

