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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326498"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="1461f-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="1461f-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="1461f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1461f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1461f-105">Solicita la liberación ordenada de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1461f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1461f-106">Parameters</span></span>

 <span data-ttu-id="1461f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1461f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1461f-108">[in, out] Una máscara de máscara de marcadores que controla cómo se produce la cierre de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="1461f-109">En la entrada, todas las marcas de este parámetro se excluyen mutuamente; solo se puede establecer una de las siguientes marcas por llamada:</span><span class="sxs-lookup"><span data-stu-id="1461f-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="1461f-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="1461f-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="1461f-111">Cualquier actividad de proveedor de transporte para este almacén debe detenerse antes del cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1461f-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="1461f-112">El control se devuelve al cliente después de que se detenga la actividad y la cola MAPI haya cerrado sesión en el almacén.</span><span class="sxs-lookup"><span data-stu-id="1461f-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="1461f-113">Si se está llevando a cabo alguna actividad de transporte, no se produce el cierre de sesión y no se produce ningún cambio en la cola MAPI ni en el comportamiento del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1461f-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="1461f-114">Si actualmente no hay actividad, la cola MAPI libera el almacén.</span><span class="sxs-lookup"><span data-stu-id="1461f-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="1461f-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="1461f-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="1461f-116">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que se envíe todo el correo saliente que está listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="1461f-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="1461f-117">Si el almacén de mensajes tiene la bandeja de entrada predeterminada, se recibe cualquier mensaje en proceso y, a continuación, se deshabilita la recepción.</span><span class="sxs-lookup"><span data-stu-id="1461f-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="1461f-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="1461f-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="1461f-119">La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que finalice el procesamiento de los mensajes pendientes.</span><span class="sxs-lookup"><span data-stu-id="1461f-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="1461f-120">No se deben procesar mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="1461f-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="1461f-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="1461f-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="1461f-122">Funciona igual que la marca LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="1461f-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="1461f-123">La marca LOGOFF_PURGE devuelve el control al autor de la llamada después de completarse.</span><span class="sxs-lookup"><span data-stu-id="1461f-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="1461f-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="1461f-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="1461f-125">El cierre de sesión no debe producirse si tiene lugar una actividad de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1461f-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="1461f-126">El tipo de actividad que se lleva a cabo se devuelve como una marca en la salida.</span><span class="sxs-lookup"><span data-stu-id="1461f-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="1461f-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="1461f-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="1461f-128">El cierre de sesión puede completarse.</span><span class="sxs-lookup"><span data-stu-id="1461f-128">The logoff can complete.</span></span> <span data-ttu-id="1461f-129">Se han lanzado todos los recursos asociados con el almacén y el objeto se ha invalidado.</span><span class="sxs-lookup"><span data-stu-id="1461f-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="1461f-130">La cola MAPI ha realizado o realizará todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="1461f-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="1461f-131">En este momento, solo debe llamarse al método **IUnknown:: Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="1461f-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="1461f-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="1461f-133">Un mensaje se encuentra actualmente en el almacén de uno o más proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1461f-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="1461f-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1461f-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="1461f-135">Uno o más proveedores de transporte están enviando un mensaje desde el almacén en este momento.</span><span class="sxs-lookup"><span data-stu-id="1461f-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="1461f-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="1461f-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="1461f-137">Actualmente hay mensajes en la cola de salida de la tienda.</span><span class="sxs-lookup"><span data-stu-id="1461f-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1461f-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1461f-138">Return value</span></span>

<span data-ttu-id="1461f-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="1461f-139">S_OK</span></span> 
  
> <span data-ttu-id="1461f-140">El procedimiento de cierre de sesión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1461f-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1461f-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1461f-141">Remarks</span></span>

<span data-ttu-id="1461f-142">El método **IMAPISupport:: StoreLogoffTransports** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1461f-143">Los proveedores de almacenamiento de mensajes llaman a **StoreLogoffTransports** para dar a las aplicaciones cliente algún control sobre cómo administra MAPI la actividad del proveedor de transporte a medida que se cierra un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="1461f-144">Si otro proceso tiene la tienda que se va a cerrar sesión abierta para el mismo perfil, MAPI omite una llamada a **StoreLogoffTransports** y devuelve la marca LOGOFF_COMPLETE en el parámetro _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1461f-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1461f-145">El comportamiento del proveedor de almacenamiento tras la devolución de **StoreLogoffTransports** debe basarse en el valor de _lpulFlags_, que indica el estado del sistema y transmite instrucciones de cliente para el comportamiento de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1461f-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1461f-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1461f-146">Notes to callers</span></span>

 <span data-ttu-id="1461f-147">**StoreLogoffTransports** se suele llamar desde un método [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) del proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="1461f-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="1461f-148">Sin embargo, también se puede llamar desde el método **IUnknown:: Release** del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="1461f-149">Implemente el método **Release** del almacén de mensajes para poder comprobar si se ha producido una llamada a **StoreLogoffTransports** .</span><span class="sxs-lookup"><span data-stu-id="1461f-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="1461f-150">Si no se ha realizado una llamada, llame a **StoreLogoffTransports** con la marca LOGOFF_ABORT establecida.</span><span class="sxs-lookup"><span data-stu-id="1461f-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="1461f-151">El parámetro _lpulFlags_ se establece en una marca que indica cómo el cliente requiere que se cierre el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1461f-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="1461f-152">DeTermine la configuración adecuada para _ulFlags_ basada en la configuración del parámetro correspondiente en la llamada a **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="1461f-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="1461f-153">Es decir, si un cliente llama al método **StoreLogoff** con _ULFLAGS_ establecido en LOGOFF_ORDERLY, debe llamar a **STORELOGOFFTRANSPORTS** con _ulFlags_ establecido en LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="1461f-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="1461f-154">Para obtener más información acerca del proceso de cierre de sesión del almacén de mensajes, consulte [apagar un proveedor de almacenamiento de mensajes](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1461f-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1461f-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="1461f-155">See also</span></span>



[<span data-ttu-id="1461f-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1461f-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="1461f-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1461f-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="1461f-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1461f-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

