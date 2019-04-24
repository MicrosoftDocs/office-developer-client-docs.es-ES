---
title: Inicializar MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309733"
---
# <a name="initializing-mapi"></a><span data-ttu-id="a1cfd-103">Inicializar MAPI</span><span class="sxs-lookup"><span data-stu-id="a1cfd-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="a1cfd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1cfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1cfd-105">Todas las aplicaciones cliente que usan las bibliotecas MAPI deben llamar a la función **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="a1cfd-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="a1cfd-106">Para obtener más información, vea [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a1cfd-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="a1cfd-107">**MAPIInitialize** inicializa datos globales para la sesión y prepara las bibliotecas MAPI para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="a1cfd-108">Hay algunos marcadores que es importante establecer en algunas situaciones:</span><span class="sxs-lookup"><span data-stu-id="a1cfd-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="a1cfd-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="a1cfd-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="a1cfd-110">Establezca la marca MAPI_NT_SERVICE si su cliente se implementa como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="a1cfd-111">Si el cliente es un servicio de Windows y no establece esta marca, MAPI no la reconocerá como un servicio.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="a1cfd-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="a1cfd-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="a1cfd-113">La marca MAPI_MULTITHREAD_NOTIFICATIONS está relacionada con el modo en que MAPI administra las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="a1cfd-114">MAPI crea una ventana oculta que recibe mensajes de ventana cuando se producen cambios en un objeto que genera notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="a1cfd-115">Los mensajes de ventana se procesan en algún momento, lo que hace que se envíen las notificaciones y que se llame a los métodos [IMAPIAdviseSink::](imapiadvisesink-onnotify.md) método de Notify apropiados.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="a1cfd-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="a1cfd-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="a1cfd-117">Establezca la marca MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar com con una llamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1cfd-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="a1cfd-118">Si se pasa una estructura **MAPIINIT_0** a **MAPIInitialize** con _ULFLAGS_ establecido en MAPI_NO_COINIT, MAPI asumirá que com ya se ha inicializado y omitirá la llamada a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="a1cfd-119">Si no se pasa la marca MAPI_MULTITHREAD_NOTIFICATIONS, MAPI crea la ventana de notificación en el subproceso que se usó para la primera llamada **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="a1cfd-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="a1cfd-120">MAPI crea la ventana de notificación en un subproceso independiente si se pasa MAPI_MULTITHREAD_NOTIFICATIONS (un subproceso dedicado para controlar las notificaciones).</span><span class="sxs-lookup"><span data-stu-id="a1cfd-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="a1cfd-121">MAPI espera que el subproceso que se usa para crear la ventana de notificación oculta sea el siguiente:</span><span class="sxs-lookup"><span data-stu-id="a1cfd-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="a1cfd-122">Tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-122">Have a message loop.</span></span>
    
- <span data-ttu-id="a1cfd-123">Permanecer desbloqueado durante toda la duración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="a1cfd-124">Tienen una duración mayor que cualquier otro subproceso creado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="a1cfd-125">Puede elegir qué subproceso se usa si se establece una marca en la primera llamada de **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="a1cfd-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="a1cfd-126">El peligro de permitir que uno de los subprocesos controle las notificaciones es que si el subproceso desaparece, se destruye la ventana de notificación y ya no se pueden enviar notificaciones a ningún otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="a1cfd-127">Además, el procesamiento especial puede ser necesario para controlar la distribución de los mensajes de notificación que se publican en la cola de mensajes de la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="a1cfd-128">Si usa una ventana independiente para controlar las notificaciones, asegúrese de que las notificaciones aparecerán en el momento adecuado en un subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="a1cfd-129">No necesitará ningún código especial para buscar y procesar los mensajes de Windows que se envían a la ventana de notificación.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="a1cfd-130">MAPI recomienda que los siguientes tipos de aplicaciones cliente usen un subproceso independiente para crear la ventana oculta para la compatibilidad con notificaciones:</span><span class="sxs-lookup"><span data-stu-id="a1cfd-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="a1cfd-131">Todos los clientes multiproceso.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="a1cfd-132">Servicios de Windows de un solo proceso y aplicaciones de consola Win32.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="a1cfd-133">Clientes de un único subproceso que no necesitan usar su subproceso principal para la notificación.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="a1cfd-134">Para usar el enfoque de subprocesos independiente, llame a **MAPIInitialize** en cada subproceso, estableciendo la marca MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1cfd-135">Solo la primera llamada de un cliente a **MAPIInitialize** hace que se cree una ventana oculta para admitir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="a1cfd-136">Las llamadas posteriores solo hacen que se incremente un recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="a1cfd-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

