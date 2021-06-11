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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317314"
---
# <a name="imslogonadvise"></a><span data-ttu-id="0625b-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="0625b-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="0625b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0625b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0625b-105">Registra un objeto con un proveedor de almacén de mensajes para recibir notificaciones sobre los cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0625b-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="0625b-106">A continuación, el almacén de mensajes enviará notificaciones sobre los cambios realizados en el objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="0625b-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0625b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0625b-107">Parameters</span></span>

 <span data-ttu-id="0625b-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0625b-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="0625b-109">[in] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="0625b-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0625b-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0625b-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="0625b-111">[in] Puntero al identificador de entrada del objeto sobre qué notificaciones se deben generar.</span><span class="sxs-lookup"><span data-stu-id="0625b-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="0625b-112">Este objeto puede ser una carpeta, un mensaje o cualquier otro objeto del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0625b-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="0625b-113">Como alternativa, si MAPI establece el  _parámetro cbEntryID_ en 0 y pasa **null** para  _lpEntryID,_ el receptor de notificaciones proporciona notificaciones sobre los cambios en todo el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0625b-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="0625b-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="0625b-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="0625b-115">[in] Máscara de evento de los tipos de eventos de notificación que se producen para el objeto sobre el que MAPI generará notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0625b-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="0625b-116">La máscara filtra casos específicos.</span><span class="sxs-lookup"><span data-stu-id="0625b-116">The mask filters specific cases.</span></span> <span data-ttu-id="0625b-117">Cada tipo de evento tiene una estructura asociada que contiene información adicional sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="0625b-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="0625b-118">En la tabla siguiente se enumeran los tipos de eventos posibles junto con sus estructuras correspondientes.</span><span class="sxs-lookup"><span data-stu-id="0625b-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="0625b-119">**Tipo de evento Notification**</span><span class="sxs-lookup"><span data-stu-id="0625b-119">**Notification event type**</span></span>|<span data-ttu-id="0625b-120">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="0625b-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0625b-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="0625b-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="0625b-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="0625b-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="0625b-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="0625b-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="0625b-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="0625b-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="0625b-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="0625b-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="0625b-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="0625b-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="0625b-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="0625b-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="0625b-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="0625b-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="0625b-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="0625b-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="0625b-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0625b-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="0625b-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="0625b-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0625b-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="0625b-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="0625b-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="0625b-140">[in] Puntero a un objeto receptor de aviso al que se llamará cuando se produzca un evento para el objeto de sesión sobre el que se ha solicitado la notificación.</span><span class="sxs-lookup"><span data-stu-id="0625b-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="0625b-141">Esto aconseja que el objeto receptor ya debe existir.</span><span class="sxs-lookup"><span data-stu-id="0625b-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="0625b-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="0625b-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="0625b-143">[salida] Puntero a una variable que, tras una devolución correcta, contiene el número de conexión para el registro de notificación.</span><span class="sxs-lookup"><span data-stu-id="0625b-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="0625b-144">El número de conexión debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0625b-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0625b-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0625b-145">Return value</span></span>

<span data-ttu-id="0625b-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="0625b-146">S_OK</span></span> 
  
> <span data-ttu-id="0625b-147">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0625b-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0625b-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0625b-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0625b-149">Mapi o uno o varios proveedores de servicios no admiten la operación.</span><span class="sxs-lookup"><span data-stu-id="0625b-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0625b-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0625b-150">Remarks</span></span>

<span data-ttu-id="0625b-151">Los proveedores de almacén de mensajes implementan el método **IMSLogon::Advise** para registrar un objeto para las devoluciones de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="0625b-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="0625b-152">Siempre que se produce un cambio en el objeto indicado, el proveedor comprueba qué bit de máscara de evento se estableció en el parámetro  _ulEventMask_ y, por lo tanto, qué tipo de cambio se produjo.</span><span class="sxs-lookup"><span data-stu-id="0625b-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="0625b-153">Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor advise indicado por el parámetro  _lpAdviseSink_ para notificar el evento.</span><span class="sxs-lookup"><span data-stu-id="0625b-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="0625b-154">Los datos pasados en la estructura de notificación a la **rutina OnNotify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="0625b-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="0625b-155">La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto o en cualquier momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0625b-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="0625b-156">En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="0625b-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="0625b-157">Para controlar de forma segura una llamada a **OnNotify** que puede ocurrir en un momento inoportuna, una aplicación cliente debe usar la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="0625b-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="0625b-158">Para proporcionar notificaciones, el proveedor del almacén de mensajes que implementa **Advise** debe mantener una copia del puntero al objeto receptor _lpAdviseSink_ advise; para ello, el proveedor llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para que el receptor de notificaciones mantenga su puntero de objeto hasta que se cancele el registro de notificaciones con una llamada al método [IMSLogon::Unadvise.](imslogon-unadvise.md)</span><span class="sxs-lookup"><span data-stu-id="0625b-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="0625b-159">La **implementación advise** debe asignar un número de conexión al registro de notificación y llamar a **AddRef** en este número de conexión antes de devolverlo en el _parámetro lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="0625b-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="0625b-160">Los proveedores de servicios pueden liberar el objeto receptor de aviso antes de cancelar el registro, pero no deben liberar el número de conexión hasta que se llame **a Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="0625b-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="0625b-161">Después de que una llamada **a Advise** se haya realizado correctamente y antes de llamar a **Unadvise,** los proveedores deben estar preparados para que el objeto de receptor de aviso se liberará.</span><span class="sxs-lookup"><span data-stu-id="0625b-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="0625b-162">Por lo tanto, un proveedor debe liberar el objeto de receptor advise después de **que advise** devuelva, a menos que tenga un uso específico a largo plazo para él.</span><span class="sxs-lookup"><span data-stu-id="0625b-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="0625b-163">Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0625b-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0625b-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="0625b-164">See also</span></span>



[<span data-ttu-id="0625b-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0625b-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="0625b-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0625b-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0625b-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0625b-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="0625b-168">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="0625b-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="0625b-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0625b-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

