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
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421385"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="a3a49-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="a3a49-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="a3a49-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3a49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3a49-105">Solicita la publicación por orden de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3a49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3a49-106">Parameters</span></span>

 <span data-ttu-id="a3a49-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3a49-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a3a49-108">[entrada, salida] Máscara de bits de marcas que controla cómo se produce el cierre de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="a3a49-109">En la entrada, todas las marcas de este parámetro son mutuamente excluyentes; solo se puede establecer una de las siguientes marcas por llamada:</span><span class="sxs-lookup"><span data-stu-id="a3a49-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="a3a49-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="a3a49-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="a3a49-111">Cualquier actividad del proveedor de transporte para este almacén debe detenerse antes de cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="a3a49-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="a3a49-112">El control se devuelve al cliente después de detener la actividad y de que la cola MAPI haya cerrado sesión en el almacén.</span><span class="sxs-lookup"><span data-stu-id="a3a49-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="a3a49-113">Si se produce alguna actividad de transporte, no se produce el cierre de sesión y no se produce ningún cambio en la cola MAPI ni en el comportamiento del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a3a49-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="a3a49-114">Si actualmente no hay ninguna actividad, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="a3a49-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="a3a49-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="a3a49-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="a3a49-116">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que se envíe todo el correo saliente que esté listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="a3a49-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="a3a49-117">Si el almacén de mensajes tiene la Bandeja de entrada predeterminada, se recibe cualquier mensaje dentro del proceso y, a continuación, se deshabilita la recepción adicional.</span><span class="sxs-lookup"><span data-stu-id="a3a49-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="a3a49-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="a3a49-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="a3a49-119">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que finalice el procesamiento de los mensajes pendientes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="a3a49-120">No se deben procesar mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="a3a49-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="a3a49-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="a3a49-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="a3a49-122">Funciona igual que la marca LOGOFF_NO_WAIT de datos.</span><span class="sxs-lookup"><span data-stu-id="a3a49-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="a3a49-123">La LOGOFF_PURGE devuelve el control al autor de la llamada después de finalizar.</span><span class="sxs-lookup"><span data-stu-id="a3a49-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="a3a49-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="a3a49-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="a3a49-125">El cierre de sesión no debe producirse si se está llevando a cabo alguna actividad del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a3a49-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="a3a49-126">El tipo de actividad que tiene lugar se devuelve como una marca en el resultado.</span><span class="sxs-lookup"><span data-stu-id="a3a49-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="a3a49-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="a3a49-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="a3a49-128">El cierre de sesión puede completarse.</span><span class="sxs-lookup"><span data-stu-id="a3a49-128">The logoff can complete.</span></span> <span data-ttu-id="a3a49-129">Se han liberado todos los recursos asociados con el almacén y se ha invalidado el objeto.</span><span class="sxs-lookup"><span data-stu-id="a3a49-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="a3a49-130">La cola MAPI ha realizado o realizará todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="a3a49-131">Solo se debe llamar al método **IUnknown::Release** del almacén de mensajes en este momento.</span><span class="sxs-lookup"><span data-stu-id="a3a49-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="a3a49-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="a3a49-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="a3a49-133">Actualmente, hay un mensaje en el almacén procedente de uno o más proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="a3a49-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="a3a49-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="a3a49-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="a3a49-135">Actualmente, uno o varios proveedores de transporte envían un mensaje desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="a3a49-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="a3a49-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="a3a49-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="a3a49-137">Actualmente hay mensajes en la cola de salida para el almacén.</span><span class="sxs-lookup"><span data-stu-id="a3a49-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3a49-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a49-138">Return value</span></span>

<span data-ttu-id="a3a49-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3a49-139">S_OK</span></span> 
  
> <span data-ttu-id="a3a49-140">El procedimiento de cierre de sesión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3a49-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3a49-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3a49-141">Remarks</span></span>

<span data-ttu-id="a3a49-142">El **método IMAPISupport::StoreLogoffTransports** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a3a49-143">Los proveedores de almacén de mensajes llaman a **StoreLogoffTransports** para proporcionar a las aplicaciones cliente cierto control sobre cómo MAPI controla la actividad del proveedor de transporte mientras se cierra un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="a3a49-144">Si otro proceso tiene que haber cerrado la sesión del almacén para el mismo perfil, MAPI omite una llamada a **StoreLogoffTransports** y devuelve la marca LOGOFF_COMPLETE en el parámetro _lpulFlags._</span><span class="sxs-lookup"><span data-stu-id="a3a49-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a3a49-145">El comportamiento del proveedor del almacén después de la devolución de **StoreLogoffTransports** debe basarse en el valor de  _lpulFlags_, que indica el estado del sistema y transmite instrucciones de cliente para el comportamiento de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="a3a49-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3a49-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a3a49-146">Notes to callers</span></span>

 <span data-ttu-id="a3a49-147">Normalmente se llama a **StoreLogoffTransports** desde el método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) de un proveedor de almacén.</span><span class="sxs-lookup"><span data-stu-id="a3a49-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="a3a49-148">Sin embargo, también se puede llamar desde el método **IUnknown::Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="a3a49-149">Implemente **el método Release** del almacén de mensajes para que pueda comprobar si se ha producido o no una llamada a **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="a3a49-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="a3a49-150">Si no se ha producido una llamada, llame **a StoreLogoffTransports** con LOGOFF_ABORT marca establecida.</span><span class="sxs-lookup"><span data-stu-id="a3a49-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="a3a49-151">El  _parámetro lpulFlags_ se establece en una marca que indica cómo el cliente requiere que se cierre el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a3a49-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="a3a49-152">Determine la configuración adecuada para  _ulFlags_ en función de la configuración del parámetro correspondiente en la llamada **a StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="a3a49-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="a3a49-153">Es decir, si un cliente llamó al método **StoreLogoff** con  _ulFlags_ establecido en LOGOFF_ORDERLY, debe llamar a **StoreLogoffTransports** con  _ulFlags_ establecido en LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="a3a49-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="a3a49-154">Para obtener más información acerca del proceso de cierre de sesión del almacén de mensajes, vea [Apagar un proveedor de almacenamiento de mensajes.](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="a3a49-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3a49-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3a49-155">See also</span></span>



[<span data-ttu-id="a3a49-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="a3a49-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="a3a49-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a3a49-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="a3a49-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3a49-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

