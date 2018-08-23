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
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570985"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="3cfe3-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3cfe3-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="3cfe3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cfe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cfe3-105">Cancela las notificaciones que se han configurado previamente con una llamada al método [IABLogon::Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfe3-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3cfe3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cfe3-106">Parameters</span></span>

 <span data-ttu-id="3cfe3-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="3cfe3-107">_ulConnection_</span></span>
  
> <span data-ttu-id="3cfe3-108">[entrada] El número de conexión asociado con un registro activo de notificación.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="3cfe3-109">Una llamada anterior a **Advise** debe haber devuelve el valor de _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3cfe3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cfe3-110">Return value</span></span>

<span data-ttu-id="3cfe3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3cfe3-111">S_OK</span></span> 
  
> <span data-ttu-id="3cfe3-112">El registro de notificación se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3cfe3-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cfe3-113">Remarks</span></span>

<span data-ttu-id="3cfe3-114">MAPI llama al método de **Unadvise** para cancelar el registro de una notificación para un contenedor, usuario o el objeto de lista de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3cfe3-115">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="3cfe3-115">Notes to implementers</span></span>

<span data-ttu-id="3cfe3-116">La implementación de **Unadvise** dependen de si se admite la notificación con ayuda de MAPI o de forma manual.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="3cfe3-117">Si MAPI proporciona el soporte técnico, llame al método [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="3cfe3-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="3cfe3-118">Si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones, se puede retrasar hasta que se ha devuelto **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="3cfe3-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="3cfe3-119">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="3cfe3-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="3cfe3-120">Para obtener información acerca de cómo usar el [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="3cfe3-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cfe3-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3cfe3-121">See also</span></span>



[<span data-ttu-id="3cfe3-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="3cfe3-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="3cfe3-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3cfe3-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3cfe3-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cfe3-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

