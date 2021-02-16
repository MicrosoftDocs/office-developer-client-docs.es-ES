---
title: Garantizar una notificación Thread-Safe personalizada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424850"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="2ff1a-103">Garantizar una notificación Thread-Safe personalizada</span><span class="sxs-lookup"><span data-stu-id="2ff1a-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="2ff1a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff1a-105">Si el cliente se ejecuta en una plataforma multiproceso, es posible que necesite la seguridad de que las llamadas a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se producen en un subproceso determinado.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="2ff1a-106">Dado que las llamadas a **OnNotify** suelen producirse en cualquier subproceso, es posible recibir notificaciones en subprocesos inesperados y no deseados, lo que provoca errores que son difíciles de depurar.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="2ff1a-107">Para garantizar que las llamadas a **OnNotify** para una notificación determinada se realizan en el mismo subproceso que se usó para la llamada **advise,** llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de llamar a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="2ff1a-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* crea un nuevo objeto receptor de aviso a partir del objeto receptor de avisos.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="2ff1a-109">Pase este nuevo objeto en la llamada a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="2ff1a-110">Todos los clientes con objetos receptores de aviso que podrían no funcionar fuera del contexto de un subproceso determinado siempre deben registrar los objetos receptores de aviso creados con **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="2ff1a-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

