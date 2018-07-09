---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817787"
---
# <a name="imslogonadvise"></a><span data-ttu-id="a4442-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="a4442-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="a4442-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4442-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4442-105">Registra un objeto con un proveedor de almacén de mensajes para las notificaciones sobre cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a4442-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="a4442-106">El almacén de mensajes, a continuación, enviará las notificaciones sobre cambios en el objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="a4442-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a4442-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4442-107">Parameters</span></span>

 <span data-ttu-id="a4442-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4442-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="a4442-109">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a4442-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a4442-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a4442-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="a4442-111">[entrada] Un puntero al identificador de entrada del objeto sobre el que se deben generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a4442-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="a4442-112">Este objeto puede ser una carpeta, un mensaje o cualquier otro objeto en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a4442-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="a4442-113">Como alternativa, si MAPI establece el parámetro _cbEntryID_ en 0 y pasa **null** para _lpEntryID_, el receptor de notificaciones proporciona notificaciones sobre cambios en el almacén de todo el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a4442-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="a4442-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="a4442-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="a4442-115">[entrada] Una máscara de eventos de los tipos de eventos de notificación que se producen para el objeto sobre qué MAPI generará notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a4442-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="a4442-116">La máscara de los filtros específicos de los casos.</span><span class="sxs-lookup"><span data-stu-id="a4442-116">The mask filters specific cases.</span></span> <span data-ttu-id="a4442-117">Cada tipo de evento tiene una estructura asociada que contiene información adicional sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="a4442-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="a4442-118">En la siguiente tabla enumera los tipos de evento posibles junto con las estructuras de sus correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a4442-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="a4442-119">**Tipo de evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="a4442-119">**Notification event type**</span></span>|<span data-ttu-id="a4442-120">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="a4442-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4442-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="a4442-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="a4442-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="a4442-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="a4442-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="a4442-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="a4442-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="a4442-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="a4442-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="a4442-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="a4442-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="a4442-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="a4442-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="a4442-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="a4442-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="a4442-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="a4442-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="a4442-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="a4442-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="a4442-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="a4442-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="a4442-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4442-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="a4442-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="a4442-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="a4442-140">[entrada] Un puntero a un objeto de receptor advise que se llama cuando se produce un evento para el objeto de sesión acerca de qué se ha solicitado la notificación.</span><span class="sxs-lookup"><span data-stu-id="a4442-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="a4442-141">Este objeto de receptor advise ya debe existir.</span><span class="sxs-lookup"><span data-stu-id="a4442-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="a4442-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="a4442-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="a4442-143">[out] Un puntero a una variable que, tras una devolución es correcta, contiene el número de conexión para el registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="a4442-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="a4442-144">El número de conexión debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a4442-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4442-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4442-145">Return value</span></span>

<span data-ttu-id="a4442-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4442-146">S_OK</span></span> 
  
> <span data-ttu-id="a4442-147">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a4442-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a4442-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a4442-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a4442-149">La operación no se admite por MAPI o por uno o más proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="a4442-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4442-150">Notas</span><span class="sxs-lookup"><span data-stu-id="a4442-150">Remarks</span></span>

<span data-ttu-id="a4442-151">Los proveedores de almacén de mensajes implementan el método **IMSLogon::Advise** para registrar un objeto para realizar devoluciones de llamadas de notificación.</span><span class="sxs-lookup"><span data-stu-id="a4442-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="a4442-152">Cada vez que se produce un cambio en el objeto indicado, el proveedor comprueba qué bit de máscara de eventos se estableció en el parámetro _ulEventMask_ y, por lo tanto, ¿qué tipo de cambio se ha producido.</span><span class="sxs-lookup"><span data-stu-id="a4442-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="a4442-153">Si un bit está establecido, el proveedor llama al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise indicado por el parámetro _lpAdviseSink_ para notificar el evento.</span><span class="sxs-lookup"><span data-stu-id="a4442-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="a4442-154">Datos que se pasan en la estructura de notificación a la rutina de **OnNotify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="a4442-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="a4442-155">La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto, o en cualquier momento posterior.</span><span class="sxs-lookup"><span data-stu-id="a4442-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="a4442-156">En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="a4442-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="a4442-157">Para administrar de forma segura una llamada a **OnNotify** que puede suceder en un momento inoportuno, una aplicación de cliente debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="a4442-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="a4442-158">Para proporcionar notificaciones, el proveedor de almacenamiento de mensajes que implementa las necesidades de **Advise** para mantener una copia del puntero a la _lpAdviseSink_ aviso objeto receptor; Para ello, el proveedor llama al método [IUnknown:: AddRef](http://msdn.microsoft.com/es-es/library/ms691379%28v=VS.85%29.aspx) para el receptor de notificaciones mantener su puntero del objeto hasta que se cancele el registro de la notificación con una llamada al método [IMSLogon::Unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="a4442-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](http://msdn.microsoft.com/es-es/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="a4442-159">La implementación de **Advise** debe asignar a un número de conexión para el registro de la notificación y llamar a **AddRef** en este número de conexión antes de devolver en el parámetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="a4442-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="a4442-160">Proveedores de servicios pueden liberar el objeto de receptor de advise antes de que se ha cancelado el registro, pero no debe liberar el número de conexión hasta que se ha llamado al **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="a4442-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="a4442-161">Después de que se ha realizado correctamente una llamada a **Advise** y antes de que se ha llamado al **Unadvise** , es preciso preparar los proveedores para que el objeto de receptor advise que liberar.</span><span class="sxs-lookup"><span data-stu-id="a4442-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="a4442-162">Por lo tanto, un proveedor debe liberar su objeto de receptor advise después **Advise** devuelve, a menos que tenga un uso a largo plazo específico para él.</span><span class="sxs-lookup"><span data-stu-id="a4442-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="a4442-163">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="a4442-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4442-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="a4442-164">See also</span></span>



[<span data-ttu-id="a4442-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a4442-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="a4442-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a4442-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a4442-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a4442-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="a4442-168">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="a4442-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="a4442-169">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4442-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

