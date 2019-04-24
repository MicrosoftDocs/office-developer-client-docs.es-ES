---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280102"
---
# <a name="notification"></a><span data-ttu-id="42842-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-103">NOTIFICATION</span></span>
 
<span data-ttu-id="42842-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42842-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42842-105">Contiene información sobre un evento que se ha producido y los datos afectados por el evento.</span><span class="sxs-lookup"><span data-stu-id="42842-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42842-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="42842-106">Header file:</span></span>  <br/> |<span data-ttu-id="42842-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42842-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="42842-108">Members</span><span class="sxs-lookup"><span data-stu-id="42842-108">Members</span></span>

<span data-ttu-id="42842-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="42842-109">**ulEventType**</span></span>
  
> <span data-ttu-id="42842-110">Tipo de evento de notificación que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="42842-110">Type of notification event that occurred.</span></span> <span data-ttu-id="42842-111">El valor del miembro **ulEventType** corresponde a la estructura que se incluye en la **información** de la Unión.</span><span class="sxs-lookup"><span data-stu-id="42842-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="42842-112">El miembro **ulEventType** se puede establecer en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="42842-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="42842-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="42842-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="42842-114">Se ha producido un error global, como que se apagó la sesión en curso.</span><span class="sxs-lookup"><span data-stu-id="42842-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="42842-115">El miembro **info** contiene una estructura [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="42842-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="42842-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="42842-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="42842-117">Se ha producido un evento interno definido por un proveedor de servicios en particular.</span><span class="sxs-lookup"><span data-stu-id="42842-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="42842-118">El miembro **info** contiene una estructura [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="42842-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="42842-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="42842-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="42842-120">Se entregó un mensaje a la carpeta de recepción adecuada para la clase de mensaje y está a la espera de ser procesado.</span><span class="sxs-lookup"><span data-stu-id="42842-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="42842-121">El miembro **info** contiene una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="42842-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="42842-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="42842-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="42842-123">Se ha copiado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="42842-123">A MAPI object has been copied.</span></span> <span data-ttu-id="42842-124">El miembro **info** contiene una estructura [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="42842-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="42842-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="42842-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="42842-126">Se ha creado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="42842-126">A MAPI object has been created.</span></span> <span data-ttu-id="42842-127">El miembro **info** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="42842-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="42842-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="42842-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="42842-129">Se ha eliminado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="42842-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="42842-130">El miembro **info** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="42842-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="42842-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="42842-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="42842-132">Un objeto MAPI ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="42842-132">A MAPI object has changed.</span></span> <span data-ttu-id="42842-133">El miembro **info** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="42842-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="42842-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="42842-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="42842-135">Se movió un objeto de la libreta de direcciones o de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="42842-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="42842-136">El miembro **info** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="42842-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="42842-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="42842-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="42842-138">Una operación de búsqueda ha finalizado y los resultados están disponibles.</span><span class="sxs-lookup"><span data-stu-id="42842-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="42842-139">El miembro **info** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="42842-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="42842-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="42842-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="42842-141">La información de una tabla ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="42842-141">Information in a table has changed.</span></span> <span data-ttu-id="42842-142">El miembro **info** contiene una estructura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="42842-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="42842-143">**info**</span><span class="sxs-lookup"><span data-stu-id="42842-143">**info**</span></span>
  
> <span data-ttu-id="42842-144">Unión de estructuras de notificación que describen los datos afectados para un tipo concreto de evento.</span><span class="sxs-lookup"><span data-stu-id="42842-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="42842-145">La estructura que se incluye en el miembro **info** depende del valor del miembro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="42842-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42842-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42842-146">Remarks</span></span>

<span data-ttu-id="42842-147">Una o más estructuras de **notificación** se pasan como parámetros de entrada con cada llamada a un método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) del receptor registrado.</span><span class="sxs-lookup"><span data-stu-id="42842-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="42842-148">Las estructuras de **notificación** contienen información sobre los eventos concretos que se han producido y describen los objetos afectados.</span><span class="sxs-lookup"><span data-stu-id="42842-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="42842-149">Antes de que los clientes o proveedores de servicios que reciben una notificación puedan usar la estructura para procesar el evento, deben comprobar el tipo de evento como se indica en el miembro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="42842-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="42842-150">Por ejemplo, el ejemplo de código que se muestra aquí comprueba la llegada de un nuevo mensaje y, después de detectar un evento de este tipo, imprime la clase de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="42842-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="42842-151">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="42842-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="42842-152">**Tema**</span><span class="sxs-lookup"><span data-stu-id="42842-152">**Topic**</span></span>|<span data-ttu-id="42842-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42842-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42842-154">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="42842-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="42842-155">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="42842-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="42842-156">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="42842-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="42842-157">Descripción de cómo deben administrar los clientes las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="42842-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="42842-158">Admitir notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="42842-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="42842-159">Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="42842-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42842-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="42842-160">See also</span></span>


- [<span data-ttu-id="42842-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="42842-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="42842-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="42842-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="42842-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="42842-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42842-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="42842-167">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="42842-167">MAPI Structures</span></span>](mapi-structures.md)

