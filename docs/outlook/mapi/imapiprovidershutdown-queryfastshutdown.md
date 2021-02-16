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
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418221"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="c283e-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c283e-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="c283e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c283e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c283e-105">Consulta al proveedor MAPI la compatibilidad con el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="c283e-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="c283e-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c283e-106">Return value</span></span>

<span data-ttu-id="c283e-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="c283e-107">S_OK</span></span>
  
> <span data-ttu-id="c283e-108">El proveedor MAPI admite que el cliente MAPI realice un apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="c283e-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="c283e-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c283e-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="c283e-110">El proveedor MAPI no admite el cliente MAPI para realizar el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="c283e-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c283e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c283e-111">Remarks</span></span>

<span data-ttu-id="c283e-112">Los proveedores MAPI que no necesitan admitir el apagado rápido del cliente deben seguir implementando la interfaz [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) y hacer que el método **IMAPIProviderShutdown::QueryFastShutdown** devuelva MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c283e-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c283e-113">Para Outlook como cliente MAPI, esto hace que Outlook espere a que se liberarán todas las referencias externas antes de salir.</span><span class="sxs-lookup"><span data-stu-id="c283e-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="c283e-114">Según la configuración del Registro de Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido del cliente.</span><span class="sxs-lookup"><span data-stu-id="c283e-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c283e-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c283e-115">See also</span></span>



[<span data-ttu-id="c283e-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c283e-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="c283e-117">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="c283e-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

