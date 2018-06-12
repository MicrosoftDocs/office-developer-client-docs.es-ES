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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817408"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="ebb13-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ebb13-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="ebb13-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebb13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebb13-105">Indica que el proveedor MAPI que el cliente MAPI está saliendo inmediatamente, para que el proveedor MAPI guardará los cambios para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="ebb13-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ebb13-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb13-106">Return value</span></span>

<span data-ttu-id="ebb13-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebb13-107">S_OK</span></span>
  
> <span data-ttu-id="ebb13-108">El proveedor MAPI está listo para el cliente de MAPI salir inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ebb13-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ebb13-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="ebb13-109">See also</span></span>



[<span data-ttu-id="ebb13-110">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebb13-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="ebb13-111">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb13-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

