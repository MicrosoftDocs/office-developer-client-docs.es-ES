---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424080"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="391c5-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="391c5-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="391c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="391c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="391c5-105">Cancela las notificaciones configuradas anteriormente con una llamada al [método IABLogon::Advise.](iablogon-advise.md)</span><span class="sxs-lookup"><span data-stu-id="391c5-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="391c5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="391c5-106">Parameters</span></span>

 <span data-ttu-id="391c5-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="391c5-107">_ulConnection_</span></span>
  
> <span data-ttu-id="391c5-108">[in] Número de conexión asociado a un registro de notificación activo.</span><span class="sxs-lookup"><span data-stu-id="391c5-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="391c5-109">Una llamada anterior a **Advise** debe haber devuelto el valor de  _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="391c5-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="391c5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="391c5-110">Return value</span></span>

<span data-ttu-id="391c5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="391c5-111">S_OK</span></span> 
  
> <span data-ttu-id="391c5-112">El registro de notificación se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="391c5-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="391c5-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="391c5-113">Remarks</span></span>

<span data-ttu-id="391c5-114">MAPI llama al **método Unadvise** para cancelar un registro de notificación para un contenedor, un usuario de mensajería o un objeto de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="391c5-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="391c5-115">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="391c5-115">Notes to implementers</span></span>

<span data-ttu-id="391c5-116">La implementación de **Unadvise** dependerá de si admite la notificación con la ayuda de MAPI o manualmente.</span><span class="sxs-lookup"><span data-stu-id="391c5-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="391c5-117">Si MAPI proporciona soporte técnico, llama al [método IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="391c5-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="391c5-118">Si otro subproceso está en el proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de aviso, puede retrasarse hasta que **OnNotify** haya devuelto.</span><span class="sxs-lookup"><span data-stu-id="391c5-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="391c5-119">Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="391c5-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="391c5-120">Para obtener información sobre cómo usar los métodos [IMAPISupport : IUnknown](imapisupportiunknown.md) para admitir la notificación, vea [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="391c5-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="391c5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="391c5-121">See also</span></span>



[<span data-ttu-id="391c5-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="391c5-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="391c5-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="391c5-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="391c5-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="391c5-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

