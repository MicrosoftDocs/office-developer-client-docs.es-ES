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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817446"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="7b531-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="7b531-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="7b531-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b531-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b531-105">Se registra para recibir notificaciones de los eventos que afectan a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7b531-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7b531-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b531-106">Parameters</span></span>

 <span data-ttu-id="7b531-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7b531-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7b531-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7b531-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7b531-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7b531-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7b531-110">[entrada] Un puntero al identificador de entrada de la libreta de direcciones o mensaje almacén de objeto sobre el que se deben generar notificaciones o NULL, que indica que el cliente se está registrando para recibir notificaciones sobre los eventos que afectan a la sesión de sólo.</span><span class="sxs-lookup"><span data-stu-id="7b531-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="7b531-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7b531-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="7b531-112">[entrada] Una máscara de valores que se indican los tipos de eventos de notificación que el cliente está interesado en y se debe incluir en el registro.</span><span class="sxs-lookup"><span data-stu-id="7b531-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="7b531-113">Si _lpEntryID_ es NULL, MAPI registra automáticamente el cliente para los eventos de error crítico que afectan a sólo la sesión.</span><span class="sxs-lookup"><span data-stu-id="7b531-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="7b531-114">Cuando _lpEntryID_ apunta a un identificador de entrada, los valores siguientes son válidos para el parámetro _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="7b531-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="7b531-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="7b531-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="7b531-116">Registra las notificaciones acerca de los errores graves, como memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="7b531-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="7b531-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="7b531-117">fnevExtended</span></span> 
  
> <span data-ttu-id="7b531-118">Registra las notificaciones sobre los eventos específicos de una libreta de direcciones determinada o un mensaje de proveedor de almacén y acerca de la sesión de apagado.</span><span class="sxs-lookup"><span data-stu-id="7b531-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="7b531-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="7b531-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="7b531-120">Registra las notificaciones sobre la llegada de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="7b531-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="7b531-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="7b531-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="7b531-122">Registra las notificaciones sobre la creación de un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="7b531-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="7b531-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="7b531-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="7b531-124">Registra las notificaciones sobre un objeto que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="7b531-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="7b531-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="7b531-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="7b531-126">Registra las notificaciones sobre un objeto que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="7b531-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="7b531-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="7b531-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="7b531-128">Registra las notificaciones sobre un objeto que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="7b531-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="7b531-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="7b531-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="7b531-130">Registra las notificaciones sobre un objeto que se va a mover.</span><span class="sxs-lookup"><span data-stu-id="7b531-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="7b531-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="7b531-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="7b531-132">Registra las notificaciones sobre la finalización de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7b531-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="7b531-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7b531-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7b531-134">[entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7b531-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="7b531-135">Este objeto de receptor advise debe ya se han asignado.</span><span class="sxs-lookup"><span data-stu-id="7b531-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="7b531-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7b531-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="7b531-137">[out] Un puntero a un número distinto de cero que representa la conexión entre el autor de la llamada de aviso objeto receptor y la sesión.</span><span class="sxs-lookup"><span data-stu-id="7b531-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b531-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b531-138">Return value</span></span>

<span data-ttu-id="7b531-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b531-139">S_OK</span></span> 
  
> <span data-ttu-id="7b531-140">El registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7b531-140">The registration was successful.</span></span>
    
<span data-ttu-id="7b531-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7b531-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7b531-142">El identificador de entrada que señala _lpEntryID_ no representa un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="7b531-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="7b531-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7b531-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7b531-144">El proveedor de servicio responsable para el identificador de entrada que señala _lpEntryID_ no admite el tipo de eventos especificado en el parámetro _ulEventMask_ o no admite la notificación.</span><span class="sxs-lookup"><span data-stu-id="7b531-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="7b531-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7b531-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7b531-146">El identificador de entrada que señala _lpEntryID_ no se puede controlar mediante cualquiera de los proveedores de servicios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="7b531-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7b531-147">Notas</span><span class="sxs-lookup"><span data-stu-id="7b531-147">Remarks</span></span>

<span data-ttu-id="7b531-148">El método **IMAPISession::Advise** establece una conexión entre el autor de la llamada del objeto de receptor, la sesión y, opcionalmente, un proveedor de servicios de avisos.</span><span class="sxs-lookup"><span data-stu-id="7b531-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="7b531-149">Esta conexión se utiliza para enviar las notificaciones para el receptor de notificaciones cuando uno o más eventos especificados en el parámetro _ulEventMask_ se producen en el objeto al que señala por _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="7b531-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="7b531-150">Cuando _lpEntryID_ es NULL, el objeto de destino es la sesión y se envían únicamente para los errores críticos y eventos extendidos.</span><span class="sxs-lookup"><span data-stu-id="7b531-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="7b531-151">Cuando _lpEntryID_ apunta a un identificador de entrada válido, MAPI llama al método **Advise** del objeto de inicio de sesión que pertenece al proveedor de servicios responsable.</span><span class="sxs-lookup"><span data-stu-id="7b531-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="7b531-152">Por ejemplo, si _lpEntryID_ puntos para el identificador de entrada de una lista de distribución, MAPI llama (método [IABLogon::Advise](iablogon-advise.md) ) del proveedor de la libreta de dirección adecuada.</span><span class="sxs-lookup"><span data-stu-id="7b531-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="7b531-153">Para enviar una notificación, el proveedor de servicios o MAPI llama (método) [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor advise registrados.</span><span class="sxs-lookup"><span data-stu-id="7b531-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="7b531-154">Uno de los parámetros para **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.</span><span class="sxs-lookup"><span data-stu-id="7b531-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b531-155">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7b531-155">Notes to callers</span></span>

<span data-ttu-id="7b531-156">En los sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="7b531-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="7b531-157">Si necesita garantía de que las notificaciones se producen sólo en un momento determinado en un subproceso concreto, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de receptor advise que se pasa al método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="7b531-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="7b531-158">Para determinar cuando un cliente ha cerrado la sesión, registrar para las notificaciones en su proveedor de servicios mediante una llamada a **Advise** con _lpEntryID_ establecido en NULL y _cbEntryID_ establece en 0.</span><span class="sxs-lookup"><span data-stu-id="7b531-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="7b531-159">Cuando se produce el cierre de sesión, recibirá una notificación de fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="7b531-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="7b531-160">Después de que se ha realizado correctamente una llamada a **Advise** y antes de que se ha llamado a [IMAPISession::Unadvise](imapisession-unadvise.md) para cancelar el registro, versión de su objeto de receptor advise a menos que tengan un uso específico a largo plazo para él.</span><span class="sxs-lookup"><span data-stu-id="7b531-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="7b531-161">Para obtener información general del proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7b531-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="7b531-162">Para obtener más información acerca de cómo controlar las notificaciones, vea [Controlar notificaciones](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7b531-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b531-163">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b531-163">MFCMAPI reference</span></span>

<span data-ttu-id="7b531-164">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7b531-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b531-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7b531-165">**File**</span></span>|<span data-ttu-id="7b531-166">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="7b531-166">**Function**</span></span>|<span data-ttu-id="7b531-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7b531-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b531-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="7b531-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="7b531-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="7b531-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="7b531-170">MFCMAPI utiliza el método **IMAPISession::Advise** para registrar para notificaciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="7b531-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b531-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="7b531-171">See also</span></span>



[<span data-ttu-id="7b531-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="7b531-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="7b531-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7b531-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7b531-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7b531-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7b531-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7b531-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="7b531-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b531-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="7b531-177">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7b531-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7b531-178">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="7b531-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

