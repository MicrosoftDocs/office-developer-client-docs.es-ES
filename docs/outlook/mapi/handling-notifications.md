---
title: Administrar notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fdd66e4a27209e6b80757bcf52408eb0cea43794
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816937"
---
# <a name="handling-notifications"></a><span data-ttu-id="1507d-103">Administrar notificaciones</span><span class="sxs-lookup"><span data-stu-id="1507d-103">Handling notifications</span></span>

<span data-ttu-id="1507d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1507d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1507d-105">Las notificaciones de habilitar un objeto informar a otro objeto que ha experimentado un cambio.</span><span class="sxs-lookup"><span data-stu-id="1507d-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="1507d-106">El tipo de cambio se conoce como un evento.</span><span class="sxs-lookup"><span data-stu-id="1507d-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="1507d-107">MAPI define varios eventos para el que se generan notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1507d-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="1507d-108">Normalmente, los clientes de registrar los eventos de uno o más con uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="1507d-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="1507d-109">Estos objetos se conocen como orígenes de aviso.</span><span class="sxs-lookup"><span data-stu-id="1507d-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="1507d-110">Los objetos que pueden actuar como orígenes de aviso incluyen el objeto de sesión, bajo control de MAPI o un objeto creado por un proveedor de servicios, como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1507d-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="1507d-111">El objeto informado, que se conoce como el receptor de notificaciones, contiene puede ser una implementación de la [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interfaz o el [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) de la interfaz y está dentro de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="1507d-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="1507d-112">Objetos de origen de Advise implementan un método **Advise** , que se llama a los clientes para registrar las notificaciones y un método **Unadvise** , que se llama para cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="1507d-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="1507d-113">Uno de los parámetros a **Advise** es un puntero a una implementación de **IMAPIAdviseSink** o ** IMAPIViewAdviseSink **.</span><span class="sxs-lookup"><span data-stu-id="1507d-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or ** IMAPIViewAdviseSink **.</span></span> <span data-ttu-id="1507d-114">El origen de advise se almacena en caché en este puntero para que pueda llamar [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) o uno de los métodos en **IMAPIViewAdviseSink** cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="1507d-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="1507d-115">Debido a que recibir notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes de registrarse para obtener y controlan las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1507d-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="1507d-116">Sin embargo, es opcional.</span><span class="sxs-lookup"><span data-stu-id="1507d-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1507d-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1507d-117">In this section</span></span>

- <span data-ttu-id="1507d-118">[Registrar para una notificación](registering-for-a-notification.md): se describe cómo registrar un cliente para las notificaciones como parte de su proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="1507d-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="1507d-119">[Cancelación de una notificación](canceling-a-notification.md): se describe cómo cancelar una suscripción a una notificación.</span><span class="sxs-lookup"><span data-stu-id="1507d-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="1507d-120">[Controlar la notificación del almacén de mensaje](handling-message-store-notification.md): se describe cómo registrarse para las notificaciones del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1507d-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="1507d-121">[Tener que proporcionar la notificación de la libreta de direcciones](handing-address-book-notification.md): describe cómo registrarse para obtener y controlar las notificaciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1507d-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="1507d-122">[Controlar la notificación de tabla](handling-table-notification.md): describe cómo registrarse para recibir notificaciones de la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="1507d-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="1507d-123">[Implementación de un objeto de receptor de aviso](implementing-an-advise-sink-object.md): describe cómo implementar un objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="1507d-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="1507d-124">[Una notificación de intervalos de tiempo](timing-a-notification.md): describe los intervalos de notificación de cliente por los proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="1507d-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="1507d-125">[Garantizar una notificación de subprocesos](ensuring-a-thread-safe-notification.md): describe cómo asegurar la notificación de seguros para subprocesos con MAPI.</span><span class="sxs-lookup"><span data-stu-id="1507d-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="1507d-126">[Forzar una notificación](forcing-a-notification.md): se describen los procedimientos para forzar una notificación en MAPI.</span><span class="sxs-lookup"><span data-stu-id="1507d-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

