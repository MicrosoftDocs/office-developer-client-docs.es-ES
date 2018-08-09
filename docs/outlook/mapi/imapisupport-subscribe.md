---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817579"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="d5abd-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="d5abd-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="d5abd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5abd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5abd-105">Registra un receptor de notificaciones para recibir notificaciones a través de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5abd-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d5abd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5abd-106">Parameters</span></span>

 <span data-ttu-id="d5abd-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="d5abd-107">_lpKey_</span></span>
  
> <span data-ttu-id="d5abd-108">[entrada] Un puntero a una clave de notificación que representa el objeto de origen advise.</span><span class="sxs-lookup"><span data-stu-id="d5abd-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="d5abd-109">El parámetro _lpKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d5abd-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d5abd-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="d5abd-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="d5abd-111">[entrada] Una máscara de valores que se indican los tipos de eventos de notificación que el autor de la llamada está interesado en y se debe incluir en el registro.</span><span class="sxs-lookup"><span data-stu-id="d5abd-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="d5abd-112">Los valores siguientes son válidos:</span><span class="sxs-lookup"><span data-stu-id="d5abd-112">The following values are valid:</span></span>
    
 <span data-ttu-id="d5abd-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="d5abd-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="d5abd-114">Registra las notificaciones acerca de los errores graves, como memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="d5abd-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="d5abd-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="d5abd-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="d5abd-116">Proveedor de almacén de registros para las notificaciones sobre los eventos específicos de la libreta de direcciones determinada o mensaje.</span><span class="sxs-lookup"><span data-stu-id="d5abd-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="d5abd-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="d5abd-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="d5abd-118">Registra las notificaciones sobre la llegada de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="d5abd-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="d5abd-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="d5abd-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="d5abd-120">Registra las notificaciones sobre la creación de un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="d5abd-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="d5abd-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="d5abd-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="d5abd-122">Registra las notificaciones sobre un objeto que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="d5abd-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="d5abd-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="d5abd-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="d5abd-124">Registra las notificaciones sobre un objeto que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="d5abd-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="d5abd-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="d5abd-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="d5abd-126">Registra las notificaciones sobre un objeto que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d5abd-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="d5abd-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="d5abd-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="d5abd-128">Registra las notificaciones sobre un objeto que se va a mover.</span><span class="sxs-lookup"><span data-stu-id="d5abd-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="d5abd-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="d5abd-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="d5abd-130">Registra las notificaciones sobre la finalización de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5abd-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="d5abd-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5abd-131">_ulFlags_</span></span>
  
> <span data-ttu-id="d5abd-132">[entrada] Una máscara de bits de indicadores que controla cómo se produce la notificación.</span><span class="sxs-lookup"><span data-stu-id="d5abd-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="d5abd-133">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5abd-133">The following flag can be set:</span></span>
    
<span data-ttu-id="d5abd-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="d5abd-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="d5abd-135">Cuando el autor de la llamada, llama al método de [IMAPISupport::Notify](imapisupport-notify.md) para generar las notificaciones para este receptor de notificaciones, **Notify** debe realizar todas las llamadas necesarias para avisar a los receptores antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="d5abd-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="d5abd-136">Si no se establece este marcador, notificación es asincrónica y se ponen en cola devoluciones de llamada a los procesos que se han suscrito y se inicia cuando estos procesos obtienen el control de la CPU.</span><span class="sxs-lookup"><span data-stu-id="d5abd-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="d5abd-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d5abd-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="d5abd-138">[entrada] Un puntero a un objeto de receptor advise.</span><span class="sxs-lookup"><span data-stu-id="d5abd-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="d5abd-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="d5abd-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="d5abd-140">[out] Un puntero a un número distinto de cero de conexión que representa el registro.</span><span class="sxs-lookup"><span data-stu-id="d5abd-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5abd-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5abd-141">Return value</span></span>

<span data-ttu-id="d5abd-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5abd-142">S_OK</span></span> 
  
> <span data-ttu-id="d5abd-143">La notificación el registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5abd-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5abd-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5abd-144">Remarks</span></span>

<span data-ttu-id="d5abd-145">El método **IMAPISupport::Subscribe** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="d5abd-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d5abd-146">Proveedores de servicios de llamar a **Subscribe** desde uno de sus métodos **Advise** para permitir MAPI administrar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d5abd-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5abd-147">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d5abd-147">Notes to callers</span></span>

<span data-ttu-id="d5abd-148">Para usar los métodos de soporte técnico MAPI para la notificación, cree una clave para el origen de advise se debería generar el objeto acerca de las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d5abd-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="d5abd-149">El valor de la clave debe ser único y debe ser fácilmente vuelve a generar cada vez que cambia el objeto.</span><span class="sxs-lookup"><span data-stu-id="d5abd-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="d5abd-150">MAPI utiliza la clave de notificación para buscar todas las funciones de devolución de llamada registradas a través de la función [HrAllocAdviseSink](hrallocadvisesink.md) para el origen de advise correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d5abd-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="d5abd-151">Pase esta clave a **IMAPISupport::Notify** cada vez que se necesita generar una notificación para el origen de advise correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d5abd-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="d5abd-152">El indicador NOTIFY_SYNC afecta a la operación de las llamadas subsiguientes a **Notify**.</span><span class="sxs-lookup"><span data-stu-id="d5abd-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="d5abd-153">Cuando se establece NOTIFY_SYNC, **Notificar** no devuelve hasta que ha terminado de enviar todas las notificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="d5abd-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="d5abd-154">Cuando no se establece NOTIFY_SYNC, **Notify** funciona de forma asincrónica, devolución, posiblemente, antes de que todas las notificaciones se han enviado.</span><span class="sxs-lookup"><span data-stu-id="d5abd-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5abd-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5abd-155">See also</span></span>



[<span data-ttu-id="d5abd-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d5abd-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="d5abd-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d5abd-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d5abd-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="d5abd-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="d5abd-159">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="d5abd-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d5abd-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="d5abd-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="d5abd-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5abd-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

