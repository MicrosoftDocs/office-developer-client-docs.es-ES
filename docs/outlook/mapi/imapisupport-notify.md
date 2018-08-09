---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: db23d1801bf32fd947a77dfd887c56f75ded5681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817519"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="82260-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="82260-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="82260-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82260-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82260-105">Envía una notificación de un evento especificado a un origen de advise que registró originalmente para la notificación a través del método [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="82260-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="82260-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82260-106">Parameters</span></span>

<span data-ttu-id="82260-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="82260-107">_lpKey_</span></span>
  
> <span data-ttu-id="82260-108">[entrada] Un puntero a la clave de notificación para el objeto de origen advise.</span><span class="sxs-lookup"><span data-stu-id="82260-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="82260-109">El parámetro _lpKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="82260-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="82260-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="82260-110">_cNotification_</span></span>
  
> <span data-ttu-id="82260-111">[entrada] El recuento de las estructuras de notificación que señala el parámetro _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="82260-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="82260-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="82260-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="82260-113">[entrada] Un puntero a una matriz de estructuras de [notificación](notification.md) que se describen las notificaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="82260-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="82260-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="82260-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="82260-115">[entrada, salida] Una máscara de bits de indicadores que controla el proceso de notificación.</span><span class="sxs-lookup"><span data-stu-id="82260-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="82260-116">En la entrada, se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="82260-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="82260-117">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="82260-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="82260-118">Las cadenas en las estructuras de notificación que señala _lpNotifications_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="82260-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="82260-119">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="82260-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="82260-120">En la salida, MAPI puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="82260-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="82260-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="82260-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="82260-122">Una función de devolución de llamada cancela una notificación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="82260-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82260-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82260-123">Return value</span></span>

<span data-ttu-id="82260-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="82260-124">S_OK</span></span> 
  
> <span data-ttu-id="82260-125">Las notificaciones se han generado correctamente.</span><span class="sxs-lookup"><span data-stu-id="82260-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82260-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82260-126">Remarks</span></span>

<span data-ttu-id="82260-127">El método **IMAPISupport::Notify** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="82260-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="82260-128">Proveedores de servicios de llamada **Notify** para solicitar que MAPI generar una notificación para un receptor de notificaciones que se ha registrado previamente para la notificación a través del método **IMAPISupport::Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="82260-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="82260-129">**Notify** copias las estructuras indicada por el parámetro _lpNotifications_ en la memoria y llama a método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor advise adecuado.</span><span class="sxs-lookup"><span data-stu-id="82260-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="82260-130">Cuando finalice **OnNotify** con la notificación, libera la memoria implicados.</span><span class="sxs-lookup"><span data-stu-id="82260-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="82260-131">El autor de la llamada no es necesario asignar memoria; MAPI realiza toda la asignación de memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="82260-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82260-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="82260-132">Notes to callers</span></span>

<span data-ttu-id="82260-133">La clave de notificación que se pasa en el parámetro _lpKey_ debe ser idéntica a la clave pasada en _lpKey_ al método **IMAPISupport::Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="82260-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="82260-134">Muchos proveedores de utilizan el identificador de entrada del origen de advise como la clave, pero otros datos, como una ruta de acceso de archivo, se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="82260-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="82260-135">MAPI utiliza esta clave para buscar todos los registros para las notificaciones en el origen de advise identificados.</span><span class="sxs-lookup"><span data-stu-id="82260-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="82260-136">Asegúrese de que establece al miembro **lpEntryID** de la estructura de notificación en un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="82260-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="82260-137">Si se establece el indicador NOTIFY_SYNC en la **suscripción** de llamadas para cualquiera de las notificaciones pendientes, **Notificar** llamadas las funciones de devolución de llamada de método **IMAPIAdviseSink::OnNotify** antes de devolver.</span><span class="sxs-lookup"><span data-stu-id="82260-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="82260-138">Un receptor de notificaciones puede crearse manualmente o mediante una llamada a [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="82260-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="82260-139">La función **HrAllocAdviseSink** permite su autor de la llamada especificar una función de devolución de llamada que llama **Notify** como parte de la notificación.</span><span class="sxs-lookup"><span data-stu-id="82260-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="82260-140">La función de devolución de llamada se ajusta al prototipo [NOTIFCALLBACK](notifcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="82260-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="82260-141">Funciones de devolución de llamada implementadas por los clientes siempre devuelven S_OK; funciones de devolución de llamada que se implementan los proveedores de servicio pueden devolver CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="82260-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="82260-142">Si una función de devolución de llamada devuelve CALLBACK_DISCONTINUE, MAPI deja de enviar notificaciones y devuelve NOTIFY_CANCELED en el **Notify** parámetro del método _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="82260-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="82260-143">Puede asumir que el proceso está inactivo y detención de generación de notificaciones para ese proceso.</span><span class="sxs-lookup"><span data-stu-id="82260-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="82260-144">Si **Notify** devuelve 0 en _lpulFlags_, el proceso todavía está activo y se debe seguir enviar notificaciones, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="82260-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="82260-145">Al usar notificaciones sincrónicas, tenga cuidado para evitar situaciones de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="82260-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="82260-146">Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="82260-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82260-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="82260-147">See also</span></span>

- [<span data-ttu-id="82260-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="82260-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="82260-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="82260-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="82260-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="82260-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="82260-151">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="82260-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="82260-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="82260-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="82260-153">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="82260-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="82260-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82260-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

