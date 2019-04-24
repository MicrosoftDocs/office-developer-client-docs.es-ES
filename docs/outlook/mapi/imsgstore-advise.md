---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317328"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="f6d6f-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="f6d6f-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="f6d6f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6d6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6d6f-105">Se registra para recibir una notificación de eventos especificados que afectan al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f6d6f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f6d6f-106">Parameters</span></span>

 <span data-ttu-id="f6d6f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f6d6f-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f6d6f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f6d6f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f6d6f-110">a Un puntero al identificador de entrada de la carpeta o mensaje sobre qué notificaciones se deben generar o **null**.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="f6d6f-111">Si _lpEntryID_ se establece en null, **Advise** registra las notificaciones en todo el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="f6d6f-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="f6d6f-113">a Máscara de valores que indican los tipos de eventos de notificación en los que está interesado el autor de la llamada y que deben incluirse en el registro.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="f6d6f-114">Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="f6d6f-115">Los siguientes son valores válidos para el parámetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="f6d6f-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="f6d6f-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="f6d6f-117">Registra las notificaciones sobre errores graves, como memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="f6d6f-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="f6d6f-119">Registra notificaciones sobre eventos específicos del proveedor de almacén de mensajes en particular.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="f6d6f-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="f6d6f-121">Registra las notificaciones sobre la llegada de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="f6d6f-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="f6d6f-123">Registra las notificaciones sobre la creación de una nueva carpeta o mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="f6d6f-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="f6d6f-125">Registra notificaciones sobre una carpeta o un mensaje que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="f6d6f-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="f6d6f-127">Registra notificaciones sobre una carpeta o un mensaje que se está eliminando.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="f6d6f-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="f6d6f-129">Registra notificaciones sobre una carpeta o un mensaje que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="f6d6f-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="f6d6f-131">Registra notificaciones sobre una carpeta o un mensaje que se está moviendo.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="f6d6f-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="f6d6f-133">Registra las notificaciones sobre la finalización de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="f6d6f-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f6d6f-135">a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f6d6f-136">Este objeto de receptor de notificaciones debe haber sido asignado ya.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="f6d6f-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="f6d6f-138">contempla Un puntero a un número distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y la sesión.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="f6d6f-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f6d6f-140">a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f6d6f-141">Este objeto de receptor de notificaciones debe haber sido asignado ya.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="f6d6f-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f6d6f-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="f6d6f-143">contempla Un puntero a un número de conexión distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6d6f-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6d6f-144">Return value</span></span>

<span data-ttu-id="f6d6f-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6d6f-145">S_OK</span></span> 
  
> <span data-ttu-id="f6d6f-146">El registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-146">The registration was successful.</span></span>
    
<span data-ttu-id="f6d6f-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f6d6f-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f6d6f-148">El proveedor de almacenamiento de mensajes no admite el registro para la notificación a través del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6d6f-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6d6f-149">Remarks</span></span>

<span data-ttu-id="f6d6f-150">El método **IMsgStore:: Advise** establece una conexión entre el objeto de notificación de notificaciones del receptor del autor de la llamada y el almacén de mensajes o un objeto en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="f6d6f-151">Esta conexión se usa para enviar notificaciones al receptor de notificaciones cuando uno o más eventos, tal como se especifica en el parámetro _ulEventMask_ , se producen en el objeto de origen Advise.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="f6d6f-152">Cuando el parámetro _lpEntryID_ apunta a un identificador de entrada válido, el origen Advise es el objeto identificado por este identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="f6d6f-153">Cuando _lpEntryID_ es null, el origen de Advise es el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="f6d6f-154">Para enviar una notificación, el proveedor de almacenamiento de mensajes o MAPI llama al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor registrado.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="f6d6f-155">Uno de los parámetros para **BENOTIFY**, una estructura de notificación, contiene información que describe el evento específico.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f6d6f-156">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="f6d6f-156">Notes to implementers</span></span>

<span data-ttu-id="f6d6f-157">Puede admitir la notificación con o sin ayuda de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="f6d6f-158">MAPI tiene tres métodos de objeto de soporte para ayudar a los proveedores de servicios a implementar la notificación: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport:: Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="f6d6f-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="f6d6f-159">Si decide usar los métodos de compatibilidad con MAPI, llame a **subscribe** cuando se llame al método Advise y suelte el puntero _lpAdviseSink_ . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f6d6f-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="f6d6f-160">Si opta por admitir la notificación usted mismo, llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para conservar una copia de este puntero.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="f6d6f-161">Mantenga esta copia hasta que se llame al método [IMsgStore:: Unadvise](imsgstore-unadvise.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="f6d6f-162">Independientemente de cómo se admita la notificación, asigne un número de conexión distinto de cero al registro de notificaciones y devuelva el parámetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="f6d6f-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f6d6f-163">No libere este número de conexión hasta que se haya llamado a **Unadvise** y haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6d6f-164">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f6d6f-164">Notes to callers</span></span>

<span data-ttu-id="f6d6f-165">En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** también puede producirse en cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="f6d6f-166">Si tiene la certeza de que las notificaciones solo se producen en un momento determinado en un determinado subproceso, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de notificación de aviso que pasa a Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f6d6f-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="f6d6f-167">Después de llamar a **Advise** correctamente y antes \*\*\*\* de llamar a Unadvise para cancelar el registro, prepárese para que se publique el objeto receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="f6d6f-168">Debe liberar su objeto de notificación de notificaciones después de que se devuelva **Advise** a menos que tenga un uso específico a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f6d6f-169">Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f6d6f-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="f6d6f-170">Para obtener más información sobre el control de notificaciones, consulte [control](handling-notifications.md)de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6d6f-171">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6d6f-171">MFCMAPI reference</span></span>

<span data-ttu-id="f6d6f-172">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6d6f-173">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f6d6f-173">**File**</span></span>|<span data-ttu-id="f6d6f-174">**Función**</span><span class="sxs-lookup"><span data-stu-id="f6d6f-174">**Function**</span></span>|<span data-ttu-id="f6d6f-175">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f6d6f-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6d6f-176">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="f6d6f-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="f6d6f-177">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="f6d6f-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="f6d6f-178">MFCMAPI usa el método **IMsgStore:: Advise** para registrarse en las notificaciones en todo el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d6f-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6d6f-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6d6f-179">See also</span></span>



[<span data-ttu-id="f6d6f-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f6d6f-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f6d6f-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f6d6f-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f6d6f-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f6d6f-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="f6d6f-183">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="f6d6f-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f6d6f-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f6d6f-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="f6d6f-185">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="f6d6f-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

