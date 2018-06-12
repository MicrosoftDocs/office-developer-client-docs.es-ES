---
title: Inicialización de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817841"
---
# <a name="initializing-mapi"></a><span data-ttu-id="65af6-103">Inicialización de MAPI</span><span class="sxs-lookup"><span data-stu-id="65af6-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="65af6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65af6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65af6-105">Todas las aplicaciones de cliente que usan las bibliotecas de MAPI deben llamar a la función **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="65af6-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="65af6-106">Para obtener más información, vea [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="65af6-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="65af6-107">**MAPIInitialize** inicializa datos globales para la sesión y prepara las bibliotecas de MAPI para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="65af6-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="65af6-108">Hay algunas marcas que son importantes para establecer en algunas situaciones:</span><span class="sxs-lookup"><span data-stu-id="65af6-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="65af6-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="65af6-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="65af6-110">Establecer la marca MAPI_NT_SERVICE si su cliente se implementa como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="65af6-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="65af6-111">Si el cliente es un servicio de Windows y no se establece este marcador, MAPI no la reconocerá como un servicio.</span><span class="sxs-lookup"><span data-stu-id="65af6-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="65af6-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="65af6-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="65af6-113">El indicador MAPI_MULTITHREAD_NOTIFICATIONS relaciona con cómo MAPI administra las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="65af6-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="65af6-114">MAPI crea una ventana oculta que recibe los mensajes de ventana cuando se producen cambios a un objeto de generación de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="65af6-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="65af6-115">Se procesan los mensajes de ventana en algún momento, lo que provoca que las notificaciones se envíen y los métodos de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropiados para llamarla.</span><span class="sxs-lookup"><span data-stu-id="65af6-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="65af6-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="65af6-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="65af6-117">Establecer la marca MAPI_NO_COINT para que no intente inicializar COM con una llamada a [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx) **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="65af6-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx).</span></span> <span data-ttu-id="65af6-118">Si se pasa una estructura **MAPIINIT_0** **MAPIInitialize** con _ulFlags_ establecida en MAPI_NO_COINIT, MAPI asumirá que COM ya se ha inicializado y omitir la llamada a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="65af6-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="65af6-119">Si no se pasa el indicador MAPI_MULTITHREAD_NOTIFICATIONS, MAPI crea la ventana de notificación en el subproceso que se usó para la primera llamada **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="65af6-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="65af6-120">MAPI crea la ventana de notificación en un subproceso independiente, si se pasa MAPI_MULTITHREAD_NOTIFICATIONS: un subproceso dedicado para controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="65af6-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="65af6-121">MAPI espera del subproceso que se usa para crear la ventana de notificación oculto para:</span><span class="sxs-lookup"><span data-stu-id="65af6-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="65af6-122">Tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="65af6-122">Have a message loop.</span></span>
    
- <span data-ttu-id="65af6-123">Permanezca desbloqueada durante la vida útil de la sesión.</span><span class="sxs-lookup"><span data-stu-id="65af6-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="65af6-124">Tener una duración mayor que cualquier otro subproceso creado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="65af6-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="65af6-125">Puede elegir qué subproceso se usa al establecer una marca en la primera llamada **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="65af6-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="65af6-126">El riesgo de que uno de los subprocesos para controlar las notificaciones permite es si desaparece el subproceso, se destruye la ventana de notificación y las notificaciones ya no pueden enviarse a cualquiera de los otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="65af6-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="65af6-127">Además, el procesamiento especial podría ser necesarios para controlar el comportamiento de los mensajes de notificación que se registran en la cola de mensajes de la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="65af6-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="65af6-128">Si se utiliza una ventana independiente para controlar las notificaciones, estar seguro de que las notificaciones aparecerá en el momento adecuado en un subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="65af6-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="65af6-129">No necesita ningún código especial para buscar y procesar los mensajes de Windows que están registrados en la ventana de notificación.</span><span class="sxs-lookup"><span data-stu-id="65af6-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="65af6-130">MAPI, se recomienda que los siguientes tipos de aplicaciones cliente de utilizan un subproceso independiente para crear la ventana oculta para compatibilidad con notificación:</span><span class="sxs-lookup"><span data-stu-id="65af6-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="65af6-131">Todos los clientes de multiproceso.</span><span class="sxs-lookup"><span data-stu-id="65af6-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="65af6-132">Aplicaciones de consola de servicios de Windows y Win32 de un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="65af6-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="65af6-133">Clientes de un único subproceso que no es necesario usar su subproceso principal para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="65af6-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="65af6-134">Para usar el método de subproceso separado, llamar **MAPIInitialize** en cada subproceso, establecer el indicador MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="65af6-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="65af6-135">Sólo un cliente primera llamada a **MAPIInitialize** hace que una ventana oculta que se creará para admitir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="65af6-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="65af6-136">Llamadas posteriores causa sólo se incrementa un recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="65af6-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

