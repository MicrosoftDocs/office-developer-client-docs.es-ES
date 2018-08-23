---
title: Establecer intervalos de una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b4b0292ab16eabe30755fe84885a29fb8e3ce295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595198"
---
# <a name="timing-a-notification"></a><span data-ttu-id="9cee1-103">Establecer intervalos de una notificación</span><span class="sxs-lookup"><span data-stu-id="9cee1-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="9cee1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cee1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cee1-105">Debido a que la notificación de eventos es un proceso asincrónico, puede recibir una notificación en cualquier momento, no necesariamente inmediatamente después de que se ha producido el evento.</span><span class="sxs-lookup"><span data-stu-id="9cee1-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="9cee1-106">La duración de las llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varía según el proveedor de servicios de implementar el origen advise.</span><span class="sxs-lookup"><span data-stu-id="9cee1-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="9cee1-107">Proveedores de servicios pueden notificar a su cliente, ya sea:</span><span class="sxs-lookup"><span data-stu-id="9cee1-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="9cee1-108">Simultáneamente con el evento.</span><span class="sxs-lookup"><span data-stu-id="9cee1-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="9cee1-109">Directamente después del evento.</span><span class="sxs-lookup"><span data-stu-id="9cee1-109">Directly after the event.</span></span>
    
- <span data-ttu-id="9cee1-110">En algún más adelante momento después del evento, posiblemente después de una llamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="9cee1-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="9cee1-111">La mayoría de los proveedores de servicios de llamadas **OnNotify** después de que el método MAPI responsable del evento devuelva a su autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9cee1-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="9cee1-112">Por ejemplo, en los mensajes se envían cuando se guardan los cambios realizados en el mensaje, después de la llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , o cuando se libera el mensaje, después de la llamada **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="9cee1-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="9cee1-113">Hasta que se envía la notificación, no hay ningún cambio está visible en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9cee1-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="9cee1-114">Puede recibir notificaciones desde un origen de advise después de haber llamado **Unadvise** para cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="9cee1-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="9cee1-115">Asegúrese de liberar el receptor de notificaciones sólo después de que haya caído su recuento de referencia a cero, no después de una correcta **Unadvise** llamada.</span><span class="sxs-lookup"><span data-stu-id="9cee1-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="9cee1-116">No asuma que debido a que se ha llamado **Unadvise** el receptor de notificaciones ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="9cee1-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

