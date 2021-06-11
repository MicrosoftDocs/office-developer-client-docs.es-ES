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
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435939"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="0f7b0-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="0f7b0-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="0f7b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f7b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f7b0-105">Envía una notificación de un evento especificado a un origen de aviso que se registró originalmente para la notificación a través del [método IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="0f7b0-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0f7b0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0f7b0-106">Parameters</span></span>

<span data-ttu-id="0f7b0-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="0f7b0-107">_lpKey_</span></span>
  
> <span data-ttu-id="0f7b0-108">[in] Puntero a la clave de notificación del objeto de origen advise.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="0f7b0-109">El  _parámetro lpKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="0f7b0-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="0f7b0-110">_cNotification_</span></span>
  
> <span data-ttu-id="0f7b0-111">[in] Recuento de estructuras de notificación a las que apunta el _parámetro lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="0f7b0-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="0f7b0-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="0f7b0-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="0f7b0-113">[in] Puntero a una matriz de estructuras [NOTIFICATION](notification.md) que describen notificaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="0f7b0-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f7b0-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="0f7b0-115">[in, out] Máscara de bits de marcas que controla el proceso de notificación.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="0f7b0-116">En la entrada, se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="0f7b0-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="0f7b0-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f7b0-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="0f7b0-118">Las cadenas de las estructuras de notificación a las que  _apunta lpNotifications_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="0f7b0-119">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="0f7b0-120">En el resultado, MAPI puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="0f7b0-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="0f7b0-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="0f7b0-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="0f7b0-122">Una función de devolución de llamada canceló una notificación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f7b0-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f7b0-123">Return value</span></span>

<span data-ttu-id="0f7b0-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f7b0-124">S_OK</span></span> 
  
> <span data-ttu-id="0f7b0-125">Las notificaciones se generaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f7b0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f7b0-126">Remarks</span></span>

<span data-ttu-id="0f7b0-127">El **método IMAPISupport::Notify** se implementa para todos los objetos de soporte técnico del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="0f7b0-128">Los proveedores de servicios llaman a **Notify** para solicitar que MAPI genere una notificación para un receptor de notificaciones que se haya registrado previamente para la notificación a través del **método IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="0f7b0-129">**Notify** copia las estructuras a las que apunta el parámetro  _lpNotifications_ en la memoria y llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones adecuado.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="0f7b0-130">Cuando **OnNotify** finaliza con la notificación, libera la memoria implicada.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="0f7b0-131">El autor de la llamada no necesita asignar memoria; MAPI realiza toda la asignación de memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f7b0-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0f7b0-132">Notes to callers</span></span>

<span data-ttu-id="0f7b0-133">La clave de notificación pasada en el _parámetro lpKey_ debe ser idéntica a la clave pasada en _lpKey_ al **método IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="0f7b0-134">Muchos proveedores usan el identificador de entrada del origen de aviso como clave, pero se pueden usar otros datos, como una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="0f7b0-135">MAPI usa esta clave para buscar todos los registros de notificaciones en el origen de aviso identificado.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="0f7b0-136">Asegúrese de establecer el miembro **lpEntryID** de la estructura de notificaciones en un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="0f7b0-137">Si establece la marca NOTIFY_SYNC en la llamada **Subscribe** para cualquiera de las notificaciones pendientes, **Notify** llama a las funciones de devolución de llamada del método **IMAPIAdviseSink::OnNotify** antes de devolver.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="0f7b0-138">Un receptor de avisos se puede crear manualmente o llamando a [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="0f7b0-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="0f7b0-139">La **función HrAllocAdviseSink** permite a su autor de la llamada especificar una función de devolución de llamada que **Notify** llama como parte de la notificación.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="0f7b0-140">La función de devolución de llamada se ajusta al prototipo [NOTIFCALLBACK.](notifcallback.md)</span><span class="sxs-lookup"><span data-stu-id="0f7b0-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="0f7b0-141">Las funciones de devolución de llamada implementadas por los clientes siempre devuelven S_OK; Las funciones de devolución de llamada implementadas por los proveedores de servicios pueden devolver CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="0f7b0-142">Si una función de devolución de llamada devuelve CALLBACK_DISCONTINUE, MAPI deja de enviar notificaciones y devuelve NOTIFY_CANCELED en el parámetro _lpulFlags_ del método **Notify.**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="0f7b0-143">Puede asumir que el proceso está inactivo y dejar de generar notificaciones para ese proceso.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="0f7b0-144">Si **Notify** devuelve 0 en  _lpulFlags,_ el proceso sigue activo y debe continuar con el envío de notificaciones, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="0f7b0-145">Cuando use notificaciones sincrónicas, tenga cuidado de evitar situaciones de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="0f7b0-146">Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0f7b0-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f7b0-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f7b0-147">See also</span></span>

- [<span data-ttu-id="0f7b0-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="0f7b0-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="0f7b0-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="0f7b0-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="0f7b0-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0f7b0-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="0f7b0-151">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="0f7b0-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="0f7b0-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="0f7b0-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="0f7b0-153">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="0f7b0-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="0f7b0-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f7b0-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

