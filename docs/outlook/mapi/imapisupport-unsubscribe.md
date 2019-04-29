---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421217"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="5f155-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="5f155-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="5f155-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f155-105">Cancela la responsabilidad para enviar notificaciones previamente establecidas con una llamada al método [IMAPISupport:: subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="5f155-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5f155-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f155-106">Parameters</span></span>

 <span data-ttu-id="5f155-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5f155-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5f155-108">a Número de conexión NonZero que representa el registro de notificaciones previamente establecido mediante **IMAPISupport:: subscribe**.</span><span class="sxs-lookup"><span data-stu-id="5f155-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f155-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f155-109">Return value</span></span>

<span data-ttu-id="5f155-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f155-110">S_OK</span></span> 
  
> <span data-ttu-id="5f155-111">Se canceló el registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="5f155-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="5f155-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5f155-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5f155-113">El número de conexión pasado en el parámetro _ulConnection_ no existe.</span><span class="sxs-lookup"><span data-stu-id="5f155-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f155-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f155-114">Remarks</span></span>

<span data-ttu-id="5f155-115">El método **IMAPISupport:: unsubscribe** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5f155-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="5f155-116">Los proveedores de \*\*\*\* servicios llaman a unsubscribe para cancelar un registro de notificaciones configurado anteriormente por **subscribe**.</span><span class="sxs-lookup"><span data-stu-id="5f155-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="5f155-117">**Unsubscribe** cancela el registro mediante la liberación del puntero Advise Sink pasado en la llamada **subscribe** .</span><span class="sxs-lookup"><span data-stu-id="5f155-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="5f155-118">Por lo general, se llama al método **IUnknown:: Release** del receptor de \*\*\*\* Adviser durante la llamada unsubscribe.</span><span class="sxs-lookup"><span data-stu-id="5f155-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="5f155-119">Sin embargo, si hay otro subproceso que llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto Asesor de notificaciones, la llamada de **liberación** se retrasa hasta que se devuelva el método **BENOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="5f155-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f155-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="5f155-120">See also</span></span>



[<span data-ttu-id="5f155-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5f155-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5f155-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="5f155-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="5f155-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f155-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

