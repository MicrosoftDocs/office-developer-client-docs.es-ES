---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5429f98a0335ae99b719d0f15b66a95ba87430e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818020"
---
# <a name="ixplogontransportnotify"></a><span data-ttu-id="20088-103">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="20088-103">IXPLogon::TransportNotify</span></span>

<span data-ttu-id="20088-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20088-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20088-105">Indica la aparición de un evento sobre el que el proveedor de transporte solicita la notificación.</span><span class="sxs-lookup"><span data-stu-id="20088-105">Signals the occurrence of an event about which the transport provider requested notification.</span></span>
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a><span data-ttu-id="20088-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20088-106">Parameters</span></span>

 <span data-ttu-id="20088-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="20088-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="20088-108">[entrada, salida] Una máscara de bits de marcadores que indica los eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="20088-108">[in, out] A bitmask of flags that signals notification events.</span></span> <span data-ttu-id="20088-109">Las siguientes marcas se pueden establecer mediante la cola MAPI en la entrada y deben devolverse sin cambios en la salida:</span><span class="sxs-lookup"><span data-stu-id="20088-109">The following flags can be set by the MAPI spooler on input and must be returned unchanged on output:</span></span>
    
<span data-ttu-id="20088-110">NOTIFY_ABORT_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="20088-110">NOTIFY_ABORT_DEFERRED</span></span> 
  
> <span data-ttu-id="20088-111">Notifica al proveedor de transporte que se ha aplazado un mensaje para el que acepta responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="20088-111">Notifies the transport provider that a message for which it accepted responsibility is being deferred.</span></span> <span data-ttu-id="20088-112">Sólo los proveedores de transporte que admiten aplazamiento deben admitir esta marca.</span><span class="sxs-lookup"><span data-stu-id="20088-112">Only transport providers that support deferral must support this flag.</span></span> <span data-ttu-id="20088-113">El parámetro _lppvData_ apunta el identificador de entrada del mensaje cancelado.</span><span class="sxs-lookup"><span data-stu-id="20088-113">The  _lppvData_ parameter points to the entry identifier of the canceled message.</span></span> <span data-ttu-id="20088-114">Los mensajes que no haya procesado la cola MAPI aún se pueden aplazar llamando al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) .</span><span class="sxs-lookup"><span data-stu-id="20088-114">Messages that the MAPI spooler has not processed can still be deferred by calling the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method.</span></span> 
    
<span data-ttu-id="20088-115">NOTIFY_BEGIN_INBOUND</span><span class="sxs-lookup"><span data-stu-id="20088-115">NOTIFY_BEGIN_INBOUND</span></span> 
  
> <span data-ttu-id="20088-116">La cola MAPI ahora puede aceptar mensajes entrantes para esta sesión de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20088-116">The MAPI spooler can now accept inbound messages for this transport provider session.</span></span> <span data-ttu-id="20088-117">La cola MAPI con regularidad llama al método de [IXPLogon::Poll](ixplogon-poll.md) si el proveedor de transporte establece la marca LOGON_SP_POLL con la llamada a [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="20088-117">The MAPI spooler regularly calls the [IXPLogon::Poll](ixplogon-poll.md) method if the transport provider set the LOGON_SP_POLL flag with the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) call at logon.</span></span> <span data-ttu-id="20088-118">Una vez que se establece la marca NOTIFY_BEGIN_INBOUND, la cola MAPI respeta la marca NOTIFY_NEWMAIL que se pasan en la llamada al método [SpoolerNotify](imapisupport-spoolernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="20088-118">Once the NOTIFY_BEGIN_INBOUND flag is set, the MAPI spooler honors the NOTIFY_NEWMAIL flag passed in the call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method.</span></span> <span data-ttu-id="20088-119">La fila de la tabla de estado de la sesión de proveedor de transporte debe actualizarse antes de devolverlo al llamar al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) .</span><span class="sxs-lookup"><span data-stu-id="20088-119">The status table row for the transport provider session should be updated before returning by calling the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method.</span></span> <span data-ttu-id="20088-120">Los indicadores NOTIFY_BEGIN_INBOUND y NOTIFY_END_INBOUND son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="20088-120">The NOTIFY_BEGIN_INBOUND and NOTIFY_END_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="20088-121">NOTIFY_BEGIN_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="20088-121">NOTIFY_BEGIN_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20088-122">Indica el proveedor de transporte para recorrer los mensajes entrantes lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="20088-122">Signals the transport provider to cycle through inbound messages as quickly as possible.</span></span> <span data-ttu-id="20088-123">Para cumplir con esta notificación, el proveedor de transporte debe establecer la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de la tabla de estado tan pronto como puede, mediante el uso de **ModifyStatusRow**.</span><span class="sxs-lookup"><span data-stu-id="20088-123">To comply with this notification, the transport provider should set the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status table row as soon as it can, by using **ModifyStatusRow**.</span></span> <span data-ttu-id="20088-124">Un ciclo de mensajería entrante finalizada cuando el proveedor determina que ha descargado todo que lo posible o cuando ha recibido una llamada al método **TransportNotify** con el conjunto de marca NOTIFY_END_INBOUND_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="20088-124">An inbound messaging cycle is complete when the provider determines it has downloaded all it can, or when it has received a **TransportNotify** method call with the NOTIFY_END_INBOUND_FLUSH flag set.</span></span> <span data-ttu-id="20088-125">Hasta el final del ciclo de mensajería entrante, el proveedor no debe llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) o en caso contrario, ceder ciclos en el sistema operativo a la entrega de velocidad de los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="20088-125">Until the end of the inbound messaging cycle, the provider should not call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method or otherwise relinquish cycles to the operating system to speed delivery of incoming messages.</span></span> <span data-ttu-id="20088-126">Esto es aceptable porque la cola MAPI utiliza normalmente NOTIFY_BEGIN_INBOUND_FLUSH sólo en respuesta a una solicitud de un usuario, a través de una aplicación cliente, para entregar todos los mensajes ahora.</span><span class="sxs-lookup"><span data-stu-id="20088-126">This is acceptable because the MAPI spooler typically uses NOTIFY_BEGIN_INBOUND_FLUSH only in response to a user's request, via a client application, to deliver all messages now.</span></span> <span data-ttu-id="20088-127">Al final de la operación de vaciado entrante, el proveedor debe usar **SpoolerNotify** para borrar la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** de la fila de estado correspondiente.</span><span class="sxs-lookup"><span data-stu-id="20088-127">At the end of the inbound flush operation, the provider should use **SpoolerNotify** to clear the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** property of its status row.</span></span> 
    
<span data-ttu-id="20088-128">NOTIFY_BEGIN_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="20088-128">NOTIFY_BEGIN_OUTBOUND</span></span> 
  
> <span data-ttu-id="20088-129">Ahora pueden producirse las operaciones de salida para esta sesión de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20088-129">Outbound operations can now occur for this transport provider session.</span></span> <span data-ttu-id="20088-130">Si existen todos los mensajes que se envíen para este proveedor, sigue una llamada al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="20088-130">If there are any messages to be sent for this provider, a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method follows.</span></span> <span data-ttu-id="20088-131">La fila de la tabla de estado para esta sesión debe actualizarse antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="20088-131">The status table row for this session should be updated before returning.</span></span> <span data-ttu-id="20088-132">Los indicadores NOTIFY_BEGIN_OUTBOUND y NOTIFY_END_OUTBOUND son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="20088-132">The NOTIFY_BEGIN_OUTBOUND and NOTIFY_END_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="20088-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="20088-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20088-134">Funciona de manera similar a la marca NOTIFY_BEGIN_INBOUND_FLUSH, pero hace referencia a los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="20088-134">Works similarly to the NOTIFY_BEGIN_INBOUND_FLUSH flag, but refers to outbound messages.</span></span> <span data-ttu-id="20088-135">El indicador de estado correspondiente es STATUS_OUTBOUND_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="20088-135">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
<span data-ttu-id="20088-136">NOTIFY_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="20088-136">NOTIFY_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="20088-137">La cola MAPI debe cancelar la transferencia del mensaje para el que llame los puntos de parámetro _lppvData_ en el valor de 32 bits desde el método **IXPLogon::SubmitMessage** .</span><span class="sxs-lookup"><span data-stu-id="20088-137">The MAPI spooler must cancel transfer of the message for which the  _lppvData_ parameter points to the 32-bit value from the **IXPLogon::SubmitMessage** method call.</span></span> <span data-ttu-id="20088-138">Sin el proveedor de transporte que ha devuelto desde el **SubmitMessage**, **IXPLogon::StartMessage**o llamada al método **IXPLogon::EndMessage** que está asociada con el mensaje, se puede establecer la marca NOTIFY_CANCEL_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="20088-138">The NOTIFY_CANCEL_MESSAGE flag can be set without the transport provider having returned from the **SubmitMessage**, **IXPLogon::StartMessage**, or **IXPLogon::EndMessage** method call that is associated with the message.</span></span> <span data-ttu-id="20088-139">El proveedor de transporte debe devolver tan pronto como sea posible desde el punto de entrada que se encarga del mensaje cancelado.</span><span class="sxs-lookup"><span data-stu-id="20088-139">The transport provider must return as soon as possible from the entry point that is handling the canceled message.</span></span> <span data-ttu-id="20088-140">Para un mensaje entrante que se está procesando actualmente, el proveedor de transporte debe guardar el mensaje entrante dondequiera que actualmente se encuentra almacenada y entregar nuevo a la siguiente hora conveniente.</span><span class="sxs-lookup"><span data-stu-id="20088-140">For an inbound message that is currently being processed, the transport provider should save the incoming message wherever it is presently stored and deliver it again at the next convenient time.</span></span> <span data-ttu-id="20088-141">Se descartan los datos del objeto de mensaje ya almacenados para el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="20088-141">The message object data already stored for the incoming message is discarded.</span></span> <span data-ttu-id="20088-142">Si el proveedor de transporte no se actualizó este valor de 32 bits en el momento **desea iniciar** o **SubmitMessage** , el valor es 0 para los mensajes salientes y 1 para los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="20088-142">If the transport provider did not update this 32-bit value at the **StartMessage** or **SubmitMessage** time, the value is 0 for outbound messages and 1 for inbound messages.</span></span> 
    
<span data-ttu-id="20088-143">NOTIFY_END_INBOUND</span><span class="sxs-lookup"><span data-stu-id="20088-143">NOTIFY_END_INBOUND</span></span> 
  
> <span data-ttu-id="20088-144">Deben dejar de las operaciones de entrada para esta sesión de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20088-144">Inbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="20088-145">La cola MAPI se deja de utilizar el método de **sondeo** y omite NOTIFY_NEWMAIL para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="20088-145">The MAPI spooler ceases to use the **Poll** method and ignores NOTIFY_NEWMAIL for this session.</span></span> <span data-ttu-id="20088-146">Deben realizarse en procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="20088-146">In-process messages should be completed.</span></span> <span data-ttu-id="20088-147">La fila de la tabla de estado de la sesión de transporte debe actualizarse mediante una llamada a [ModifyStatusRow](imapisupport-modifystatusrow.md) antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="20088-147">The status table row for the transport session should be updated by calling [ModifyStatusRow](imapisupport-modifystatusrow.md) before returning.</span></span> <span data-ttu-id="20088-148">Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_INBOUND son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="20088-148">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="20088-149">NOTIFY_END_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="20088-149">NOTIFY_END_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20088-150">Notifica al proveedor de transporte para salir de modo de vaciado entrante.</span><span class="sxs-lookup"><span data-stu-id="20088-150">Notifies the transport provider to come out of inbound flush mode.</span></span> <span data-ttu-id="20088-151">El proveedor de transporte debe detener la descarga, pero descarga debe realizarse en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="20088-151">The transport provider should not stop downloading, but downloading should be done in the background.</span></span> <span data-ttu-id="20088-152">La fila de la tabla de estado de la sesión de transporte debe actualizarse al llamar a **ModifyStatusRow** cuando el proveedor de transporte puede cumplir con esta notificación.</span><span class="sxs-lookup"><span data-stu-id="20088-152">The status table row for the transport session should be updated by calling **ModifyStatusRow** when the transport provider can comply with this notification.</span></span> 
    
<span data-ttu-id="20088-153">NOTIFY_END_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="20088-153">NOTIFY_END_OUTBOUND</span></span> 
  
> <span data-ttu-id="20088-154">Deben dejar de operaciones de salida para esta sesión de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20088-154">Outbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="20088-155">La cola MAPI deja de llamar a **SubmitMessage** y pasa por alto la marca NOTIFY_READYTOSEND **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="20088-155">The MAPI spooler ceases to call **SubmitMessage** and ignores the **SpoolerNotify** NOTIFY_READYTOSEND flag.</span></span> <span data-ttu-id="20088-156">Si hay un mensaje de salida que se está enviando actualmente, no debe detener; Para detener la entrega de un mensaje, use la marca NOTIFY_CANCEL_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="20088-156">If there is an outbound message currently being sent, it should not be stopped; to stop delivery of a message, use the NOTIFY_CANCEL_MESSAGE flag.</span></span> <span data-ttu-id="20088-157">La fila de la tabla de estado para esta sesión debe actualizarse mediante una llamada a **ModifyStatusRow** antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="20088-157">The status table row for this session should be updated by calling **ModifyStatusRow** before returning.</span></span> <span data-ttu-id="20088-158">Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_OUTBOUND son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="20088-158">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="20088-159">NOTIFY_END_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="20088-159">NOTIFY_END_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20088-160">Funciona de forma similar a NOTIFY_END_INBOUND_FLUSH, pero hace referencia a los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="20088-160">Works similarly to NOTIFY_END_INBOUND_FLUSH, but refers to outbound messages.</span></span> <span data-ttu-id="20088-161">El indicador de estado correspondiente es STATUS_OUTBOUND_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="20088-161">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
 <span data-ttu-id="20088-162">_lppvData_</span><span class="sxs-lookup"><span data-stu-id="20088-162">_lppvData_</span></span>
  
> <span data-ttu-id="20088-163">[out] Un puntero a un puntero a datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="20088-163">[out] A pointer to a pointer to event-specific data.</span></span> <span data-ttu-id="20088-164">Para obtener más información acerca de qué _lppvData_ especifica, vea la descripción para el parámetro _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="20088-164">For more information about what  _lppvData_ specifies, see the description for the  _lpulFlags_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20088-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20088-165">Return value</span></span>

<span data-ttu-id="20088-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="20088-166">S_OK</span></span> 
  
> <span data-ttu-id="20088-167">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="20088-167">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20088-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20088-168">Remarks</span></span>

<span data-ttu-id="20088-169">La cola MAPI llama al método de **IXPLogon::TransportNotify** para indicar el proveedor de transporte acerca de los eventos para el que se ha solicitado la notificación.</span><span class="sxs-lookup"><span data-stu-id="20088-169">The MAPI spooler calls the **IXPLogon::TransportNotify** method to signal the transport provider about events for which notification has been requested.</span></span> <span data-ttu-id="20088-170">Estos eventos incluyen una solicitud de cola de impresión MAPI para cancelar la transferencia de un mensaje, el principio o final de las operaciones de transporte de entrada y salida y principio o al final de una operación para borrar una cola de mensajes entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="20088-170">These events include a MAPI spooler request to cancel a message transfer, the beginning or ending of inbound or outbound transport operations, and the beginning or ending of an operation to clear an inbound or outbound message queue.</span></span> 
  
<span data-ttu-id="20088-171">Cuando el usuario intenta cancelar un mensaje que el proveedor de transporte ha aplazado anteriormente, la cola MAPI llama a **TransportNotify**, pasando el NOTIFY_ABORT_DEFERRED y la NOTIFY_CANCEL_MESSAGE marcas en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="20088-171">When the user tries to cancel a message that the transport provider has previously deferred, the MAPI spooler calls **TransportNotify**, passing in both the NOTIFY_ABORT_DEFERRED and NOTIFY_CANCEL_MESSAGE flags in  _ulFlags_.</span></span> <span data-ttu-id="20088-172">Si la cola MAPI es cerrar la sesión y aún tiene los mensajes en la cola, se pasa NOTIFY_ABORT_DEFERRED sólo en _ulFlags_ cuando llama a **TransportNotify**.</span><span class="sxs-lookup"><span data-stu-id="20088-172">If the MAPI spooler is logging off and still has messages in the queue, it passes only NOTIFY_ABORT_DEFERRED in  _ulFlags_ when it calls **TransportNotify**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20088-173">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="20088-173">Notes to implementers</span></span>

<span data-ttu-id="20088-174">El proveedor debe sincronizar el acceso a sus datos en esta llamada, debido a que la cola MAPI puede invocar este método desde otro subproceso de ejecución o desde un procedimiento para una ventana diferente.</span><span class="sxs-lookup"><span data-stu-id="20088-174">The provider must synchronize access to its data on this call, because the MAPI spooler can invoke this method from another thread of execution or from a procedure for a different window.</span></span> <span data-ttu-id="20088-175">Esto es muy probable que se producirá cuando la cola MAPI señala la cancelación de un mensaje que el proveedor de transporte ha empezado a enviar.</span><span class="sxs-lookup"><span data-stu-id="20088-175">This will most likely occur when the MAPI spooler signals the cancellation of a message that the transport provider has started sending.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20088-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="20088-176">See also</span></span>

- [<span data-ttu-id="20088-177">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="20088-177">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md) 
- [<span data-ttu-id="20088-178">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="20088-178">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md) 
- [<span data-ttu-id="20088-179">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="20088-179">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md) 
- [<span data-ttu-id="20088-180">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="20088-180">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md) 
- [<span data-ttu-id="20088-181">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="20088-181">IXPLogon::Poll</span></span>](ixplogon-poll.md)
- [<span data-ttu-id="20088-182">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="20088-182">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
- [<span data-ttu-id="20088-183">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="20088-183">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
- [<span data-ttu-id="20088-184">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="20088-184">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="20088-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20088-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)
