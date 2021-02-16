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
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406279"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="4bbcb-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="4bbcb-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="4bbcb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bbcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bbcb-105">Registra un cliente o proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4bbcb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bbcb-106">Parameters</span></span>

 <span data-ttu-id="4bbcb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4bbcb-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4bbcb-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4bbcb-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4bbcb-110">[entrada] Puntero al identificador de entrada del contenedor de la libreta de direcciones, el usuario de mensajería o la lista de distribución que generará una notificación cuando se produzca un cambio del tipo o los tipos descritos en el parámetro _ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="4bbcb-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="4bbcb-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="4bbcb-112">[entrada] Uno o más eventos de notificación que el autor de la llamada está registrando para recibir.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="4bbcb-113">Cada evento está asociado a una estructura de notificación determinada que contiene información sobre el cambio que se produjo.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="4bbcb-114">En la tabla siguiente se enumeran los valores válidos  _para ulEventMask_ y sus estructuras correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="4bbcb-115">**Evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-115">**Notification event**</span></span>|<span data-ttu-id="4bbcb-116">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bbcb-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="4bbcb-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4bbcb-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="4bbcb-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4bbcb-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="4bbcb-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4bbcb-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="4bbcb-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4bbcb-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="4bbcb-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4bbcb-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="4bbcb-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4bbcb-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="4bbcb-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="4bbcb-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4bbcb-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="4bbcb-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4bbcb-132">[entrada] Un puntero al objeto receptor de aviso al que se llamará cuando se produzca el evento para el que se ha solicitado la notificación.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="4bbcb-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="4bbcb-134">[salida] Puntero a un número de conexión distinto de cero que representa el registro de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4bbcb-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bbcb-135">Return value</span></span>

<span data-ttu-id="4bbcb-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bbcb-136">S_OK</span></span> 
  
> <span data-ttu-id="4bbcb-137">El registro de notificaciones se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="4bbcb-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4bbcb-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="4bbcb-139">El proveedor de libreta de direcciones responsable del identificador de entrada pasado  _en lpEntryID_ no pudo registrar una notificación para la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="4bbcb-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4bbcb-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4bbcb-141">El proveedor de libreta de direcciones responsable del objeto identificado por el identificador de entrada pasado en el  _parámetro lpEntryID_ no admite la notificación.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="4bbcb-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4bbcb-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4bbcb-143">El identificador de entrada pasado  _en lpEntryID_ no puede ser manipulado por ninguno de los proveedores de libretas de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4bbcb-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4bbcb-144">Remarks</span></span>

<span data-ttu-id="4bbcb-145">Los clientes y proveedores de servicios llaman **al método Advise** para registrarse para un tipo determinado o tipos de notificación en una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="4bbcb-146">Los tipos de notificación se indican mediante la máscara de evento que se pasa con el _parámetro ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="4bbcb-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="4bbcb-147">MAPI reenvía esta llamada **advise** al proveedor de libreta de direcciones responsable de la entrada, tal como lo indica el identificador de entrada en el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4bbcb-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="4bbcb-148">El proveedor de libreta de direcciones controla el propio registro o llama al método de soporte técnico [IMAPISupport::Subscribe](imapisupport-subscribe.md)para solicitar a MAPI que registre al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="4bbcb-149">Se devuelve un número de conexión distinto de cero para representar el registro correcto.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="4bbcb-150">Siempre que se produce un cambio en la entrada del tipo indicado por el registro de notificaciones, el proveedor de libreta de direcciones llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor de aviso especificado en el parámetro _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="4bbcb-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="4bbcb-151">El **método OnNotify** incluye una [estructura NOTIFICATION](notification.md) como un parámetro de entrada que contiene datos para describir el evento.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="4bbcb-152">Según el proveedor de libreta de direcciones, la llamada a **OnNotify** puede producirse inmediatamente después del cambio en el objeto registrado o en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="4bbcb-153">En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="4bbcb-154">Los clientes pueden solicitar que estas notificaciones se produzcan en un subproceso determinado llamando a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto receptor de aviso que se pasa a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="4bbcb-155">Dado que un proveedor de libreta de direcciones puede liberar el objeto receptor de avisos pasado por los clientes en cualquier momento después de la finalización correcta de la llamada **advise** y antes de una llamada [IAddrBook::Unadvise](iaddrbook-unadvise.md) para cancelar la notificación, los clientes deben liberar sus objetos receptores de aviso cuando **advise** vuelva.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="4bbcb-156">Para obtener más información acerca del proceso de notificación, vea [Notificación de eventos en MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="4bbcb-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4bbcb-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4bbcb-157">See also</span></span>



[<span data-ttu-id="4bbcb-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4bbcb-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4bbcb-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4bbcb-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="4bbcb-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4bbcb-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4bbcb-161">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="4bbcb-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4bbcb-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4bbcb-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

