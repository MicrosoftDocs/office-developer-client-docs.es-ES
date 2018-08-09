---
title: Asegurar una notificación de seguro para subprocesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816758"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="716bd-103">Asegurar una notificación de seguro para subprocesos</span><span class="sxs-lookup"><span data-stu-id="716bd-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="716bd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="716bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="716bd-105">Si el cliente se ejecuta en una plataforma de multiproceso, puede que tenga la garantía de que las llamadas a los métodos de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se producen en un subproceso concreto.</span><span class="sxs-lookup"><span data-stu-id="716bd-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="716bd-106">Debido a que las llamadas a **OnNotify** normalmente pueden suceder en cualquier subproceso, es posible recibir notificaciones en subprocesos inesperados y no deseados, conduce a los errores que son difíciles de depurar.</span><span class="sxs-lookup"><span data-stu-id="716bd-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="716bd-107">Para garantizar que las llamadas a **OnNotify** para una notificación en particular se realizan en el mismo subproceso que se usó para la **Advise** llamar, llamar [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de llamar a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="716bd-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="716bd-108">\*\* \*\* HrThisThreadAdviseSink \*\*\* crea un nuevo objeto de receptor de advise desde su objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="716bd-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="716bd-109">Pase el nuevo objeto de la llamada a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="716bd-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="716bd-110">Todos los clientes con objetos que pueden no funcionar fuera del contexto de un subproceso determinado siempre deben registrar el receptor de notificaciones de aviso objetos del receptor creados con **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="716bd-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

