---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415722"
---
# <a name="extended_notification"></a><span data-ttu-id="8c57e-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8c57e-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8c57e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c57e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c57e-105">Describe la información relacionada con un evento específico del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8c57e-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c57e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c57e-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c57e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c57e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="8c57e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c57e-108">Members</span></span>

 <span data-ttu-id="8c57e-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="8c57e-109">**ulEvent**</span></span>
  
> <span data-ttu-id="8c57e-110">Código de evento extendido definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8c57e-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="8c57e-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="8c57e-111">**cb**</span></span>
  
> <span data-ttu-id="8c57e-112">Recuento de bytes en los parámetros específicos del evento a los que apunta **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="8c57e-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="8c57e-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="8c57e-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="8c57e-114">Puntero a parámetros específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="8c57e-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="8c57e-115">El tipo de parámetros que se usan depende del valor del **miembro ulEvent;** estos parámetros los documenta el proveedor que emitió el evento.</span><span class="sxs-lookup"><span data-stu-id="8c57e-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8c57e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c57e-116">Remarks</span></span>

<span data-ttu-id="8c57e-117">La **EXTENDED_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de** información de la [estructura notification.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="8c57e-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8c57e-118">Cuando el miembro  **de** información de una estructura notification contiene una estructura **EXTENDED_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="8c57e-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="8c57e-119">El evento extendido lo define un proveedor de servicios para representar un tipo de cambio que no puede estar cubierto por ninguno de los demás eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="8c57e-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="8c57e-120">Solo los clientes que sepan antes de registrar que un proveedor de servicios admite un evento extendido pueden registrarse para ese evento.</span><span class="sxs-lookup"><span data-stu-id="8c57e-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="8c57e-121">No es posible que los clientes determinen sin conocimientos avanzados si un proveedor de servicios admite un evento extendido.</span><span class="sxs-lookup"><span data-stu-id="8c57e-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="8c57e-122">Si un proveedor de servicios admite un evento extendido, muestra cómo controlar dicho evento cuando se recibe.</span><span class="sxs-lookup"><span data-stu-id="8c57e-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="8c57e-123">La sesión envía una notificación extendida cuando un cliente cierra sesión.</span><span class="sxs-lookup"><span data-stu-id="8c57e-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="8c57e-124">Regístrese para esta notificación llamando a [IMAPISession::Advise](imapisession-advise.md) con el parámetro  _lpEntryID_ establecido en NULL y el parámetro  _cbEntryID_ establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="8c57e-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="8c57e-125">Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c57e-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8c57e-126">**Tema**</span><span class="sxs-lookup"><span data-stu-id="8c57e-126">**Topic**</span></span>|<span data-ttu-id="8c57e-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c57e-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c57e-128">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="8c57e-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8c57e-129">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="8c57e-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8c57e-130">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="8c57e-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8c57e-131">Discusión sobre cómo deben administrarse las notificaciones los clientes.</span><span class="sxs-lookup"><span data-stu-id="8c57e-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8c57e-132">Notificación de eventos de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="8c57e-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8c57e-133">Discusión sobre cómo los proveedores de servicios pueden usar [los métodos IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c57e-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c57e-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c57e-134">See also</span></span>



[<span data-ttu-id="8c57e-135">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="8c57e-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="8c57e-136">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8c57e-136">MAPI Structures</span></span>](mapi-structures.md)

