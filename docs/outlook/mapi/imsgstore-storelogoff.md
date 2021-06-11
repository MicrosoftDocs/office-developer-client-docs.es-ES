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
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="a0bd4-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="a0bd4-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="a0bd4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0bd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0bd4-105">Habilita el cierre de sesión orden del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a0bd4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0bd4-106">Parameters</span></span>

 <span data-ttu-id="a0bd4-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0bd4-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a0bd4-108">[in, out] Máscara de bits de marcas que controla el cierre de sesión desde el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="a0bd4-109">En la entrada, todas las marcas establecidas para este parámetro son mutuamente excluyentes; Un autor de la llamada debe especificar solo una marca por llamada.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="a0bd4-110">Las siguientes marcas son válidas en la entrada:</span><span class="sxs-lookup"><span data-stu-id="a0bd4-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="a0bd4-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="a0bd4-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="a0bd4-112">Cualquier actividad del proveedor de transporte para este almacén de mensajes debe detenerse antes de cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="a0bd4-113">El control se devuelve al autor de la llamada después de detener la actividad.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="a0bd4-114">Si se está llevando a cabo alguna actividad del proveedor de transporte, el cierre de sesión no se produce y no se produce ningún cambio en el comportamiento de la cola MAPI o los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="a0bd4-115">Si la actividad del proveedor de transporte está inactiva, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="a0bd4-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="a0bd4-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="a0bd4-117">El almacén de mensajes no debe esperar los mensajes de los proveedores de transporte antes de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="a0bd4-118">Se envían los mensajes salientes que están listos para enviarse.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="a0bd4-119">Si este almacén contiene la Bandeja de entrada predeterminada, se reciben los mensajes en proceso y, a continuación, se deshabilita la recepción adicional.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="a0bd4-120">Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="a0bd4-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="a0bd4-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="a0bd4-122">El almacén de mensajes no debe esperar la información de los proveedores de transporte antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="a0bd4-123">Los mensajes que se están procesando actualmente se completan, pero no se procesan mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="a0bd4-124">Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al proveedor de la tienda.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="a0bd4-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="a0bd4-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="a0bd4-126">El cierre de sesión debe funcionar igual que si se establece la marca LOGOFF_NO_WAIT, pero se debe llamar al método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) o [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) para los proveedores de transporte adecuados.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="a0bd4-127">La LOGOFF_PURGE devuelve el control al autor de la llamada después de finalizar.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="a0bd4-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="a0bd4-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="a0bd4-129">Si se está llevando a cabo alguna actividad del proveedor de transporte, no debe producirse el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="a0bd4-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="a0bd4-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="a0bd4-131">Los mensajes entrantes están llegando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="a0bd4-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="a0bd4-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="a0bd4-133">Los mensajes salientes están en proceso de envío.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="a0bd4-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="a0bd4-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="a0bd4-135">Los mensajes salientes están pendientes (es decir, están en la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="a0bd4-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0bd4-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0bd4-136">Return value</span></span>

<span data-ttu-id="a0bd4-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0bd4-137">S_OK</span></span> 
  
> <span data-ttu-id="a0bd4-138">El cierre de sesión se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0bd4-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0bd4-139">Remarks</span></span>

<span data-ttu-id="a0bd4-140">El **método IMsgStore::StoreLogoff** ejerce control sobre la interacción del almacén de mensajes y los proveedores de transporte durante el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="a0bd4-141">La **llamada a StoreLogoff** solo es válida para los almacenes de mensajes que solo usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="a0bd4-142">Por ejemplo, cuando dos clientes usan el mismo almacén de mensajes y uno de ellos llama a **StoreLogoff,** el almacén de mensajes se libera inmediatamente y el control se devuelve al cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a0bd4-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="a0bd4-143">Notes to implementers</span></span>

<span data-ttu-id="a0bd4-144">Guarde las marcas que se pasan a **StoreLogoff** y pásalos cuando llame al método [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md)</span><span class="sxs-lookup"><span data-stu-id="a0bd4-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="a0bd4-145">No llame a **StoreLogoffTransports hasta** que el recuento de referencias del almacén de mensajes caiga a cero.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="a0bd4-146">Varias llamadas a **StoreLogoffTransports** simplemente sobrescriben las marcas guardadas.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="a0bd4-147">Si no se ha realizado ninguna llamada a **StoreLogoff** antes de que el recuento de referencias del almacén de mensajes alcance cero, establezca la marca LOGOFF_ABORT en el parámetro  _ulFlags_ que pase a **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="a0bd4-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0bd4-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0bd4-148">See also</span></span>



[<span data-ttu-id="a0bd4-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a0bd4-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="a0bd4-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="a0bd4-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="a0bd4-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a0bd4-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="a0bd4-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a0bd4-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

