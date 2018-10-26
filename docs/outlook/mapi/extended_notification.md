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
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580645"
---
# <a name="extendednotification"></a><span data-ttu-id="d6b62-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d6b62-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="d6b62-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6b62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6b62-105">Describe la información que se relaciona con un evento que es específico del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="d6b62-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6b62-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d6b62-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6b62-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6b62-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="d6b62-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6b62-108">Members</span></span>

 <span data-ttu-id="d6b62-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="d6b62-109">**ulEvent**</span></span>
  
> <span data-ttu-id="d6b62-110">Código de evento extendido que está definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d6b62-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="d6b62-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="d6b62-111">**cb**</span></span>
  
> <span data-ttu-id="d6b62-112">Recuento de bytes en los parámetros específicos del evento que señala **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="d6b62-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="d6b62-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="d6b62-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="d6b62-114">Puntero a los parámetros específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="d6b62-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="d6b62-115">El tipo de parámetros que se usan depende del valor del miembro **ulEvent** ; Estos parámetros se documentan por el proveedor que ha emitido el evento.</span><span class="sxs-lookup"><span data-stu-id="d6b62-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6b62-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6b62-116">Remarks</span></span>

<span data-ttu-id="d6b62-117">La estructura **EXTENDED_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b62-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="d6b62-118">Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **EXTENDED_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="d6b62-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="d6b62-119">El evento extendido está definido por un proveedor de servicios para representar un tipo de cambio que no se debe estar cubierto por cualquiera de los demás eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="d6b62-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="d6b62-120">Solo los clientes que saber antes de que registran que un proveedor de servicios admite un evento extendido pueden registrar para dicho evento.</span><span class="sxs-lookup"><span data-stu-id="d6b62-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="d6b62-121">No es posible para los clientes determinar sin conocimientos avanzados si un proveedor de servicios admite un evento extendido.</span><span class="sxs-lookup"><span data-stu-id="d6b62-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="d6b62-122">Si un proveedor de servicios admite un evento extendido, se muestra cómo controlar un evento cuando se recibe.</span><span class="sxs-lookup"><span data-stu-id="d6b62-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="d6b62-123">Se envía una notificación extendida por la sesión cuando un cliente cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="d6b62-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="d6b62-124">Registre esta notificación mediante una llamada a [IMAPISession::Advise](imapisession-advise.md) con el parámetro _lpEntryID_ establecido en NULL y el parámetro de _cbEntryID_ que se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="d6b62-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="d6b62-125">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d6b62-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d6b62-126">**Tema**</span><span class="sxs-lookup"><span data-stu-id="d6b62-126">**Topic**</span></span>|<span data-ttu-id="d6b62-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6b62-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6b62-128">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b62-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d6b62-129">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="d6b62-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d6b62-130">Administrar notificaciones</span><span class="sxs-lookup"><span data-stu-id="d6b62-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d6b62-131">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d6b62-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d6b62-132">Compatibilidad con la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="d6b62-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d6b62-133">Explicación de cómo los proveedores de servicios pueden usar los métodos [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d6b62-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6b62-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6b62-134">See also</span></span>



[<span data-ttu-id="d6b62-135">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="d6b62-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="d6b62-136">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b62-136">MAPI Structures</span></span>](mapi-structures.md)

