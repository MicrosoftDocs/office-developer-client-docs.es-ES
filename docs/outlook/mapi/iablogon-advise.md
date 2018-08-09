---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817109"
---
# <a name="iablogonadvise"></a><span data-ttu-id="528e1-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="528e1-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="528e1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="528e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="528e1-105">Registra el autor de la llamada para recibir notificaciones de los eventos que afectan a un contenedor, usuario o lista de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="528e1-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="528e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="528e1-106">Parameters</span></span>

 <span data-ttu-id="528e1-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="528e1-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="528e1-108">[entrada] El número de bytes en el identificador de entrada indicada por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="528e1-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="528e1-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="528e1-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="528e1-110">[entrada] Un puntero al identificador de entrada del objeto sobre el que se deben generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="528e1-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="528e1-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="528e1-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="528e1-112">[entrada] Una máscara de bits de valores que se indican los tipos de eventos de notificación que el autor de la llamada está interesado en y se debe incluir en el registro.</span><span class="sxs-lookup"><span data-stu-id="528e1-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="528e1-113">Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="528e1-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="528e1-114">En la siguiente tabla se enumera los valores válidos para el parámetro _ulEventMask_ y las estructuras de asociado a cada valor.</span><span class="sxs-lookup"><span data-stu-id="528e1-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="528e1-115">**Tipo de evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="528e1-115">**Notification event type**</span></span>|<span data-ttu-id="528e1-116">**Estructura de **notificación** correspondiente**</span><span class="sxs-lookup"><span data-stu-id="528e1-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="528e1-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="528e1-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="528e1-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="528e1-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="528e1-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="528e1-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="528e1-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="528e1-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="528e1-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="528e1-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="528e1-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="528e1-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="528e1-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="528e1-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="528e1-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="528e1-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="528e1-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="528e1-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="528e1-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="528e1-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="528e1-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="528e1-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="528e1-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="528e1-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="528e1-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="528e1-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="528e1-130">[entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="528e1-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="528e1-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="528e1-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="528e1-132">[out] Un puntero a un valor distinto de cero que representa el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="528e1-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="528e1-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="528e1-133">Return value</span></span>

<span data-ttu-id="528e1-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="528e1-134">S_OK</span></span> 
  
> <span data-ttu-id="528e1-135">La notificación el registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="528e1-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="528e1-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="528e1-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="528e1-137">El identificador de entrada que se pasa en el parámetro _lpEntryID_ no está en el formato adecuado.</span><span class="sxs-lookup"><span data-stu-id="528e1-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="528e1-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="528e1-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="528e1-139">El proveedor de la libreta de direcciones no admite la notificación, posiblemente porque no permite que se realicen cambios en sus objetos.</span><span class="sxs-lookup"><span data-stu-id="528e1-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="528e1-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="528e1-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="528e1-141">El proveedor de la libreta de direcciones no puede controlar el identificador de entrada que se pasó _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="528e1-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="528e1-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="528e1-142">Remarks</span></span>

<span data-ttu-id="528e1-143">Los proveedores de la libreta de direcciones implementan el método **IABLogon::Advise** para registrar el autor de la llamada para recibir una notificación cuando se produce un cambio a un objeto en uno de sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="528e1-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="528e1-144">Los autores de llamadas pueden registrarse para notificaciones en relación con los usuarios de mensajería, las listas de distribución o contenedores todo.</span><span class="sxs-lookup"><span data-stu-id="528e1-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="528e1-145">Los clientes normalmente llaman al método de [IAddrBook::Advise](iaddrbook-advise.md) para registrar para las notificaciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="528e1-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="528e1-146">MAPI, a continuación, llama el método **Advise** del proveedor de libreta de direcciones que se encarga del objeto representado por el identificador de entrada en _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="528e1-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="528e1-147">Cuando se produce un cambio en el objeto del tipo representado en _ulEventMask_indicado, se realiza una llamada al método **OnNotify** del receptor de notificaciones que señala _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="528e1-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="528e1-148">Datos que se pasan en la estructura de **notificación** a la rutina de **OnNotify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="528e1-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="528e1-149">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="528e1-149">Notes to implementers</span></span>

<span data-ttu-id="528e1-150">Puede admitir notificación con o sin ayuda de MAPI.</span><span class="sxs-lookup"><span data-stu-id="528e1-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="528e1-151">MAPI tiene tres métodos del objeto de soporte técnico para ayudar a los proveedores de servicios de implementar la notificación de:</span><span class="sxs-lookup"><span data-stu-id="528e1-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="528e1-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="528e1-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="528e1-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="528e1-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="528e1-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="528e1-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="528e1-155">Si decide utilizar los métodos de soporte técnico MAPI, llamar a **Subscribe** cuando se llame al método **Advise** y liberar el puntero _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="528e1-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="528e1-156">Si decide admitir la notificación usted mismo, llame al método **AddRef** del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para mantener una copia de este puntero.</span><span class="sxs-lookup"><span data-stu-id="528e1-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="528e1-157">Mantener esta copia hasta que se llama al método [IABLogon::Unadvise](iablogon-unadvise.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="528e1-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="528e1-158">Independientemente de cómo se admite la notificación, asigne a un número distinto de cero de conexión para el registro de la notificación y devolver en el parámetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="528e1-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="528e1-159">No número de versión de esta conexión hasta que se ha llamado al método **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="528e1-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="528e1-160">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="528e1-160">Notes to callers</span></span>

<span data-ttu-id="528e1-161">El puntero de receptor advise que se pasa en el parámetro _lpAdviseSink_ a **Advise** puede apuntar a un objeto que haya creado o que ha creado MAPI a través de la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="528e1-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="528e1-162">Es posible que desee usar **HrThisThreadAdviseSink** si desea admite varios subprocesos de ejecución y asegúrese de que las llamadas posteriores al método **OnNotify** se producen en un momento adecuado en un subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="528e1-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="528e1-163">Esté preparado para que su objeto de receptor advise liberarse en cualquier momento después de la llamada a **Advise** y antes de la llamada a **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="528e1-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="528e1-164">Por lo tanto, debe liberar su objeto de receptor advise después **Advise** devuelve, a menos que tengan un uso específico a largo plazo para él.</span><span class="sxs-lookup"><span data-stu-id="528e1-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="528e1-165">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="528e1-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="528e1-166">Para obtener información acerca de cómo usar los métodos **IMAPISupport** para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="528e1-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="528e1-167">Para obtener más información acerca de subprocesamiento múltiple y MAPI, vea [subprocesamiento en MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="528e1-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="528e1-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="528e1-168">See also</span></span>



[<span data-ttu-id="528e1-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="528e1-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="528e1-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="528e1-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="528e1-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="528e1-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="528e1-172">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="528e1-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="528e1-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="528e1-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

