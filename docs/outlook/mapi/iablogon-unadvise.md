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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817110"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="10a3e-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="10a3e-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="10a3e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10a3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10a3e-105">Cancela las notificaciones que se han configurado previamente con una llamada al método [IABLogon::Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="10a3e-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="10a3e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10a3e-106">Parameters</span></span>

 <span data-ttu-id="10a3e-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="10a3e-107">_ulConnection_</span></span>
  
> <span data-ttu-id="10a3e-108">[entrada] El número de conexión asociado con un registro activo de notificación.</span><span class="sxs-lookup"><span data-stu-id="10a3e-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="10a3e-109">Una llamada anterior a **Advise** debe haber devuelve el valor de _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="10a3e-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10a3e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10a3e-110">Return value</span></span>

<span data-ttu-id="10a3e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="10a3e-111">S_OK</span></span> 
  
> <span data-ttu-id="10a3e-112">El registro de notificación se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="10a3e-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10a3e-113">Notas</span><span class="sxs-lookup"><span data-stu-id="10a3e-113">Remarks</span></span>

<span data-ttu-id="10a3e-114">MAPI llama al método de **Unadvise** para cancelar el registro de una notificación para un contenedor, usuario o el objeto de lista de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="10a3e-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="10a3e-115">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="10a3e-115">Notes to implementers</span></span>

<span data-ttu-id="10a3e-116">La implementación de **Unadvise** dependen de si se admite la notificación con ayuda de MAPI o de forma manual.</span><span class="sxs-lookup"><span data-stu-id="10a3e-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="10a3e-117">Si MAPI proporciona el soporte técnico, llame al método [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="10a3e-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="10a3e-118">Si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones, se puede retrasar hasta que se ha devuelto **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="10a3e-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="10a3e-119">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="10a3e-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="10a3e-120">Para obtener información acerca de cómo usar el [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="10a3e-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10a3e-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="10a3e-121">See also</span></span>



[<span data-ttu-id="10a3e-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="10a3e-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="10a3e-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="10a3e-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="10a3e-124">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="10a3e-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

