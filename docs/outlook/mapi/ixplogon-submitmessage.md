---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423324"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="00f0f-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="00f0f-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="00f0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00f0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00f0f-105">Indica que la cola MAPI tiene un mensaje para que el proveedor de transporte entregue.</span><span class="sxs-lookup"><span data-stu-id="00f0f-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="00f0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00f0f-106">Parameters</span></span>

 <span data-ttu-id="00f0f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00f0f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="00f0f-108">[entrada] Máscara de bits de marcas que controla cómo se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="00f0f-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="00f0f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="00f0f-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="00f0f-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="00f0f-111">La cola MAPI llama a un proveedor de transporte con un mensaje que se aplazó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="00f0f-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="00f0f-112">El identificador de entrada del mensaje es el mismo que cuando se aplazó.</span><span class="sxs-lookup"><span data-stu-id="00f0f-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="00f0f-113">El mensaje se aplazó pasando su identificador de entrada de nuevo a la cola MAPI mediante el método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_SENTDEFERRED entrada.</span><span class="sxs-lookup"><span data-stu-id="00f0f-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="00f0f-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="00f0f-114">_lpMessage_</span></span>
  
> <span data-ttu-id="00f0f-115">[entrada] Puntero a un objeto de mensaje (que representa el mensaje que se va a entregar) que tiene permiso de lectura y escritura, que el proveedor de transporte usa para obtener acceso a ese mensaje y manipularlo.</span><span class="sxs-lookup"><span data-stu-id="00f0f-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="00f0f-116">Este objeto permanece válido hasta que el proveedor de transporte vuelve de una llamada posterior al método [IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="00f0f-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="00f0f-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="00f0f-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="00f0f-118">[salida] Puntero a una variable en la que el proveedor de transporte devuelve el valor de referencia asignado a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="00f0f-119">La cola MAPI pasa este valor de referencia en llamadas posteriores para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="00f0f-120">La cola MAPI inicializa el valor en 0 antes de devolverlo al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="00f0f-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="00f0f-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="00f0f-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="00f0f-122">[salida] Puntero a una variable que corresponde al valor MAPI_E_WAIT o MAPI_E_NETWORK_ERROR error devuelto por **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="00f0f-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00f0f-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00f0f-123">Return value</span></span>

<span data-ttu-id="00f0f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="00f0f-124">S_OK</span></span> 
  
> <span data-ttu-id="00f0f-125">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="00f0f-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="00f0f-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="00f0f-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="00f0f-127">El proveedor de transporte no puede controlar el mensaje porque está realizando otra operación.</span><span class="sxs-lookup"><span data-stu-id="00f0f-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="00f0f-128">Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar **a EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="00f0f-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="00f0f-129">La cola MAPI volverá a intentar la llamada **SubmitMessage** más adelante.</span><span class="sxs-lookup"><span data-stu-id="00f0f-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="00f0f-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="00f0f-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="00f0f-131">Aunque el proveedor de transporte solicitó que la cola MAPI vuelva a enviar el mensaje en una llamada **SpoolerNotify** anterior, las condiciones han cambiado desde entonces y el mensaje no debe reenviarse.</span><span class="sxs-lookup"><span data-stu-id="00f0f-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="00f0f-132">La cola MAPI pasará a controlar otra cosa.</span><span class="sxs-lookup"><span data-stu-id="00f0f-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="00f0f-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="00f0f-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="00f0f-134">Un error de red impidió que la operación se completara correctamente.</span><span class="sxs-lookup"><span data-stu-id="00f0f-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="00f0f-135">El  _parámetro lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI vuelva a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="00f0f-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="00f0f-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="00f0f-137">El proveedor de transporte no puede controlar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="00f0f-138">La cola MAPI debe intentar encontrar otro proveedor de transporte para él.</span><span class="sxs-lookup"><span data-stu-id="00f0f-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="00f0f-139">Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar **a EndMessage**.</span><span class="sxs-lookup"><span data-stu-id="00f0f-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="00f0f-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="00f0f-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="00f0f-141">Un problema temporal impide que el proveedor de transporte controle el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="00f0f-142">El  _parámetro lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI vuelva a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00f0f-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00f0f-143">Remarks</span></span>

<span data-ttu-id="00f0f-144">La cola MAPI llama al método **IXPLogon::SubmitMessage** cuando tiene un mensaje para que el proveedor de transporte entregue.</span><span class="sxs-lookup"><span data-stu-id="00f0f-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="00f0f-145">El mensaje se pasa al proveedor de transporte mediante el parámetro _lpMessage._</span><span class="sxs-lookup"><span data-stu-id="00f0f-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="00f0f-146">Si el proveedor está listo para aceptar el mensaje, debe devolver un valor de referencia mediante el parámetro  _lpulMsgRef,_ procesar el objeto pasado y devolver el valor apropiado (normalmente S_OK).</span><span class="sxs-lookup"><span data-stu-id="00f0f-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="00f0f-147">Si el proveedor no está preparado para controlar la transferencia, debe devolver un valor de error y, opcionalmente, otro valor devuelto de MAPI en  _lpulReturnParm_ para indicar cuánto tiempo debe esperar la cola MAPI antes de volver a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="00f0f-148">La implementación de este método por parte de un proveedor de transporte puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00f0f-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="00f0f-149">Coloque el mensaje en una cola interna para esperar la transmisión, posiblemente copiando el mensaje en el almacenamiento local y devolviendo.</span><span class="sxs-lookup"><span data-stu-id="00f0f-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="00f0f-150">Intente realizar la transmisión real y volver cuando la transmisión finalice, ya sea correcta o incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="00f0f-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="00f0f-151">Determinar si se va a enviar el mensaje después de comprobar el recurso implicado.</span><span class="sxs-lookup"><span data-stu-id="00f0f-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="00f0f-152">En este caso, si el recurso es gratuito, el proveedor puede bloquear el recurso, preparar el mensaje y enviarlo.</span><span class="sxs-lookup"><span data-stu-id="00f0f-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="00f0f-153">Si el recurso está ocupado, el proveedor puede preparar el mensaje y aplazar el envío más adelante.</span><span class="sxs-lookup"><span data-stu-id="00f0f-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="00f0f-154">La técnica preferida para la transmisión de mensajes depende del proveedor de transporte y del número esperado de procesos que compiten por los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="00f0f-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="00f0f-155">Durante una **llamada SubmitMessage,** el proveedor de transporte controla la transferencia de datos del mensaje desde el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="00f0f-156">Sin embargo, el proveedor de transporte debe asignar un valor de referencia al mensaje, al que devuelve un puntero en  _lpulMsgRef_, antes de transferir datos.</span><span class="sxs-lookup"><span data-stu-id="00f0f-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="00f0f-157">Lo hace porque, en cualquier momento durante el proceso, la cola MAPI puede llamar al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) con la marca NOTIFY_CANCEL_MESSAGE establecida para indicar al proveedor que debe liberar los objetos abiertos y detener la transferencia de mensajes.</span><span class="sxs-lookup"><span data-stu-id="00f0f-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="00f0f-158">El proveedor de transporte no debe enviar ninguna propiedad notransmitible del mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="00f0f-159">Cuando encuentre dicha propiedad, debe seguir procesando la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="00f0f-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="00f0f-160">El proveedor debe hacer todo lo posible para no mostrar MAPI_P1 de destinatarios como parte del contenido del mensaje transmitido; el proveedor debe usar esta información de destinatario solo con fines de direccionamiento.</span><span class="sxs-lookup"><span data-stu-id="00f0f-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="00f0f-161">MAPI_P1 destinatarios son destinatarios generados internamente que se usan para reenviar mensajes; no deben transmitirse.</span><span class="sxs-lookup"><span data-stu-id="00f0f-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="00f0f-162">En su lugar, use los demás destinatarios para transmitir información del destinatario.</span><span class="sxs-lookup"><span data-stu-id="00f0f-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="00f0f-163">El propósito de este acuerdo es permitir que los destinatarios que vuelvan a enviar vean exactamente la misma tabla de destinatarios que los destinatarios originales.</span><span class="sxs-lookup"><span data-stu-id="00f0f-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="00f0f-164">Durante una **llamada SubmitMessage,** la cola MAPI procesa métodos para objetos que se abren durante la transferencia del mensaje y procesa los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="00f0f-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="00f0f-165">Este procesamiento puede tardar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="00f0f-165">This processing can take a long time.</span></span> <span data-ttu-id="00f0f-166">Los proveedores de transporte pueden llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este procesamiento para liberar tiempo de CPU para otras tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="00f0f-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="00f0f-167">Todos los destinatarios del mensaje están visibles en la tabla de destinatarios del mensaje que pasó originalmente la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="00f0f-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="00f0f-168">El proveedor de transporte debe procesar solo los destinatarios que pueda controlar , en función del identificador de entrada, el tipo de dirección o ambos, y que aún no tengan la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="00f0f-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="00f0f-169">Si **PR_RESPONSIBILITY** está establecido en TRUE, otro proveedor de transporte controla ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="00f0f-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="00f0f-170">Cuando el proveedor complete el procesamiento suficiente de un destinatario para determinar si puede controlar los mensajes de ese destinatario, debe establecer la propiedad **PR_RESPONSIBILITY** del destinatario en TRUE en el mensaje pasado.</span><span class="sxs-lookup"><span data-stu-id="00f0f-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="00f0f-171">Normalmente, el proveedor toma esta determinación una vez completada la entrega del mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="00f0f-172">Normalmente, el proveedor de transporte no vuelve de una llamada **SubmitMessage** hasta que completa la transferencia de datos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f0f-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="00f0f-173">Si no se devuelve ningún error, la siguiente llamada de la cola MAPI al proveedor es una llamada al método [IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="00f0f-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="00f0f-174">Si **SubmitMessage** devuelve un error, la cola MAPI libera el mensaje en proceso sin guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="00f0f-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="00f0f-175">Si el proveedor de transporte requiere que se guarden los cambios de mensajes, debe llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="00f0f-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="00f0f-176">En caso de errores que se producen debido a problemas de transporte, la cola MAPI conserva el mensaje, pero retrasa el reenvío del mensaje al proveedor de transporte en función del valor devuelto en  _lpulReturnParm_.</span><span class="sxs-lookup"><span data-stu-id="00f0f-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="00f0f-177">El proveedor de transporte debe rellenar ese valor si su valor devuelto de **SubmitMessage** es MAPI_E_WAIT o MAPI_E_NETWORK_ERROR.</span><span class="sxs-lookup"><span data-stu-id="00f0f-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="00f0f-178">Si se produce una condición de error grave, el proveedor de transporte debe llamar al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_CRITICAL_ERROR datos.</span><span class="sxs-lookup"><span data-stu-id="00f0f-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00f0f-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00f0f-179">See also</span></span>



[<span data-ttu-id="00f0f-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="00f0f-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="00f0f-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="00f0f-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="00f0f-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="00f0f-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="00f0f-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="00f0f-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="00f0f-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="00f0f-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="00f0f-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00f0f-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

