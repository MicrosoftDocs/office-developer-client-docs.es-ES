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
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563474"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="30c86-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="30c86-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="30c86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30c86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30c86-105">Indica que el proveedor MAPI que el cliente MAPI está saliendo inmediatamente, para que el proveedor MAPI guardará los cambios para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="30c86-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="30c86-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30c86-106">Return value</span></span>

<span data-ttu-id="30c86-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="30c86-107">S_OK</span></span>
  
> <span data-ttu-id="30c86-108">El proveedor MAPI está listo para el cliente de MAPI salir inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="30c86-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="30c86-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="30c86-109">See also</span></span>



[<span data-ttu-id="30c86-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30c86-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="30c86-111">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="30c86-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

