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
# <a name="initializing-mapi"></a><span data-ttu-id="1fb55-103">Inicializar MAPI</span><span class="sxs-lookup"><span data-stu-id="1fb55-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="1fb55-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fb55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fb55-105">Todas las aplicaciones cliente que usan las bibliotecas MAPI deben llamar a la **función MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="1fb55-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="1fb55-106">Para obtener más información, vea [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="1fb55-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="1fb55-107">**MAPIInitialize inicializa** los datos globales de la sesión y prepara las bibliotecas MAPI para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="1fb55-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="1fb55-108">Hay algunas marcas que son importantes establecer en algunas situaciones:</span><span class="sxs-lookup"><span data-stu-id="1fb55-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="1fb55-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1fb55-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="1fb55-110">Establezca la MAPI_NT_SERVICE si el cliente se implementa como un Windows cliente.</span><span class="sxs-lookup"><span data-stu-id="1fb55-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="1fb55-111">Si el cliente es un Windows y no establece esta marca, MAPI no lo reconocerá como servicio.</span><span class="sxs-lookup"><span data-stu-id="1fb55-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="1fb55-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="1fb55-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="1fb55-113">La MAPI_MULTITHREAD_NOTIFICATIONS se relaciona con la forma en que MAPI administra las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1fb55-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="1fb55-114">MAPI crea una ventana oculta que recibe mensajes de ventana cuando se producen cambios en un objeto que genera notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1fb55-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="1fb55-115">Los mensajes de ventana se procesan en algún momento, lo que hace que se envíen las notificaciones y se llame a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) adecuados.</span><span class="sxs-lookup"><span data-stu-id="1fb55-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="1fb55-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="1fb55-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="1fb55-117">Establezca la MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar COM con una llamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fb55-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="1fb55-118">Si se **pasa** una estructura MAPIINIT_0 **a MAPIInitialize** con  _ulFlags_ establecido en MAPI_NO_COINIT, MAPI supondrá que COM ya se ha inicializado y omitirá la llamada a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="1fb55-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="1fb55-119">Si MAPI_MULTITHREAD_NOTIFICATIONS marca no se pasa, MAPI crea la ventana de notificación en el subproceso que se usó para la primera **llamada MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="1fb55-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="1fb55-120">MAPI crea la ventana de notificación en un subproceso independiente si MAPI_MULTITHREAD_NOTIFICATIONS se pasa, un subproceso dedicado a controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1fb55-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="1fb55-121">MAPI espera que el subproceso que se usa para crear la ventana de notificación oculta sea:</span><span class="sxs-lookup"><span data-stu-id="1fb55-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="1fb55-122">Tener un bucle de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1fb55-122">Have a message loop.</span></span>
    
- <span data-ttu-id="1fb55-123">Permanece desbloqueado durante toda la vida de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1fb55-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="1fb55-124">Tenga una duración más larga que cualquier otro subproceso creado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="1fb55-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="1fb55-125">Puede elegir qué subproceso se usa estableciendo una marca en la primera **llamada MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="1fb55-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="1fb55-126">El peligro de permitir que uno de los subprocesos controle las notificaciones es que si el subproceso desaparece, la ventana de notificación se destruye y las notificaciones ya no se pueden enviar a ninguno de los otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1fb55-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="1fb55-127">Además, es posible que sea necesario un procesamiento especial para controlar el envío de los mensajes de notificación que se publican en la cola de mensajes de la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="1fb55-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="1fb55-128">Si usa una ventana independiente para controlar las notificaciones, asegúrese de que las notificaciones aparecerán en el momento adecuado en un subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="1fb55-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="1fb55-129">No necesitará ningún código especial para buscar y procesar los mensajes Windows que se publican en la ventana de notificación.</span><span class="sxs-lookup"><span data-stu-id="1fb55-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="1fb55-130">MAPI recomienda que los siguientes tipos de aplicaciones cliente usen un subproceso independiente para crear la ventana oculta para la compatibilidad con notificaciones:</span><span class="sxs-lookup"><span data-stu-id="1fb55-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="1fb55-131">Todos los clientes multiproceso.</span><span class="sxs-lookup"><span data-stu-id="1fb55-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="1fb55-132">Servicios de Windows de un solo subproceso y aplicaciones de consola de Win32.</span><span class="sxs-lookup"><span data-stu-id="1fb55-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="1fb55-133">Clientes de subproceso único que no necesitan usar su subproceso principal para la notificación.</span><span class="sxs-lookup"><span data-stu-id="1fb55-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="1fb55-134">Para usar el enfoque de subproceso independiente, llame **a MAPIInitialize** en cada subproceso, estableciendo la marca MAPI_MULTITHREAD_NOTIFICATIONS hilo.</span><span class="sxs-lookup"><span data-stu-id="1fb55-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1fb55-135">Solo la primera llamada de un cliente a **MAPIInitialize** hace que se cree una ventana oculta para admitir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1fb55-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="1fb55-136">Las llamadas posteriores solo hacen que se incremente un recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="1fb55-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

