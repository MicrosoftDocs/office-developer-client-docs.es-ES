---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 43569b22cace7b2700d37ace49fd734b45fec73c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580883"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="9ece0-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="9ece0-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="9ece0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ece0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ece0-105">Registra un proveedor de servicio o cliente para recibir notificaciones sobre los cambios realizados en una o más entradas en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9ece0-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="9ece0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ece0-106">Parameters</span></span>

 <span data-ttu-id="9ece0-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9ece0-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9ece0-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9ece0-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9ece0-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9ece0-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9ece0-110">[entrada] Un puntero al identificador de entrada del contenedor de libreta de direcciones, usuario o lista de distribución que genere una notificación cuando se produce un cambio del tipo o tipos que se describen en el parámetro _ulEventMask_ de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9ece0-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="9ece0-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="9ece0-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="9ece0-112">[entrada] Uno o más eventos de notificación que el autor de la llamada se está registrando para recibir.</span><span class="sxs-lookup"><span data-stu-id="9ece0-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="9ece0-113">Cada evento se asocia con una estructura de notificación en particular que contiene información sobre el cambio que se produjo.</span><span class="sxs-lookup"><span data-stu-id="9ece0-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="9ece0-114">En la siguiente tabla se enumera los valores válidos para _ulEventMask_ y las estructuras de sus correspondientes.</span><span class="sxs-lookup"><span data-stu-id="9ece0-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="9ece0-115">**Evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="9ece0-115">**Notification event**</span></span>|<span data-ttu-id="9ece0-116">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="9ece0-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ece0-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="9ece0-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="9ece0-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="9ece0-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="9ece0-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="9ece0-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9ece0-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="9ece0-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="9ece0-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9ece0-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="9ece0-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="9ece0-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9ece0-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="9ece0-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="9ece0-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9ece0-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="9ece0-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="9ece0-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9ece0-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="9ece0-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="9ece0-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ece0-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="9ece0-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="9ece0-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="9ece0-132">[entrada] Un puntero al objeto receptor advise que se llama cuando se produce el evento para el que se ha solicitado la notificación.</span><span class="sxs-lookup"><span data-stu-id="9ece0-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="9ece0-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="9ece0-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="9ece0-134">[out] Un puntero a un número distinto de cero de conexión que representa el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="9ece0-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ece0-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ece0-135">Return value</span></span>

<span data-ttu-id="9ece0-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ece0-136">S_OK</span></span> 
  
> <span data-ttu-id="9ece0-137">La notificación el registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ece0-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="9ece0-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9ece0-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="9ece0-139">El proveedor de libreta de direcciones responsable para el identificador de entrada que se pasan en _lpEntryID_ no pudo registrar una notificación de la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9ece0-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="9ece0-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9ece0-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9ece0-141">Notificación no es compatible con el proveedor de libreta de direcciones responsable del objeto identificado por el identificador de entrada que se pasa en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9ece0-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="9ece0-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9ece0-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="9ece0-143">El identificador de entrada que se pasan en _lpEntryID_ no se puede controlar mediante cualquiera de los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="9ece0-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9ece0-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ece0-144">Remarks</span></span>

<span data-ttu-id="9ece0-145">Los clientes y proveedores de servicios de llaman al método **Advise** se registre para un determinado tipo o tipos de notificación en una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9ece0-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="9ece0-146">Los tipos de notificación se indican mediante la máscara de eventos pasada con el parámetro _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="9ece0-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="9ece0-147">MAPI reenvía esta llamada **Advise** para el proveedor de libreta de direcciones que es responsable de la entrada indicada por el identificador de entrada en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9ece0-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="9ece0-148">El proveedor de la libreta de direcciones que administra el registro propio o que llama al método de soporte técnico, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para que solicite MAPI para registrar el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ece0-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="9ece0-149">Se devuelve un número de conexión distinto de cero para representar el registro correcto.</span><span class="sxs-lookup"><span data-stu-id="9ece0-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="9ece0-150">Cada vez que se produce un cambio a la entrada del tipo indicado por el registro de la notificación, en el proveedor de la libreta de direcciones se llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise especificado en el parámetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="9ece0-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="9ece0-151">El método **OnNotify** incluye una estructura de [notificación](notification.md) como un parámetro de entrada que contiene los datos para describir el evento.</span><span class="sxs-lookup"><span data-stu-id="9ece0-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="9ece0-152">Según el proveedor de la libreta de direcciones, la llamada a **OnNotify** puede ocurrir inmediatamente tras el cambio en el objeto registrado o en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="9ece0-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="9ece0-153">En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="9ece0-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="9ece0-154">Los clientes pueden solicitar que estas notificaciones se producen en un subproceso concreto mediante una llamada a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto de receptor advise que se pasa al **Advise**.</span><span class="sxs-lookup"><span data-stu-id="9ece0-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="9ece0-155">Debido a que un proveedor de la libreta de direcciones puede liberar el objeto de receptor advise que se pasan por los clientes en cualquier momento después de la finalización correcta de la **Advise** y antes de una [IAddrBook::Unadvise](iaddrbook-unadvise.md) de llamadas para cancelar la notificación, deben liberar los clientes los objetos del receptor advise cuando **Advise** devuelve.</span><span class="sxs-lookup"><span data-stu-id="9ece0-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="9ece0-156">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="9ece0-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ece0-157">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9ece0-157">See also</span></span>



[<span data-ttu-id="9ece0-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9ece0-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="9ece0-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="9ece0-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="9ece0-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="9ece0-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="9ece0-161">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="9ece0-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9ece0-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9ece0-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

