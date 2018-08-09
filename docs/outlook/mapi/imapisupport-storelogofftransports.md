---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817570"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="9a8f4-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="9a8f4-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="9a8f4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a8f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a8f4-105">Solicita la versión ordenada de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9a8f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a8f4-106">Parameters</span></span>

 <span data-ttu-id="9a8f4-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a8f4-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="9a8f4-108">[entrada, salida] Una máscara de bits de indicadores que controla cómo se produce el cierre de sesión de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="9a8f4-109">En la entrada, todos los indicadores para este parámetro son mutuamente excluyentes; por llamada, se puede establecer solo uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="9a8f4-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="9a8f4-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="9a8f4-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="9a8f4-111">Cualquier actividad de proveedor de transporte para este almacén se debe detener antes de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="9a8f4-112">Control se devuelve al cliente una vez que se ha detenido la actividad y la cola MAPI ha cerrado el almacén de la sesión.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="9a8f4-113">Si está produciendo alguna actividad de transporte, no se produce el cierre de sesión y se produce ningún cambio en el comportamiento del proveedor de cola de impresión o de transporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="9a8f4-114">Si actualmente no hay ninguna actividad, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="9a8f4-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="9a8f4-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="9a8f4-116">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente se envía el correo saliente después de todo que está listo para ser enviado.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="9a8f4-117">Si el almacén de mensajes tiene la Bandeja de entrada predeterminada, se recibe ningún mensaje en el proceso y, a continuación, se deshabilita la recepción de más.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="9a8f4-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="9a8f4-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="9a8f4-119">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que se complete cualquiera mensajes pendientes de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="9a8f4-120">No hay mensajes nuevos se deben procesar.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="9a8f4-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="9a8f4-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="9a8f4-122">Funciona de la misma que la marca LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="9a8f4-123">El indicador LOGOFF_PURGE devuelve el control al autor de la llamada después de la finalización.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="9a8f4-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="9a8f4-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="9a8f4-125">El cierre de sesión no debe producirse si está produciendo alguna actividad del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="9a8f4-126">Se devuelve el tipo de actividad que tiene lugar como una marca en la salida.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="9a8f4-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="9a8f4-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="9a8f4-128">Puede completar el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-128">The logoff can complete.</span></span> <span data-ttu-id="9a8f4-129">Se han publicado todos los recursos asociados con el almacén y el objeto se ha invalidado.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="9a8f4-130">La cola MAPI ha llevado a cabo o llevará a cabo todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="9a8f4-131">Método de **IUnknown:: Release** del almacén de mensajes sólo se debe llamar en este momento.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="9a8f4-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="9a8f4-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="9a8f4-133">Un mensaje procede actualmente en el almacén de uno o varios proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="9a8f4-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="9a8f4-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="9a8f4-135">Actualmente se que se envía un mensaje desde el almacén por uno o varios proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="9a8f4-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9a8f4-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="9a8f4-137">Actualmente hay mensajes en la cola de salida para el almacén.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a8f4-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a8f4-138">Return value</span></span>

<span data-ttu-id="9a8f4-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a8f4-139">S_OK</span></span> 
  
> <span data-ttu-id="9a8f4-140">El procedimiento de cierre de sesión fue correcto.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a8f4-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a8f4-141">Remarks</span></span>

<span data-ttu-id="9a8f4-142">El método **IMAPISupport::StoreLogoffTransports** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9a8f4-143">Los proveedores de almacén de mensajes llamada **StoreLogoffTransports** para que las aplicaciones cliente de algún control sobre cómo se está cerrando la actividad de proveedor de transporte MAPI identificadores como un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="9a8f4-144">Si otro proceso tiene el almacén que se cerró sesión abrir para el mismo perfil, MAPI omite una llamada a **StoreLogoffTransports** y devuelve la marca LOGOFF_COMPLETE en el parámetro _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9a8f4-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="9a8f4-145">El comportamiento del proveedor de almacén de seguir la devolución de **StoreLogoffTransports** debe basarse en el valor de _lpulFlags_, que indica el estado del sistema y transmite las instrucciones del cliente para el comportamiento de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9a8f4-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9a8f4-146">Notes to callers</span></span>

 <span data-ttu-id="9a8f4-147">**StoreLogoffTransports** normalmente se llama desde (método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ) del proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="9a8f4-148">Sin embargo, también se puede llamar desde el método **IUnknown:: Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="9a8f4-149">Implementar el método de la **versión** de su almacén de mensajes de modo que puede comprobar si una llamada a **StoreLogoffTransports** se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="9a8f4-150">Si no se ha producido una llamada, llame a **StoreLogoffTransports** con el conjunto de marca LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="9a8f4-151">El parámetro _lpulFlags_ se establece en una marca que indica cómo el cliente requiere que el almacén de mensajes para cerrarse.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="9a8f4-152">Determinar la configuración adecuada para _ulFlags_ según la configuración del parámetro correspondiente en la llamada a **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="9a8f4-153">Es decir, si un cliente llama al método **StoreLogoff** con _ulFlags_ establecida en LOGOFF_ORDERLY, debe llamar a **StoreLogoffTransports** con _ulFlags_ establecida en LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="9a8f4-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="9a8f4-154">Para obtener más información acerca del proceso de cierre de sesión del almacén de mensajes, vea [Cerrando hacia abajo un mensaje Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9a8f4-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a8f4-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a8f4-155">See also</span></span>



[<span data-ttu-id="9a8f4-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="9a8f4-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="9a8f4-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9a8f4-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="9a8f4-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a8f4-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

