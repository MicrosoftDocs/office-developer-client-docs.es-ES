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
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419929"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="d8c1a-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="d8c1a-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="d8c1a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8c1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8c1a-105">Registra un receptor de avisos para recibir notificaciones a través de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d8c1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8c1a-106">Parameters</span></span>

 <span data-ttu-id="d8c1a-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-107">_lpKey_</span></span>
  
> <span data-ttu-id="d8c1a-108">[entrada] Puntero a una clave de notificación que representa el objeto de origen de aviso.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="d8c1a-109">El  _parámetro lpKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d8c1a-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="d8c1a-111">[entrada] Máscara de valores que indica los tipos de eventos de notificación que el autor de la llamada está interesado y debe incluirse en el registro.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="d8c1a-112">Los siguientes valores son válidos:</span><span class="sxs-lookup"><span data-stu-id="d8c1a-112">The following values are valid:</span></span>
    
 <span data-ttu-id="d8c1a-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="d8c1a-114">Registra las notificaciones sobre errores graves, como la memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="d8c1a-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="d8c1a-116">Se registra para notificaciones sobre eventos específicos del proveedor de libreta de direcciones o almacén de mensajes en particular.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="d8c1a-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="d8c1a-118">Se registra para recibir notificaciones sobre la llegada de nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="d8c1a-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="d8c1a-120">Registra las notificaciones sobre la creación de un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="d8c1a-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="d8c1a-122">Registra las notificaciones sobre un objeto que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="d8c1a-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="d8c1a-124">Registra las notificaciones sobre un objeto que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="d8c1a-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="d8c1a-126">Registra notificaciones sobre un objeto que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="d8c1a-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="d8c1a-128">Registra las notificaciones sobre un objeto que se está trasladando.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="d8c1a-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="d8c1a-130">Se registra para recibir notificaciones sobre la finalización de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="d8c1a-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-131">_ulFlags_</span></span>
  
> <span data-ttu-id="d8c1a-132">[entrada] Máscara de bits de marcas que controla cómo se produce la notificación.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="d8c1a-133">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="d8c1a-133">The following flag can be set:</span></span>
    
<span data-ttu-id="d8c1a-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="d8c1a-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="d8c1a-135">Cuando el autor de la llamada llama al método [IMAPISupport::Notify](imapisupport-notify.md) para generar notificaciones para este receptor de aviso, **notify** debe realizar todas las llamadas necesarias para avisar a los receptores antes de volver.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="d8c1a-136">Si no se establece esta marca, la notificación es asincrónica y las devoluciones de llamada se ponen en cola en los procesos que se han suscrito e iniciado cuando esos procesos obtienen el control de la CPU.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="d8c1a-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="d8c1a-138">[entrada] Puntero a un objeto receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="d8c1a-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="d8c1a-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="d8c1a-140">[salida] Puntero a un número de conexión distinto de cero que representa el registro.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8c1a-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8c1a-141">Return value</span></span>

<span data-ttu-id="d8c1a-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8c1a-142">S_OK</span></span> 
  
> <span data-ttu-id="d8c1a-143">El registro de notificaciones se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8c1a-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8c1a-144">Remarks</span></span>

<span data-ttu-id="d8c1a-145">El **método IMAPISupport::Subscribe** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d8c1a-146">Los proveedores de servicios **llaman a Subscribe** desde uno de sus **métodos Advise** para permitir que MAPI administre las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d8c1a-147">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d8c1a-147">Notes to callers</span></span>

<span data-ttu-id="d8c1a-148">Para usar los métodos de soporte de MAPI para la notificación, cree una clave para el origen del aviso el objeto sobre qué notificaciones se deben generar.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="d8c1a-149">El valor de la clave debe ser único y debe regenerarse fácilmente cada vez que cambie el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="d8c1a-150">MAPI usa la clave de notificación para buscar cualquier función de devolución de llamada registrada a través de la función [HrAllocAdviseSink](hrallocadvisesink.md) para el origen de aviso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="d8c1a-151">Pase esta clave a **IMAPISupport::Notify** siempre que necesite generar una notificación para el origen de aviso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="d8c1a-152">El NOTIFY_SYNC marca afecta al funcionamiento de las llamadas subsiguientes a **Notify**.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="d8c1a-153">Cuando estableces NOTIFY_SYNC, **Notify** no vuelve hasta que termina de enviar todas las notificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="d8c1a-154">Cuando no estableces la NOTIFY_SYNC, **notify** funciona de forma asincrónica, posiblemente devolviendo antes de que se hayan enviado todas las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8c1a-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8c1a-155">See also</span></span>



[<span data-ttu-id="d8c1a-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d8c1a-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="d8c1a-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d8c1a-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d8c1a-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="d8c1a-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="d8c1a-159">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="d8c1a-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d8c1a-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="d8c1a-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="d8c1a-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8c1a-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

