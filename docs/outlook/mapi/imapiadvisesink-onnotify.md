---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407364"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="e150c-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e150c-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="e150c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e150c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e150c-105">Responde a una notificación realizando una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="e150c-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="e150c-106">Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="e150c-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="e150c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e150c-107">Parameters</span></span>

 <span data-ttu-id="e150c-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="e150c-108">_cNotif_</span></span>
  
> <span data-ttu-id="e150c-109">[entrada] Recuento de estructuras [notification](notification.md) a las que apunta el _parámetro lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="e150c-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="e150c-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="e150c-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="e150c-111">[entrada] Puntero a una o más estructuras **de notificación** que proporcionan información sobre los eventos que se han producido.</span><span class="sxs-lookup"><span data-stu-id="e150c-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e150c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e150c-112">Return value</span></span>

<span data-ttu-id="e150c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e150c-113">S_OK</span></span> 
  
> <span data-ttu-id="e150c-114">La notificación se procesó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e150c-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e150c-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e150c-115">Remarks</span></span>

<span data-ttu-id="e150c-116">El proceso de notificación se inicia cuando un cliente o MAPI realiza una llamada al método **Advise** de un proveedor de servicios para registrarse para recibir una notificación de un tipo determinado para un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="e150c-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="e150c-117">Uno de los parámetros del método **Advise** es un puntero a un objeto receptor de aviso que implementa la interfaz [IMAPIAdviseSink.](imapiadvisesinkiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="e150c-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="e150c-118">Cuando se produce un evento en el objeto de destino que corresponde a la notificación registrada, el proveedor de servicios, ya sea directa o indirectamente a través de MAPI, llama al método **OnNotify** del receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="e150c-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="e150c-119">La llamada a **OnNotify** puede producirse durante la llamada MAPI que está causando el evento o en algún momento posterior.</span><span class="sxs-lookup"><span data-stu-id="e150c-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="e150c-120">En sistemas que admiten varios subprocesos de ejecución, se puede llamar a **OnNotify** en el mismo subproceso que se usó para el registro o en un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="e150c-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="e150c-121">Los clientes pueden asegurarse de que la llamada **OnNotify** se realiza en el mismo subproceso usado para llamar a **Advise** mediante la creación del receptor de avisos que pasan a **Advise** con la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="e150c-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="e150c-122">El  _parámetro lpNotifications_ apunta a una o más estructuras **de notificación** que describen lo que ha cambiado durante el evento.</span><span class="sxs-lookup"><span data-stu-id="e150c-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="e150c-123">Hay un tipo diferente de estructura **de** notificación para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="e150c-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="e150c-124">En la tabla siguiente se enumeran los valores que se usan para representar los posibles tipos de eventos y las estructuras asociadas a cada valor:</span><span class="sxs-lookup"><span data-stu-id="e150c-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="e150c-125">**Tipo de evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="e150c-125">**Notification event type**</span></span>|<span data-ttu-id="e150c-126">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="e150c-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e150c-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="e150c-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="e150c-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="e150c-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="e150c-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="e150c-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="e150c-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="e150c-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="e150c-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e150c-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="e150c-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="e150c-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e150c-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e150c-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="e150c-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e150c-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="e150c-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="e150c-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e150c-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="e150c-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="e150c-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e150c-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="e150c-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="e150c-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="e150c-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e150c-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="e150c-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="e150c-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="e150c-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="e150c-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e150c-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="e150c-147">Para obtener más información acerca de cómo configurar y detener notificaciones, vea las entradas de referencia de los métodos **Advise** y **Unadvise** para cualquiera de las siguientes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e150c-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="e150c-148">Para obtener información general sobre el proceso de notificación, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e150c-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e150c-149">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e150c-149">Notes to implementers</span></span>

<span data-ttu-id="e150c-150">La **implementación de OnNotify** normalmente constará de uno o más bloques de código para cada tipo de notificación que esperas recibir.</span><span class="sxs-lookup"><span data-stu-id="e150c-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="e150c-151">Dentro de estos bloques de código, realiza las tareas que consideres necesarias como respuesta a la notificación.</span><span class="sxs-lookup"><span data-stu-id="e150c-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="e150c-152">Por ejemplo, supongamos que se registra para recibir **notificaciones fnevObjectModified** en una carpeta que se incluye en una presentación de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e150c-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="e150c-153">En el bloque de código que incluyas en el método **OnNotify** para controlar las notificaciones **fnevObjectModified,** puedes enviar un mensaje de Windows al cuadro de diálogo para solicitar una presentación actualizada.</span><span class="sxs-lookup"><span data-stu-id="e150c-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="e150c-154">No modifique ni libre la estructura **de notificación** pasada a **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="e150c-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="e150c-155">Los datos de la estructura solo son válidos hasta que **OnNotify devuelve.**</span><span class="sxs-lookup"><span data-stu-id="e150c-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e150c-156">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e150c-156">Notes to callers</span></span>

<span data-ttu-id="e150c-157">Cuando se producen cambios en varios objetos, puede notificar a un receptor de aviso registrado en una sola llamada a **OnNotify** o en varias llamadas en función de las restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="e150c-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="e150c-158">Esto es así independientemente de si los cambios son el resultado de una o varias llamadas de método.</span><span class="sxs-lookup"><span data-stu-id="e150c-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="e150c-159">Por ejemplo, una llamada a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) puede afectar a varios mensajes y carpetas.</span><span class="sxs-lookup"><span data-stu-id="e150c-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="e150c-160">Como proveedor de almacén de mensajes, puede realizar una llamada a **OnNotify** con un tipo de evento **fnevObjectModified** para la carpeta de destino o varias llamadas, una para cada mensaje que afecte a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e150c-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="e150c-161">De forma similar, si un cliente realiza llamadas repetidas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), estas llamadas se pueden combinar en un evento **fnevObjectModified** para la carpeta o separarse en eventos **fnevObjectCreated** individuales para cada mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="e150c-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="e150c-162">Para obtener más información sobre cómo y cuándo generar notificaciones, vea [Notificación de eventos](event-notification-in-mapi.md) en MAPI y Notificación de eventos de soporte [técnico.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="e150c-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e150c-163">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e150c-163">MFCMAPI reference</span></span>

<span data-ttu-id="e150c-164">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e150c-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e150c-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e150c-165">**File**</span></span>|<span data-ttu-id="e150c-166">**Función**</span><span class="sxs-lookup"><span data-stu-id="e150c-166">**Function**</span></span>|<span data-ttu-id="e150c-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e150c-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e150c-168">AdviseSink.h y AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="e150c-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="e150c-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="e150c-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="e150c-170">La clase CAdviseSink se implementa para controlar todas las notificaciones en MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e150c-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e150c-171">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e150c-171">See also</span></span>



[<span data-ttu-id="e150c-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e150c-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="e150c-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e150c-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e150c-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="e150c-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="e150c-175">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="e150c-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e150c-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e150c-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="e150c-177">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e150c-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

