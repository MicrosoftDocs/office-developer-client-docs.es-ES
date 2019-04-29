---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419838"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="6ef3a-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="6ef3a-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="6ef3a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ef3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ef3a-105">Se registra para recibir una notificación de eventos especificados que afectan a la sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6ef3a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6ef3a-106">Parameters</span></span>

 <span data-ttu-id="6ef3a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6ef3a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6ef3a-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6ef3a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6ef3a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6ef3a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6ef3a-110">a Un puntero al identificador de entrada de la libreta de direcciones o del objeto de almacén de mensajes sobre qué notificaciones se deben generar, o NULL, que indica que el cliente se está registrando para recibir notificaciones sobre eventos que afectan solo a la sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="6ef3a-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="6ef3a-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="6ef3a-112">a Máscara de valores que indican los tipos de eventos de notificación en los que está interesado el cliente y deben incluirse en el registro.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="6ef3a-113">Si _lpEntryID_ es null, MAPI registra automáticamente el cliente para los eventos de error críticos que afectan solo a la sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="6ef3a-114">Cuando _lpEntryID_ apunta a un identificador de entrada, los siguientes valores son válidos para el parámetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="6ef3a-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="6ef3a-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="6ef3a-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="6ef3a-116">Registra las notificaciones sobre errores graves, como memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="6ef3a-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="6ef3a-117">fnevExtended</span></span> 
  
> <span data-ttu-id="6ef3a-118">Registra las notificaciones sobre eventos específicos de una libreta de direcciones o un proveedor de almacenamiento de mensajes determinados y sobre el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="6ef3a-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="6ef3a-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="6ef3a-120">Registra las notificaciones sobre la llegada de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="6ef3a-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="6ef3a-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="6ef3a-122">Registra las notificaciones sobre la creación de un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="6ef3a-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="6ef3a-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="6ef3a-124">Registra notificaciones sobre un objeto que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="6ef3a-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="6ef3a-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="6ef3a-126">Registra notificaciones sobre un objeto que se está eliminando.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="6ef3a-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="6ef3a-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="6ef3a-128">Registra notificaciones sobre un objeto que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="6ef3a-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="6ef3a-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="6ef3a-130">Registra notificaciones sobre un objeto que se está moviendo.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="6ef3a-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="6ef3a-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="6ef3a-132">Registra las notificaciones sobre la finalización de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="6ef3a-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="6ef3a-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="6ef3a-134">a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="6ef3a-135">Este objeto de receptor de notificaciones debe haber sido asignado ya.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="6ef3a-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="6ef3a-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="6ef3a-137">contempla Un puntero a un número distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y la sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ef3a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ef3a-138">Return value</span></span>

<span data-ttu-id="6ef3a-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ef3a-139">S_OK</span></span> 
  
> <span data-ttu-id="6ef3a-140">El registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-140">The registration was successful.</span></span>
    
<span data-ttu-id="6ef3a-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6ef3a-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="6ef3a-142">El identificador de entrada al que apunta _lpEntryID_ no representa un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="6ef3a-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6ef3a-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6ef3a-144">El proveedor de servicios responsable del identificador de entrada al que apunta _lpEntryID_ no admite el tipo de eventos especificados en el parámetro _ulEventMask_ o no admite la notificación.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="6ef3a-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6ef3a-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6ef3a-146">Ninguno de los proveedores de servicios del perfil puede controlar el identificador de entrada al que apunta _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6ef3a-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6ef3a-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ef3a-147">Remarks</span></span>

<span data-ttu-id="6ef3a-148">El método **IMAPISession:: Advise** establece una conexión entre el objeto de notificación de notificaciones del receptor del autor de la llamada, la sesión y, opcionalmente, un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="6ef3a-149">Esta conexión se usa para enviar notificaciones al receptor de notificaciones cuando se producen uno o más eventos especificados en el parámetro _ulEventMask_ en el objeto al que señala _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="6ef3a-150">Cuando _lpEntryID_ es null, el objeto de destino es la sesión y las notificaciones se envían solo para errores críticos y eventos extendidos.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="6ef3a-151">Cuando _lpEntryID_ apunta a un identificador de entrada válido, MAPI llama al \*\*\*\* método Advise del objeto de inicio de sesión que pertenece al proveedor de servicios responsable.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="6ef3a-152">Por ejemplo, si _lpEntryID_ apunta al identificador de entrada de una lista de distribución, MAPI llama al método [IABLogon:: Advise](iablogon-advise.md) del proveedor de la libreta de direcciones correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="6ef3a-153">Para enviar una notificación, el proveedor de servicios o MAPI llama al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor registrado.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="6ef3a-154">Uno de los parámetros para **BENOTIFY**, una estructura de notificación, contiene información que describe el evento específico.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6ef3a-155">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6ef3a-155">Notes to callers</span></span>

<span data-ttu-id="6ef3a-156">En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** también puede producirse en cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="6ef3a-157">Si necesita asegurarse de que las notificaciones solo se producirán en un momento determinado de un subproceso en particular, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de notificación de aviso que se pasa al método Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6ef3a-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="6ef3a-158">Para determinar cuándo un cliente ha cerrado la sesión, registre las notificaciones en su proveedor de servicios \*\*\*\* llamando a Advise con _LPENTRYID_ establecido en NULL y _cbEntryID_ establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="6ef3a-159">Cuando se produzca el cierre de sesión, recibirá una notificación de fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="6ef3a-160">Después de que una \*\*\*\* llamada a Advise se haya realizado correctamente y antes de que se haya llamado a [IMAPISession:: Unadvise](imapisession-unadvise.md) para cancelar el registro, libere el objeto de notificación de avisos a menos que tenga un uso específico a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="6ef3a-161">Para obtener información general sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6ef3a-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="6ef3a-162">Para obtener más información sobre el control de notificaciones, consulte [control](handling-notifications.md)de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6ef3a-163">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6ef3a-163">MFCMAPI reference</span></span>

<span data-ttu-id="6ef3a-164">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6ef3a-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6ef3a-165">**File**</span></span>|<span data-ttu-id="6ef3a-166">**Función**</span><span class="sxs-lookup"><span data-stu-id="6ef3a-166">**Function**</span></span>|<span data-ttu-id="6ef3a-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6ef3a-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ef3a-168">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="6ef3a-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="6ef3a-169">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="6ef3a-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="6ef3a-170">MFCMAPI usa el método **IMAPISession:: Advise** para registrarse en las notificaciones en la sesión.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ef3a-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="6ef3a-171">See also</span></span>



[<span data-ttu-id="6ef3a-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="6ef3a-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="6ef3a-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6ef3a-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="6ef3a-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6ef3a-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6ef3a-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6ef3a-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="6ef3a-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ef3a-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6ef3a-177">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="6ef3a-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6ef3a-178">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef3a-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

