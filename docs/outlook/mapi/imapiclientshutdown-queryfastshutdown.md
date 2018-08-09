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
ms.openlocfilehash: 059d0d4427a8f2d68795a671d77fb9e3d84294f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817217"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="edb73-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="edb73-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="edb73-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edb73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edb73-105">Las consultas admiten el subsistema MAPI para apagado rápido proporcionado por proveedores MAPI cargados.</span><span class="sxs-lookup"><span data-stu-id="edb73-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="edb73-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb73-106">Return value</span></span>

<span data-ttu-id="edb73-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="edb73-107">S_OK</span></span>
  
> <span data-ttu-id="edb73-108">El subsistema MAPI es compatible con el cliente MAPI para rapidez en el cierre.</span><span class="sxs-lookup"><span data-stu-id="edb73-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="edb73-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="edb73-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="edb73-110">El proveedor MAPI no es compatible con el cliente MAPI para rapidez en el cierre.</span><span class="sxs-lookup"><span data-stu-id="edb73-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edb73-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edb73-111">Remarks</span></span>

<span data-ttu-id="edb73-112">Si el subsistema MAPI es compatible con el cliente MAPI de cierre rápido depende de configuración de registro de Windows del usuario o el comportamiento predeterminado del cliente MAPI de apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="edb73-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="edb73-113">También depende de la capacidad de los proveedores MAPI cargados para admitir apagado rápido.</span><span class="sxs-lookup"><span data-stu-id="edb73-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="edb73-114">Para obtener más información, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="edb73-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb73-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb73-115">See also</span></span>



[<span data-ttu-id="edb73-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edb73-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="edb73-117">Cierre del cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="edb73-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

