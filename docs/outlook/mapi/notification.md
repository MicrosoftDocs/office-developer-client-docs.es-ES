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
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818437"
---
# <a name="notification"></a><span data-ttu-id="342f7-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-103">NOTIFICATION</span></span>
 
<span data-ttu-id="342f7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="342f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="342f7-105">Contiene información sobre un evento que se ha producido y los datos que se ha visto afectados por el evento.</span><span class="sxs-lookup"><span data-stu-id="342f7-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="342f7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="342f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="342f7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="342f7-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="342f7-108">Members</span><span class="sxs-lookup"><span data-stu-id="342f7-108">Members</span></span>

<span data-ttu-id="342f7-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="342f7-109">**ulEventType**</span></span>
  
> <span data-ttu-id="342f7-110">Tipo de evento de notificación que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="342f7-110">Type of notification event that occurred.</span></span> <span data-ttu-id="342f7-111">El valor del miembro **ulEventType** corresponde a la estructura que se incluye en la unión de **info** .</span><span class="sxs-lookup"><span data-stu-id="342f7-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="342f7-112">El miembro **ulEventType** se puede establecer en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="342f7-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="342f7-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="342f7-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="342f7-114">Se ha producido un error global, como una sesión de apagado en curso.</span><span class="sxs-lookup"><span data-stu-id="342f7-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="342f7-115">El miembro de la **información** contiene una estructura [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="342f7-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="342f7-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="342f7-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="342f7-117">Se ha producido un evento interno definido por un proveedor de servicio en particular.</span><span class="sxs-lookup"><span data-stu-id="342f7-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="342f7-118">El miembro de la **información** contiene una estructura [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="342f7-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="342f7-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="342f7-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="342f7-120">Se ha entregado un mensaje a la correspondiente carpeta para la clase de mensaje de recepción y a la espera de ser procesados.</span><span class="sxs-lookup"><span data-stu-id="342f7-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="342f7-121">El miembro de la **información** contiene una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="342f7-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="342f7-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="342f7-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="342f7-123">Se ha copiado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="342f7-123">A MAPI object has been copied.</span></span> <span data-ttu-id="342f7-124">El miembro de la **información** contiene una estructura [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="342f7-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="342f7-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="342f7-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="342f7-126">Se ha creado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="342f7-126">A MAPI object has been created.</span></span> <span data-ttu-id="342f7-127">El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="342f7-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="342f7-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="342f7-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="342f7-129">Se ha eliminado un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="342f7-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="342f7-130">El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="342f7-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="342f7-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="342f7-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="342f7-132">Un objeto MAPI ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="342f7-132">A MAPI object has changed.</span></span> <span data-ttu-id="342f7-133">El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="342f7-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="342f7-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="342f7-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="342f7-135">Una dirección o el almacén de mensajes se ha movido el objeto de libro.</span><span class="sxs-lookup"><span data-stu-id="342f7-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="342f7-136">El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="342f7-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="342f7-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="342f7-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="342f7-138">Ha finalizado una operación de búsqueda y los resultados están disponibles.</span><span class="sxs-lookup"><span data-stu-id="342f7-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="342f7-139">El miembro de la **información** contiene una estructura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="342f7-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="342f7-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="342f7-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="342f7-141">Ha cambiado la información de una tabla.</span><span class="sxs-lookup"><span data-stu-id="342f7-141">Information in a table has changed.</span></span> <span data-ttu-id="342f7-142">El miembro de la **información** contiene una estructura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="342f7-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="342f7-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="342f7-143">**info**</span></span>
  
> <span data-ttu-id="342f7-144">Unión de las estructuras de notificación que describe los datos afectados para un tipo de evento específico.</span><span class="sxs-lookup"><span data-stu-id="342f7-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="342f7-145">La estructura que se incluyen en el miembro de la **información** depende del valor del miembro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="342f7-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="342f7-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="342f7-146">Remarks</span></span>

<span data-ttu-id="342f7-147">Una o más estructuras de **notificación** se pasan como parámetros de entrada con cada llamada al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de un receptor de notificaciones registrados.</span><span class="sxs-lookup"><span data-stu-id="342f7-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="342f7-148">Las estructuras de **notificación** contienen información acerca de los eventos particulares que se han producido y se describen los objetos afectados.</span><span class="sxs-lookup"><span data-stu-id="342f7-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="342f7-149">Antes de que los clientes o proveedores de servicios de recibir una notificación pueden utilizar la estructura para procesar el evento, debe comprobar el tipo de evento como se indica en el miembro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="342f7-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="342f7-150">Por ejemplo, el código de ejemplo que se muestra aquí comprobaciones para la llegada de un nuevo mensaje y al detectar un evento de este tipo, imprime la clase de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="342f7-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="342f7-151">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="342f7-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="342f7-152">**Tema**</span><span class="sxs-lookup"><span data-stu-id="342f7-152">**Topic**</span></span>|<span data-ttu-id="342f7-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="342f7-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="342f7-154">Notificación de eventos de MAPI</span><span class="sxs-lookup"><span data-stu-id="342f7-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="342f7-155">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="342f7-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="342f7-156">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="342f7-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="342f7-157">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="342f7-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="342f7-158">Admitir notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="342f7-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="342f7-159">Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="342f7-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="342f7-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="342f7-160">See also</span></span>


- [<span data-ttu-id="342f7-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="342f7-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="342f7-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="342f7-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="342f7-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="342f7-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="342f7-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="342f7-167">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="342f7-167">MAPI Structures</span></span>](mapi-structures.md)

