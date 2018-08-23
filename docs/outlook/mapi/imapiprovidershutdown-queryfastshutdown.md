---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4301fb504439cf0ebd70b5ece589c812cb74844e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585300"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="df892-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="df892-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="df892-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df892-105">Las consultas que admite el proveedor MAPI de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="df892-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="df892-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df892-106">Return value</span></span>

<span data-ttu-id="df892-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="df892-107">S_OK</span></span>
  
> <span data-ttu-id="df892-108">El proveedor MAPI es compatible con el cliente MAPI para rapidez en el cierre.</span><span class="sxs-lookup"><span data-stu-id="df892-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="df892-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="df892-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="df892-110">El proveedor MAPI no es compatible con el cliente MAPI para rapidez en el cierre.</span><span class="sxs-lookup"><span data-stu-id="df892-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df892-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df892-111">Remarks</span></span>

<span data-ttu-id="df892-112">Proveedores MAPI que no es necesario para admitir el apagado rápido cliente aún deben implementar la interfaz [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) y tener el método **IMAPIProviderShutdown::QueryFastShutdown** devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="df892-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="df892-113">Para Outlook como un cliente MAPI, esto hace que Outlook que se debe esperar para que todas las referencias externas a liberarse antes de que exista.</span><span class="sxs-lookup"><span data-stu-id="df892-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="df892-114">Dependiendo del registro de Windows del usuario configuración de apagado rápido, no se implementa la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="df892-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df892-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="df892-115">See also</span></span>



[<span data-ttu-id="df892-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df892-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="df892-117">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="df892-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

