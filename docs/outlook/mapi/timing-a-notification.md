---
title: Cronometrar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411151"
---
# <a name="timing-a-notification"></a><span data-ttu-id="c7cd1-103">Cronometrar una notificación</span><span class="sxs-lookup"><span data-stu-id="c7cd1-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="c7cd1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7cd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7cd1-105">Dado que la notificación de eventos es un proceso asincrónico, se le puede notificar en cualquier momento, no necesariamente inmediatamente después de que se ha producido el evento.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="c7cd1-106">El tiempo de llamadas al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) varía en función del proveedor de servicios que implemente el origen de Advise.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="c7cd1-107">Los proveedores de servicios pueden notificar al cliente:</span><span class="sxs-lookup"><span data-stu-id="c7cd1-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="c7cd1-108">Simultáneamente con el evento.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="c7cd1-109">Justo después del evento.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-109">Directly after the event.</span></span>
    
- <span data-ttu-id="c7cd1-110">En un punto posterior después del evento, posiblemente después de una llamada a **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="c7cd1-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="c7cd1-111">La mayoría de los proveedores de servicios llaman a **Notify** una vez que el método de MAPI responsable del evento ha vuelto a su autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="c7cd1-112">Por ejemplo, las notificaciones en los mensajes se envían cuando se guardan los cambios en el mensaje después de la llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) o cuando se libera el mensaje, después de la llamada a **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c7cd1-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="c7cd1-113">Hasta que se envíe la notificación, no habrá ningún cambio visible en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="c7cd1-114">Puede recibir notificaciones de un origen de notificaciones después de haber \*\*\*\* llamado a Unadvise para cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="c7cd1-115">Asegúrese de liberar el receptor de notificaciones solo después de que su recuento de referencia haya caído en cero \*\*\*\* , no después de una llamada de desaconsejar correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="c7cd1-116">No dé por supuesto que, debido a \*\*\*\* que ha llamado a unaconsejar que el receptor de notificaciones ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

