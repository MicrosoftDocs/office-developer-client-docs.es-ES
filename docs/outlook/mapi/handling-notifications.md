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
# <a name="handling-notifications"></a><span data-ttu-id="06dea-103">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="06dea-103">Handling notifications</span></span>

<span data-ttu-id="06dea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06dea-105">Las notificaciones permiten que un objeto informe a otro objeto que ha sufrido un cambio.</span><span class="sxs-lookup"><span data-stu-id="06dea-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="06dea-106">El tipo de cambio se conoce como un evento.</span><span class="sxs-lookup"><span data-stu-id="06dea-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="06dea-107">MAPI define varios eventos para los que se generan notificaciones.</span><span class="sxs-lookup"><span data-stu-id="06dea-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="06dea-108">Los clientes suelen registrarse para uno o más eventos con uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="06dea-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="06dea-109">Estos objetos se conocen como orígenes de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="06dea-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="06dea-110">Los objetos que pueden actuar como orígenes de notificaciones incluyen el objeto de sesión, bajo el control de MAPI, o un objeto creado por un proveedor de servicios, como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="06dea-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="06dea-111">El objeto informado, al que se conoce como el receptor de notificaciones, contiene una implementación de la interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) o la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y está dentro de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="06dea-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="06dea-112">Aconseje a los objetos \*\*\*\* de origen que implementen un método Advise, al que llaman los clientes para registrarse para notificaciones y un método unaconsejable, al que se llama para cancelar un registro. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="06dea-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="06dea-113">Uno de los parámetros de **Advise** es un puntero a una implementación de **IMAPIAdviseSink** o \* \* IMAPIViewAdviseSink \* \*.</span><span class="sxs-lookup"><span data-stu-id="06dea-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="06dea-114">El origen Advise almacena en caché este puntero para que pueda llamar a [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) o a uno de los métodos de **IMAPIViewAdviseSink** cuando se produzca un cambio.</span><span class="sxs-lookup"><span data-stu-id="06dea-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="06dea-115">Como la recepción de notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes se registren y controlen las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="06dea-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="06dea-116">Sin embargo, es opcional.</span><span class="sxs-lookup"><span data-stu-id="06dea-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="06dea-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="06dea-117">In this section</span></span>

- <span data-ttu-id="06dea-118">[Registro para una notificación](registering-for-a-notification.md): describe cómo registrar un cliente para las notificaciones como parte de su proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="06dea-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="06dea-119">[Cancelación de una notificación](canceling-a-notification.md): describe cómo cancelar una suscripción a una notificación.</span><span class="sxs-lookup"><span data-stu-id="06dea-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="06dea-120">[Administración](handling-message-store-notification.md)de notificaCiones del almacén de mensajes: describe cómo registrarse para recibir notificaciones del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="06dea-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="06dea-121">[Entrega](handing-address-book-notification.md)de notificaciones de la libreta de direcciones: describe cómo registrar y administrar las notificaciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="06dea-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="06dea-122">[Notificación](handling-table-notification.md)de la tabla de administración: describe cómo registrar las notificaciones en la tabla de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="06dea-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="06dea-123">[Implementar un objeto de receptor](implementing-an-advise-sink-object.md)de notificaciones: describe cómo implementar un objeto de receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="06dea-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="06dea-124">[Cronometrar una notificación](timing-a-notification.md): describe el momento de la notificación del cliente por proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="06dea-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="06dea-125">[Garantizar una notificación de seguridad para](ensuring-a-thread-safe-notification.md)subprocesos: describe cómo garantizar la notificación de seguridad para subprocesos con MAPI.</span><span class="sxs-lookup"><span data-stu-id="06dea-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="06dea-126">[Forzar una notificación](forcing-a-notification.md): describe cómo forzar una notificación en MAPI.</span><span class="sxs-lookup"><span data-stu-id="06dea-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

