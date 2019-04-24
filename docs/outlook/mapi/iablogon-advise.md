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
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338580"
---
# <a name="iablogonadvise"></a><span data-ttu-id="47cca-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="47cca-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="47cca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47cca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47cca-105">Registra el autor de la llamada para recibir una notificación de los eventos especificados que afectan a un contenedor, un usuario de mensajería o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="47cca-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="47cca-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="47cca-106">Parameters</span></span>

 <span data-ttu-id="47cca-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="47cca-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="47cca-108">a Número de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="47cca-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="47cca-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="47cca-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="47cca-110">a Un puntero al identificador de entrada del objeto sobre el que se deben generar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="47cca-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="47cca-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="47cca-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="47cca-112">a Máscara de tipo de valores que indican los tipos de eventos de notificación en los que está interesado el autor de la llamada y deben incluirse en el registro.</span><span class="sxs-lookup"><span data-stu-id="47cca-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="47cca-113">Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="47cca-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="47cca-114">En la siguiente tabla se enumeran los valores válidos para el parámetro _ulEventMask_ y las estructuras asociadas con cada valor.</span><span class="sxs-lookup"><span data-stu-id="47cca-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="47cca-115">**Tipo de evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="47cca-115">**Notification event type**</span></span>|<span data-ttu-id="47cca-116">**Estructura de **notificación** correspondiente**</span><span class="sxs-lookup"><span data-stu-id="47cca-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47cca-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="47cca-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="47cca-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="47cca-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="47cca-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="47cca-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="47cca-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="47cca-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="47cca-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="47cca-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="47cca-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="47cca-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="47cca-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="47cca-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="47cca-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="47cca-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="47cca-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="47cca-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="47cca-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="47cca-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="47cca-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="47cca-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="47cca-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="47cca-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="47cca-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="47cca-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="47cca-130">a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="47cca-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="47cca-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="47cca-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="47cca-132">contempla Un puntero a un valor distinto de cero que representa el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="47cca-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47cca-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47cca-133">Return value</span></span>

<span data-ttu-id="47cca-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="47cca-134">S_OK</span></span> 
  
> <span data-ttu-id="47cca-135">El registro de notificaciones se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="47cca-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="47cca-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47cca-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="47cca-137">El identificador de entrada pasado en el parámetro _lpEntryID_ no tiene el formato adecuado.</span><span class="sxs-lookup"><span data-stu-id="47cca-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="47cca-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="47cca-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="47cca-139">El proveedor de la libreta de direcciones no admite la notificación, posiblemente porque no permite que se realicen cambios en sus objetos.</span><span class="sxs-lookup"><span data-stu-id="47cca-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="47cca-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47cca-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="47cca-141">El proveedor de la libreta de direcciones no puede controlar el identificador de entrada pasado en _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="47cca-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47cca-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47cca-142">Remarks</span></span>

<span data-ttu-id="47cca-143">Los proveedores de la libreta de direcciones implementan el método **IABLogon:: Advise** para registrar que el autor de la llamada recibirá una notificación cuando se produzca un cambio en un objeto de uno de sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="47cca-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="47cca-144">Los autores de llamadas pueden registrarse en las notificaciones sobre los usuarios de mensajería, las listas de distribución o los contenedores completos.</span><span class="sxs-lookup"><span data-stu-id="47cca-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="47cca-145">Los clientes suelen llamar al método [IAddrBook:: Advise](iaddrbook-advise.md) para registrarse en las notificaciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="47cca-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="47cca-146">MAPI, a continuación \*\*\*\* , llama al método Advise del proveedor de la libreta de direcciones que es responsable del objeto representado por el identificador de entrada en _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="47cca-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="47cca-147">Cuando se produce un cambio en el objeto indicado del tipo representado en _ulEventMask_, se realiza una llamada al método **BENOTIFY** del receptor de notificaciones apuntado por _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="47cca-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="47cca-148">Los datos que se pasan en la estructura de **notificación** a la rutina de **Notify** describen el evento.</span><span class="sxs-lookup"><span data-stu-id="47cca-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47cca-149">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="47cca-149">Notes to implementers</span></span>

<span data-ttu-id="47cca-150">Puede admitir la notificación con o sin ayuda de MAPI.</span><span class="sxs-lookup"><span data-stu-id="47cca-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="47cca-151">MAPI tiene tres métodos de objeto de soporte para ayudar a los proveedores de servicios a implementar la notificación:</span><span class="sxs-lookup"><span data-stu-id="47cca-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="47cca-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="47cca-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="47cca-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="47cca-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="47cca-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="47cca-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="47cca-155">Si decide usar los métodos de compatibilidad con MAPI, llame a **subscribe** cuando se llame al método Advise y suelte el puntero _lpAdviseSink_ . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="47cca-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="47cca-156">Si opta por admitir la notificación usted mismo, llame al método **AddRef** del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para conservar una copia de este puntero.</span><span class="sxs-lookup"><span data-stu-id="47cca-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="47cca-157">Mantenga esta copia hasta que se llame al método [IABLogon:: Unadvise](iablogon-unadvise.md) para cancelar el registro.</span><span class="sxs-lookup"><span data-stu-id="47cca-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="47cca-158">Independientemente de cómo se admita la notificación, asigne un número de conexión distinto de cero al registro de notificaciones y devuelva el parámetro _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="47cca-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="47cca-159">No libere este número de conexión hasta que se haya llamado al método **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="47cca-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47cca-160">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="47cca-160">Notes to callers</span></span>

<span data-ttu-id="47cca-161">El puntero para avisar al receptor que se pasa en el parámetro _lpAdviseSink_ a Advise puede apuntar a un objeto que haya creado o que haya creado MAPI mediante la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="47cca-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="47cca-162">Es posible que desee usar **HrThisThreadAdviseSink** si admite varios subprocesos de ejecución y desea asegurarse de que las llamadas posteriores al método de **Notify** se produzcan en el momento adecuado en un subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="47cca-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="47cca-163">Esté preparado para que el objeto receptor de notificaciones se publique en cualquier momento después de su llamada a adVise y antes de la llamada a Unadvise. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="47cca-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="47cca-164">Por lo tanto, debe liberar su objeto de notificación \*\*\*\* de notificaciones después de que se deVuelva Advise, a menos que tenga un uso específico a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="47cca-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="47cca-165">Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="47cca-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="47cca-166">Para obtener información sobre cómo usar los métodos de **IMAPISupport** para admitir la notificación, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="47cca-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="47cca-167">Para obtener más información acerca del multiproceso y MAPI, vea el tema sobre el [procesamiento en MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="47cca-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47cca-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="47cca-168">See also</span></span>



[<span data-ttu-id="47cca-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="47cca-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="47cca-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="47cca-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="47cca-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="47cca-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="47cca-172">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="47cca-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="47cca-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47cca-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

