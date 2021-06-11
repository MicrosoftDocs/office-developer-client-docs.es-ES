---
title: Administrar las notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429162"
---
# <a name="handling-notifications"></a><span data-ttu-id="b0454-103">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="b0454-103">Handling notifications</span></span>

<span data-ttu-id="b0454-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0454-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0454-105">Las notificaciones permiten que un objeto informe a otro objeto de que ha sufrido un cambio.</span><span class="sxs-lookup"><span data-stu-id="b0454-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="b0454-106">El tipo de cambio se conoce como evento.</span><span class="sxs-lookup"><span data-stu-id="b0454-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="b0454-107">MAPI define varios eventos para los que se generan notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b0454-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="b0454-108">Normalmente, los clientes se registran para uno o más eventos con uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="b0454-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="b0454-109">Estos objetos se denominan orígenes de aviso.</span><span class="sxs-lookup"><span data-stu-id="b0454-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="b0454-110">Los objetos que pueden actuar como orígenes de aviso incluyen el objeto de sesión, bajo el control de MAPI, o un objeto creado por un proveedor de servicios, como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0454-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="b0454-111">El objeto informado, denominado receptor de avisos, contiene una implementación de la interfaz [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) o [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface y se encuentra dentro de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b0454-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="b0454-112">Los objetos de origen Advise implementan un **método Advise,** al que los clientes llaman para registrar las notificaciones, y un método **Unadvise,** al que se llama para cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="b0454-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="b0454-113">Uno de los parámetros de **Advise** es un puntero a una implementación de **IMAPIAdviseSink** o \*\* IMAPIViewAdviseSink \*\*.</span><span class="sxs-lookup"><span data-stu-id="b0454-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="b0454-114">El origen advise almacena en caché este puntero para que pueda llamar a [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) o a uno de los métodos de **IMAPIViewAdviseSink** cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="b0454-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="b0454-115">Dado que la recepción de notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes se registren y controlan las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b0454-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="b0454-116">Sin embargo, es opcional.</span><span class="sxs-lookup"><span data-stu-id="b0454-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b0454-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b0454-117">In this section</span></span>

- <span data-ttu-id="b0454-118">[Registro de una notificación:](registering-for-a-notification.md)describe cómo registrar un cliente para notificaciones como parte de su proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="b0454-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="b0454-119">[Cancelar una notificación:](canceling-a-notification.md)describe cómo cancelar una suscripción a una notificación.</span><span class="sxs-lookup"><span data-stu-id="b0454-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="b0454-120">[Controlar la notificación del almacén de](handling-message-store-notification.md)mensajes: describe cómo registrarse para las notificaciones del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b0454-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="b0454-121">[Notificación de libreta de direcciones](handing-address-book-notification.md)de entrega: describe cómo registrar y controlar las notificaciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b0454-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="b0454-122">[Controlar la notificación de tabla:](handling-table-notification.md)describe cómo registrarse para las notificaciones de la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b0454-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="b0454-123">[Implementar un objeto Advise Sink:](implementing-an-advise-sink-object.md)describe cómo implementar un objeto de receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="b0454-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="b0454-124">[Temporización de una](timing-a-notification.md)notificación: describe el tiempo de notificación del cliente por parte de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="b0454-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="b0454-125">[Garantizar una notificación Thread-Safe:](ensuring-a-thread-safe-notification.md)describe cómo garantizar una notificación segura para subprocesos con MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0454-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="b0454-126">[Forzar una notificación:](forcing-a-notification.md)describe cómo forzar una notificación en MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0454-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

