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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321318"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="b6a13-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b6a13-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="b6a13-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6a13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6a13-105">Obtiene las condiciones para las que se admiten las devoluciones de llamada por un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b6a13-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="b6a13-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b6a13-106">Parameters</span></span>

 <span data-ttu-id="b6a13-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="b6a13-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="b6a13-108">contempla Máscara de máscara de las siguientes marcas de capacidad:</span><span class="sxs-lookup"><span data-stu-id="b6a13-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="b6a13-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b6a13-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="b6a13-110">El objeto sin conexión es capaz de ofrecer notificaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b6a13-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="b6a13-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b6a13-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="b6a13-112">El objeto sin conexión es capaz de ofrecer notificaciones en línea.</span><span class="sxs-lookup"><span data-stu-id="b6a13-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6a13-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6a13-113">Remarks</span></span>

<span data-ttu-id="b6a13-114">Al abrir un objeto sin conexión con **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente puede realizar una consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obtener un puntero a una interfaz de **IMAPIOffline** y llamar a **IMAPIOffline:: GetCapabilities** para conocer las devoluciones de llamada admitidas por el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6a13-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="b6a13-115">A continuación, el cliente puede elegir configurar las devoluciones de llamada mediante **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="b6a13-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="b6a13-116">Tenga en cuenta que, según el servidor de correo de un objeto sin conexión, un objeto que admite las devoluciones de llamada para la conexión no es necesariamente compatible con las devoluciones de llamada para desconectarse.</span><span class="sxs-lookup"><span data-stu-id="b6a13-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="b6a13-117">Además, tenga en cuenta que, aunque un objeto sin conexión puede admitir devoluciones de llamada para cambios que no sean en línea o sin conexión, la API de estado sin conexión solo admite cambios en línea o sin conexión, y los clientes deben comprobar solo dichas funciones.</span><span class="sxs-lookup"><span data-stu-id="b6a13-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6a13-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6a13-118">See also</span></span>



[<span data-ttu-id="b6a13-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b6a13-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="b6a13-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b6a13-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="b6a13-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b6a13-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="b6a13-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6a13-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b6a13-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b6a13-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

