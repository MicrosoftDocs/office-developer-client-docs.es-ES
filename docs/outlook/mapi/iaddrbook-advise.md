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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334758"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="7481e-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="7481e-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="7481e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7481e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7481e-105">Registra un cliente o un proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7481e-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7481e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7481e-106">Parameters</span></span>

 <span data-ttu-id="7481e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7481e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7481e-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7481e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7481e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7481e-110">a Un puntero al identificador de entrada del contenedor de la libreta de direcciones, el usuario de mensajería o la lista de distribución que generarán una notificación cuando se produzca un cambio del tipo o de los tipos descritos en el parámetro _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="7481e-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7481e-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="7481e-112">a Uno o más eventos de notificación que el autor de la llamada está registrando para recibirlos.</span><span class="sxs-lookup"><span data-stu-id="7481e-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="7481e-113">Cada evento está asociado a una estructura de notificación determinada que contiene información sobre el cambio que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="7481e-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="7481e-114">En la siguiente tabla se enumeran los valores válidos para _ulEventMask_ y sus estructuras correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7481e-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="7481e-115">**Evento de notificación**</span><span class="sxs-lookup"><span data-stu-id="7481e-115">**Notification event**</span></span>|<span data-ttu-id="7481e-116">**Estructura correspondiente**</span><span class="sxs-lookup"><span data-stu-id="7481e-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7481e-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="7481e-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="7481e-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="7481e-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="7481e-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="7481e-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7481e-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="7481e-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="7481e-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7481e-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="7481e-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="7481e-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7481e-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="7481e-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="7481e-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7481e-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="7481e-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="7481e-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7481e-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="7481e-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="7481e-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7481e-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="7481e-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7481e-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7481e-132">a Un puntero al objeto del receptor de notificaciones al que se llamará cuando se produzca el evento para el que se ha solicitado notificación.</span><span class="sxs-lookup"><span data-stu-id="7481e-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="7481e-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7481e-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="7481e-134">contempla Un puntero a un número de conexión distinto de cero que representa el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="7481e-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7481e-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7481e-135">Return value</span></span>

<span data-ttu-id="7481e-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="7481e-136">S_OK</span></span> 
  
> <span data-ttu-id="7481e-137">El registro de notificaciones se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7481e-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="7481e-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7481e-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7481e-139">El proveedor de la libreta de direcciones responsable del identificador de entrada pasado en _lpEntryID_ no pudo registrar una notificación para la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7481e-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="7481e-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7481e-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7481e-141">La notificación no es compatible con el proveedor de la libreta de direcciones responsable del objeto identificado por el identificador de entrada pasado en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7481e-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7481e-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7481e-143">No se puede controlar el identificador de entrada que se ha pasado en _lpEntryID_ por ninguno de los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="7481e-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7481e-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7481e-144">Remarks</span></span>

<span data-ttu-id="7481e-145">Los clientes y los proveedores de \*\*\*\* servicios llaman al método Advise para registrar un tipo determinado o tipos de notificación en una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7481e-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="7481e-146">Los tipos de notificación se indican mediante la máscara de eventos que se pasa con el parámetro _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="7481e-147">MAPI reenvía \*\*\*\* esta llamada a Adviser al proveedor de la libreta de direcciones que es responsable de la entrada indicada por el identificador de entrada en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="7481e-148">El proveedor de la libreta de direcciones administra el registro en sí o llama al método support, [IMAPISupport:: subscribe](imapisupport-subscribe.md), para pedir a MAPI que registre al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7481e-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="7481e-149">Se devuelve un número de conexión distinto de cero para representar el registro correcto.</span><span class="sxs-lookup"><span data-stu-id="7481e-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="7481e-150">Siempre que se produce un cambio en la entrada del tipo indicado por el registro de la notificación, el proveedor de la libreta de direcciones llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto del receptor de notificaciones especificado en el parámetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="7481e-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="7481e-151">El método **NotifyTo** incluye una estructura de [notificación](notification.md) como un parámetro de entrada que contiene datos para describir el evento.</span><span class="sxs-lookup"><span data-stu-id="7481e-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="7481e-152">Según el proveedor de la libreta de direcciones, la llamada a la **Notify** puede producirse inmediatamente después del cambio en el objeto registrado o en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="7481e-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="7481e-153">En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** puede producirse en cualquier subproceso.</span><span class="sxs-lookup"><span data-stu-id="7481e-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="7481e-154">Los clientes pueden solicitar que estas notificaciones se produzcan en un subproceso determinado llamando a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto de notificación de notificaciones que se pasa a Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7481e-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="7481e-155">Debido a que un proveedor de libretas de direcciones puede liberar el objeto de notificación de notificaciones que pasan los clientes en \*\*\*\* cualquier momento después de la finalización correcta de la llamada a Advise y antes de una llamada a [IAddrBook:: Unadvise](iaddrbook-unadvise.md) para cancelar la notificación, los clientes deben liberar sus objetos de notificación de \*\*\*\* notificaciones cuando se devuelve Advise.</span><span class="sxs-lookup"><span data-stu-id="7481e-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="7481e-156">Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7481e-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7481e-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="7481e-157">See also</span></span>



[<span data-ttu-id="7481e-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7481e-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7481e-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7481e-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="7481e-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7481e-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7481e-161">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="7481e-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7481e-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7481e-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

