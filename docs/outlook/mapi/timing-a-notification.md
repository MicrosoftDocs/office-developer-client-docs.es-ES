---
title: Temporización de una notificación
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
# <a name="timing-a-notification"></a><span data-ttu-id="4713c-103">Temporización de una notificación</span><span class="sxs-lookup"><span data-stu-id="4713c-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="4713c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4713c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4713c-105">Dado que la notificación de eventos es un proceso asincrónico, puede recibir una notificación en cualquier momento, no necesariamente inmediatamente después de que se haya producido el evento.</span><span class="sxs-lookup"><span data-stu-id="4713c-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="4713c-106">El tiempo de las llamadas a su [método IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varía en función del proveedor de servicios que implemente el origen del aviso.</span><span class="sxs-lookup"><span data-stu-id="4713c-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="4713c-107">Los proveedores de servicios pueden notificar a su cliente:</span><span class="sxs-lookup"><span data-stu-id="4713c-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="4713c-108">Simultáneamente con el evento.</span><span class="sxs-lookup"><span data-stu-id="4713c-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="4713c-109">Directamente después del evento.</span><span class="sxs-lookup"><span data-stu-id="4713c-109">Directly after the event.</span></span>
    
- <span data-ttu-id="4713c-110">En algún momento posterior después del evento, posiblemente después de una **llamada Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="4713c-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="4713c-111">La mayoría de los proveedores de servicios llaman a **OnNotify** después de que el método MAPI responsable del evento haya devuelto a su autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4713c-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="4713c-112">Por ejemplo, las notificaciones en los mensajes se envían cuando se guardan los cambios realizados en el mensaje, después de la llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o cuando se libera el mensaje, después de la llamada **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="4713c-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="4713c-113">Hasta que se envía la notificación, no hay cambios visibles en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4713c-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="4713c-114">Puede recibir notificaciones de un origen de aviso después de haber llamado **a Unadvise** para cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="4713c-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="4713c-115">Asegúrese de liberar el receptor de avisos solo después de que su recuento de referencias haya caído a cero, no después de una llamada **de Unadvise correcta.**</span><span class="sxs-lookup"><span data-stu-id="4713c-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="4713c-116">No suponga que, dado que ha llamado **a Unadvise,** el receptor de avisos ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="4713c-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

