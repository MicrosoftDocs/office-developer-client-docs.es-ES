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
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19816789"
---
# <a name="extendednotification"></a><span data-ttu-id="8c158-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8c158-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8c158-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c158-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c158-105">Describe la información que se relaciona con un evento que es específico del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="8c158-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c158-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c158-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c158-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c158-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="8c158-108">Members</span><span class="sxs-lookup"><span data-stu-id="8c158-108">Members</span></span>

 <span data-ttu-id="8c158-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="8c158-109">**ulEvent**</span></span>
  
> <span data-ttu-id="8c158-110">Código de evento extendido que está definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8c158-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="8c158-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="8c158-111">**cb**</span></span>
  
> <span data-ttu-id="8c158-112">Recuento de bytes en los parámetros específicos del evento que señala **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="8c158-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="8c158-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="8c158-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="8c158-114">Puntero a los parámetros específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="8c158-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="8c158-115">El tipo de parámetros que se usan depende del valor del miembro **ulEvent** ; Estos parámetros se documentan por el proveedor que ha emitido el evento.</span><span class="sxs-lookup"><span data-stu-id="8c158-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8c158-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c158-116">Remarks</span></span>

<span data-ttu-id="8c158-117">La estructura **EXTENDED_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="8c158-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8c158-118">Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **EXTENDED_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="8c158-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="8c158-119">El evento extendido está definido por un proveedor de servicios para representar un tipo de cambio que no se debe estar cubierto por cualquiera de los demás eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="8c158-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="8c158-120">Solo los clientes que saber antes de que registran que un proveedor de servicios admite un evento extendido pueden registrar para dicho evento.</span><span class="sxs-lookup"><span data-stu-id="8c158-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="8c158-121">No es posible para los clientes determinar sin conocimientos avanzados si un proveedor de servicios admite un evento extendido.</span><span class="sxs-lookup"><span data-stu-id="8c158-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="8c158-122">Si un proveedor de servicios admite un evento extendido, se muestra cómo controlar un evento cuando se recibe.</span><span class="sxs-lookup"><span data-stu-id="8c158-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="8c158-123">Se envía una notificación extendida por la sesión cuando un cliente cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="8c158-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="8c158-124">Registre esta notificación mediante una llamada a [IMAPISession::Advise](imapisession-advise.md) con el parámetro _lpEntryID_ establecido en NULL y el parámetro de _cbEntryID_ que se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="8c158-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="8c158-125">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8c158-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8c158-126">**Tema**</span><span class="sxs-lookup"><span data-stu-id="8c158-126">**Topic**</span></span>|<span data-ttu-id="8c158-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c158-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c158-128">Notificación de eventos de MAPI</span><span class="sxs-lookup"><span data-stu-id="8c158-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8c158-129">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="8c158-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8c158-130">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="8c158-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8c158-131">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c158-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8c158-132">Admitir notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="8c158-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8c158-133">Explicación de cómo los proveedores de servicios pueden usar los métodos [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c158-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c158-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c158-134">See also</span></span>



[<span data-ttu-id="8c158-135">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="8c158-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="8c158-136">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8c158-136">MAPI Structures</span></span>](mapi-structures.md)

