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
ms.openlocfilehash: a55fc361120472473bcba70152c153fb7824fb9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566554"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="c617c-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="c617c-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="c617c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c617c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c617c-105">Permite el cierre de sesión ordenada del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c617c-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c617c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c617c-106">Parameters</span></span>

 <span data-ttu-id="c617c-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c617c-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="c617c-108">[entrada, salida] Una máscara de bits de indicadores que controla el cierre de sesión desde el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c617c-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="c617c-109">En la entrada, todos los indicadores que se hayan establecido para este parámetro son mutuamente excluyentes; un autor de la llamada debe especificar sólo una marca por llamada.</span><span class="sxs-lookup"><span data-stu-id="c617c-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="c617c-110">Las siguientes marcas son válidas en la entrada:</span><span class="sxs-lookup"><span data-stu-id="c617c-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="c617c-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="c617c-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="c617c-112">Cualquier actividad de proveedor de transporte para este almacén de mensajes se debe detener antes de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c617c-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="c617c-113">Control se devuelve al autor de la llamada después de que se ha detenido la actividad.</span><span class="sxs-lookup"><span data-stu-id="c617c-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="c617c-114">Si está produciendo alguna actividad del proveedor de transporte, no se produce el cierre de sesión y se produce ningún cambio en el comportamiento de los proveedores de cola de impresión o de transporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="c617c-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="c617c-115">Si la actividad del proveedor de transporte está inactivo, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="c617c-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="c617c-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="c617c-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="c617c-117">No debe esperar el almacén de mensajes para mensajes de proveedores de transporte antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="c617c-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="c617c-118">Se envían los mensajes salientes que están listos para ser enviados.</span><span class="sxs-lookup"><span data-stu-id="c617c-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="c617c-119">Si este almacén contiene la Bandeja de entrada predeterminada, se reciben los mensajes en proceso y, a continuación, se deshabilita la recepción de más.</span><span class="sxs-lookup"><span data-stu-id="c617c-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="c617c-120">Una vez finalizada toda la actividad, la cola MAPI libera el almacén y control se devuelve inmediatamente al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c617c-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="c617c-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="c617c-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="c617c-122">El almacén de mensajes no debe esperar para obtener información de los proveedores de transporte antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="c617c-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="c617c-123">Los mensajes que se están procesando actualmente están completados, pero no los mensajes nuevos se procesan.</span><span class="sxs-lookup"><span data-stu-id="c617c-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="c617c-124">Una vez finalizada toda la actividad, la cola MAPI libera el almacén e inmediatamente el control se devuelve al proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c617c-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="c617c-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="c617c-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="c617c-126">El cierre de sesión debe trabajar el mismo como si se establece la marca LOGOFF_NO_WAIT, pero debe llamar al método de la [IXPLogon::FlushQueues](ixplogon-flushqueues.md) o [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) para los proveedores de transporte apropiado.</span><span class="sxs-lookup"><span data-stu-id="c617c-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="c617c-127">El indicador LOGOFF_PURGE devuelve el control al autor de la llamada después de la finalización.</span><span class="sxs-lookup"><span data-stu-id="c617c-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="c617c-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="c617c-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="c617c-129">Si está produciendo alguna actividad del proveedor de transporte, no debe producirse el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c617c-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="c617c-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="c617c-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="c617c-131">Actualmente llegan mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="c617c-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="c617c-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c617c-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="c617c-133">Los mensajes salientes están en proceso de enviarse.</span><span class="sxs-lookup"><span data-stu-id="c617c-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="c617c-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="c617c-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="c617c-135">Los mensajes salientes son pendientes (es decir, se encuentran en la Bandeja de salida).</span><span class="sxs-lookup"><span data-stu-id="c617c-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c617c-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c617c-136">Return value</span></span>

<span data-ttu-id="c617c-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="c617c-137">S_OK</span></span> 
  
> <span data-ttu-id="c617c-138">El cierre de sesión que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c617c-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c617c-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c617c-139">Remarks</span></span>

<span data-ttu-id="c617c-140">El método **IMsgStore::StoreLogoff** ejerce control a través de la interacción del mensaje almacenar y los proveedores de transporte durante el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c617c-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="c617c-141">Al llamar a **StoreLogoff** sólo es válido para los almacenes de mensajes que se usan solo por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c617c-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="c617c-142">Por ejemplo, cuando dos clientes están utilizando el mismo almacén de mensajes y uno de ellos llama a **StoreLogoff**, inmediatamente se libera el almacén de mensajes y el control se devuelve al cliente que llama.</span><span class="sxs-lookup"><span data-stu-id="c617c-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c617c-143">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="c617c-143">Notes to implementers</span></span>

<span data-ttu-id="c617c-144">Guarde los indicadores que se pasan al **StoreLogoff** y páselos al llamar al método [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="c617c-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="c617c-145">No llame a **StoreLogoffTransports** hasta que el recuento de referencia del almacén de mensajes cae a cero.</span><span class="sxs-lookup"><span data-stu-id="c617c-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="c617c-146">Varias llamadas a **StoreLogoffTransports** simplemente sobrescribirán los indicadores de guardado.</span><span class="sxs-lookup"><span data-stu-id="c617c-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="c617c-147">Si no se ha realizado ninguna llamada a **StoreLogoff** antes de que el mensaje recuento de referencia de la tienda llega a cero, establecer el indicador LOGOFF_ABORT en el parámetro _ulFlags_ que se pasa a **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="c617c-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c617c-148">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c617c-148">See also</span></span>



[<span data-ttu-id="c617c-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c617c-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="c617c-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="c617c-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="c617c-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c617c-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="c617c-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c617c-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

