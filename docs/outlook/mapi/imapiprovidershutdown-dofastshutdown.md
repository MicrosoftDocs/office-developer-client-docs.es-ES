---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428847"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="53686-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="53686-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="53686-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53686-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53686-105">Indica al proveedor MAPI que el cliente MAPI está saliendo inmediatamente, de modo que el proveedor MAPI mantendrá los cambios para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="53686-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="53686-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53686-106">Return value</span></span>

<span data-ttu-id="53686-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="53686-107">S_OK</span></span>
  
> <span data-ttu-id="53686-108">El proveedor MAPI está preparado para que el cliente MAPI salga inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="53686-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="53686-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="53686-109">See also</span></span>



[<span data-ttu-id="53686-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53686-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="53686-111">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="53686-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

