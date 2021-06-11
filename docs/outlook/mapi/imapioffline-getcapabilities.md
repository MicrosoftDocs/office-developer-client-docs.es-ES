---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433377"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="b3dc4-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b3dc4-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="b3dc4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3dc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3dc4-105">Obtiene las condiciones para las que un objeto sin conexión admite las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="b3dc4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b3dc4-106">Parameters</span></span>

 <span data-ttu-id="b3dc4-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="b3dc4-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="b3dc4-108">[salida] Máscara de bits de las siguientes marcas de funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="b3dc4-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="b3dc4-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b3dc4-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="b3dc4-110">El objeto sin conexión es capaz de proporcionar notificaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="b3dc4-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b3dc4-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="b3dc4-112">El objeto sin conexión es capaz de proporcionar notificaciones en línea.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3dc4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3dc4-113">Remarks</span></span>

<span data-ttu-id="b3dc4-114">Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj,](hropenofflineobj.md)** un cliente puede consultar en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obtener un puntero a una interfaz **IMAPIOffline** y llamar a **IMAPIOffline::GetCapabilities** para averiguar las devoluciones de llamada admitidas por el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="b3dc4-115">A continuación, el cliente puede elegir configurar las devoluciones de llamada **mediante IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="b3dc4-116">Tenga en cuenta que, según el servidor de correo de un objeto sin conexión, un objeto que admite devoluciones de llamada para ponerse en línea no admite necesariamente devoluciones de llamada para desconectarse.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="b3dc4-117">Tenga en cuenta también que, aunque un objeto sin conexión puede admitir devoluciones de llamada para cambios distintos de online/offline, la API de estado sin conexión solo admite cambios en línea o sin conexión, y los clientes deben comprobar solo dichas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="b3dc4-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3dc4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3dc4-118">See also</span></span>



[<span data-ttu-id="b3dc4-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b3dc4-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="b3dc4-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b3dc4-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="b3dc4-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b3dc4-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="b3dc4-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3dc4-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b3dc4-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b3dc4-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

