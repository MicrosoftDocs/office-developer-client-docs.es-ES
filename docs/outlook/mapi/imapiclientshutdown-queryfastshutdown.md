---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418151"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="132c7-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="132c7-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="132c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="132c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="132c7-105">Consulta el subsistema MAPI para obtener compatibilidad con el apagado rápido que proporcionan los proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="132c7-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="132c7-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="132c7-106">Return value</span></span>

<span data-ttu-id="132c7-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="132c7-107">S_OK</span></span>
  
> <span data-ttu-id="132c7-108">El subsistema MAPI admite que el cliente MAPI realice un apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="132c7-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="132c7-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="132c7-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="132c7-110">El proveedor MAPI no admite el cliente MAPI para realizar el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="132c7-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="132c7-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="132c7-111">Remarks</span></span>

<span data-ttu-id="132c7-112">Si el subsistema MAPI admite que el cliente MAPI realice un apagado rápido depende de la configuración del Registro de Windows del usuario o del comportamiento predeterminado del cliente MAPI para el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="132c7-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="132c7-113">También depende de la capacidad de los proveedores MAPI cargados para admitir el apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="132c7-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="132c7-114">Para obtener más información, vea [Opciones de usuario de apagado rápido.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="132c7-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="132c7-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="132c7-115">See also</span></span>



[<span data-ttu-id="132c7-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="132c7-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="132c7-117">Cierre del cliente en MAPI</span><span class="sxs-lookup"><span data-stu-id="132c7-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

