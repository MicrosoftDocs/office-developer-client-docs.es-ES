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
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817564"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="3c3f4-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="3c3f4-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="3c3f4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c3f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c3f4-105">Cancela la responsabilidad de envío de notificaciones que se estableció previamente con una llamada al método [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3f4-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3c3f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c3f4-106">Parameters</span></span>

 <span data-ttu-id="3c3f4-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="3c3f4-107">_ulConnection_</span></span>
  
> <span data-ttu-id="3c3f4-108">[entrada] El número de conexión distinto de cero que representa el registro de la notificación previamente establecido mediante **IMAPISupport::Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c3f4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c3f4-109">Return value</span></span>

<span data-ttu-id="3c3f4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c3f4-110">S_OK</span></span> 
  
> <span data-ttu-id="3c3f4-111">Se ha cancelado el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="3c3f4-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3c3f4-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3c3f4-113">El número de conexión que se pasa en el parámetro _ulConnection_ no existe.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3c3f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c3f4-114">Remarks</span></span>

<span data-ttu-id="3c3f4-115">El método **IMAPISupport::Unsubscribe** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="3c3f4-116">Proveedores de servicios de llamada **Cancelar** para cancelar un registro configurado previamente por **suscribirse**a las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="3c3f4-117">**Cancelar** cancela el registro por liberar el puntero del receptor de advise pasado en la llamada **Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="3c3f4-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="3c3f4-118">Por lo general, se llama al método de **IUnknown:: Release** del receptor de notificaciones durante la llamada de **cancelación de suscripción** .</span><span class="sxs-lookup"><span data-stu-id="3c3f4-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="3c3f4-119">Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve.</span><span class="sxs-lookup"><span data-stu-id="3c3f4-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c3f4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c3f4-120">See also</span></span>



[<span data-ttu-id="3c3f4-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3c3f4-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3c3f4-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="3c3f4-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="3c3f4-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c3f4-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

