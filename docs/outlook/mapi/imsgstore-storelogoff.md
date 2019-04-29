---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424339"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="7ae60-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7ae60-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="7ae60-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ae60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ae60-105">Habilita el cierre de sesión ordenado del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7ae60-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ae60-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7ae60-106">Parameters</span></span>

 <span data-ttu-id="7ae60-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ae60-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7ae60-108">[in, out] Máscara de máscara de marcadores que controla el cierre de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7ae60-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="7ae60-109">En la entrada, todos los indicadores establecidos para este parámetro son mutuamente excluyentes; la persona que llama debe especificar sólo una marca por llamada.</span><span class="sxs-lookup"><span data-stu-id="7ae60-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="7ae60-110">Las siguientes marcas son válidas en la entrada:</span><span class="sxs-lookup"><span data-stu-id="7ae60-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="7ae60-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="7ae60-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="7ae60-112">Se debe detener cualquier actividad de proveedor de transporte para este almacén de mensajes antes de cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="7ae60-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="7ae60-113">El control se devuelve al autor de la llamada cuando se detiene la actividad.</span><span class="sxs-lookup"><span data-stu-id="7ae60-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="7ae60-114">Si se está llevando a cabo alguna actividad de proveedor de transporte, el cierre de sesión no se produce y no se produce ningún cambio en el comportamiento de la cola o los proveedores de transporte de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ae60-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="7ae60-115">Si la actividad del proveedor de transporte está inactiva, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="7ae60-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="7ae60-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="7ae60-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="7ae60-117">El almacén de mensajes no debe esperar a los mensajes de los proveedores de transporte antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="7ae60-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="7ae60-118">Se envían los mensajes salientes listos para enviarse.</span><span class="sxs-lookup"><span data-stu-id="7ae60-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="7ae60-119">Si este almacén contiene la bandeja de entrada predeterminada, se reciben todos los mensajes en proceso y, a continuación, se deshabilita la recepción.</span><span class="sxs-lookup"><span data-stu-id="7ae60-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="7ae60-120">Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7ae60-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="7ae60-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="7ae60-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="7ae60-122">El almacén de mensajes no debe esperar información de los proveedores de transporte antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="7ae60-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="7ae60-123">Los mensajes que se están procesando actualmente están completados, pero no se procesan los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="7ae60-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="7ae60-124">Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al proveedor del almacén.</span><span class="sxs-lookup"><span data-stu-id="7ae60-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="7ae60-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="7ae60-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="7ae60-126">El cierre de sesión debe funcionar del mismo modo que si se establece la marca LOGOFF_NO_WAIT, pero se debe llamar al método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) o [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) para los proveedores de transporte adecuados.</span><span class="sxs-lookup"><span data-stu-id="7ae60-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="7ae60-127">La marca LOGOFF_PURGE devuelve el control al autor de la llamada después de completarse.</span><span class="sxs-lookup"><span data-stu-id="7ae60-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="7ae60-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="7ae60-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="7ae60-129">Si se está llevando a cabo alguna actividad de proveedor de transporte, no se producirá el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="7ae60-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="7ae60-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="7ae60-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="7ae60-131">Los mensajes entrantes llegan actualmente.</span><span class="sxs-lookup"><span data-stu-id="7ae60-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="7ae60-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="7ae60-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="7ae60-133">Los mensajes salientes están en proceso de envío.</span><span class="sxs-lookup"><span data-stu-id="7ae60-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="7ae60-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="7ae60-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="7ae60-135">Los mensajes salientes están pendientes (es decir, se encuentran en la bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="7ae60-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ae60-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ae60-136">Return value</span></span>

<span data-ttu-id="7ae60-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ae60-137">S_OK</span></span> 
  
> <span data-ttu-id="7ae60-138">El cierre de sesión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ae60-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ae60-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ae60-139">Remarks</span></span>

<span data-ttu-id="7ae60-140">El método **IMsgStore:: StoreLogoff** ejerce el control sobre la interacción del almacén de mensajes y los proveedores de transporte durante el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="7ae60-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="7ae60-141">Llamar a **StoreLogoff** solo es válido para los almacenes de mensajes que solo usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7ae60-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="7ae60-142">Por ejemplo, cuando dos clientes usan el mismo almacén de mensajes y uno de ellos llama a **StoreLogoff**, el almacén de mensajes se publica inmediatamente y se devuelve el control al cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7ae60-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7ae60-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="7ae60-143">Notes to implementers</span></span>

<span data-ttu-id="7ae60-144">Guarde las marcas que se pasan a **StoreLogoff** y pásela cuando llame al método [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae60-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="7ae60-145">No llame a **StoreLogoffTransports** hasta que el recuento de referencia del almacén de mensajes caiga en cero.</span><span class="sxs-lookup"><span data-stu-id="7ae60-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="7ae60-146">Varias llamadas a **StoreLogoffTransports** simplemente sobrescriben los indicadores guardados.</span><span class="sxs-lookup"><span data-stu-id="7ae60-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="7ae60-147">Si no se ha realizado ninguna llamada a **StoreLogoff** antes de que el recuento de referencia del almacén de mensajes llegue a cero, establezca la marca LOGOFF_ABORT en el parámetro _ulFlags_ que pasa a **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="7ae60-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ae60-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="7ae60-148">See also</span></span>



[<span data-ttu-id="7ae60-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ae60-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="7ae60-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="7ae60-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="7ae60-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ae60-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="7ae60-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ae60-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

