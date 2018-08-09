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
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817366"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="e4069-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="e4069-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="e4069-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4069-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4069-105">Obtiene las condiciones para la que se admiten las devoluciones de llamada por un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e4069-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="e4069-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4069-106">Parameters</span></span>

 <span data-ttu-id="e4069-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="e4069-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="e4069-108">[out] Una máscara de bits de los siguientes indicadores de capacidad:</span><span class="sxs-lookup"><span data-stu-id="e4069-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="e4069-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e4069-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="e4069-110">El objeto sin conexión es capaz de proporcionar notificaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e4069-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="e4069-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="e4069-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="e4069-112">El objeto sin conexión es capaz de proporcionar notificaciones en línea.</span><span class="sxs-lookup"><span data-stu-id="e4069-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4069-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4069-113">Remarks</span></span>

<span data-ttu-id="e4069-114">Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, puede consultar un cliente en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obtener un puntero a una interfaz **IMAPIOffline** y llame a **IMAPIOffline::GetCapabilities** para averiguar las devoluciones de llamada compatibles por el objeto.</span><span class="sxs-lookup"><span data-stu-id="e4069-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="e4069-115">El cliente, a continuación, puede optar por configurar las devoluciones de llamada mediante **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="e4069-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="e4069-116">Tenga en cuenta que, dependiendo del servidor de correo para un objeto sin conexión, un objeto que admite las devoluciones de llamada para navegar por Internet no necesariamente admite las devoluciones de llamada para trabajar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e4069-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="e4069-117">Tenga en cuenta también, mientras que un objeto sin conexión, es posible que admitan las devoluciones de llamada para que los cambios que no sea en línea o sin conexión, la API de estado sin conexión admite sólo los cambios en línea o sin conexión y los clientes deben comprobar para sólo estas capacidades.</span><span class="sxs-lookup"><span data-stu-id="e4069-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4069-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4069-118">See also</span></span>



[<span data-ttu-id="e4069-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="e4069-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="e4069-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="e4069-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="e4069-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="e4069-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="e4069-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e4069-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e4069-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="e4069-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

