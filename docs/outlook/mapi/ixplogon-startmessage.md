---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818017"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="be40f-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="be40f-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="be40f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be40f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be40f-105">Inicia a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="be40f-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="be40f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="be40f-106">Parameters</span></span>

 <span data-ttu-id="be40f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be40f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="be40f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="be40f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="be40f-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="be40f-109">_lpMessage_</span></span>
  
> <span data-ttu-id="be40f-110">[entrada] Un puntero a un objeto de mensaje (que representa el mensaje entrante) que tiene el permiso de lectura y escritura, que se usa el proveedor de transporte para obtener acceso y gestionar ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="be40f-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="be40f-111">Este objeto sigue siendo válida hasta después de que devuelve el proveedor de transporte de la llamada a **IXPLogon::StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="be40f-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="be40f-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="be40f-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="be40f-113">[out] Un puntero a un valor de referencia asignado al mensaje.</span><span class="sxs-lookup"><span data-stu-id="be40f-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="be40f-114">La cola MAPI inicializa en este valor en 1 antes de devolver el puntero para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="be40f-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be40f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be40f-115">Return value</span></span>

<span data-ttu-id="be40f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="be40f-116">S_OK</span></span> 
  
> <span data-ttu-id="be40f-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="be40f-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be40f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be40f-118">Remarks</span></span>

<span data-ttu-id="be40f-119">La cola MAPI llama al método de **IXPLogon::StartMessage** para iniciar a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="be40f-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="be40f-120">Antes de que el proveedor de transporte comienza a usar el mensaje que apunta _lpMessage_, debería almacenar una referencia de mensaje en el parámetro _lpulMsgRef_ para su uso posible mediante una llamada al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="be40f-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="be40f-121">Durante una llamada **desea iniciar** , la cola MAPI procesa los métodos de objetos abiertos durante la transferencia del mensaje, y también procesa los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="be40f-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="be40f-122">Este proceso puede tardar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="be40f-122">This processing can take a long time.</span></span> <span data-ttu-id="be40f-123">Los proveedores de transporte pueden llamar a la función de devolución de llamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este proceso para liberar el tiempo de CPU para otras tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="be40f-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="be40f-124">Todos los destinatarios en la tabla de destinatarios que crea el proveedor de transporte para el mensaje deben contener todas las propiedades de direccionamiento necesarias.</span><span class="sxs-lookup"><span data-stu-id="be40f-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="be40f-125">Si es necesario, el proveedor puede construir un destinatario personalizado para representar a un destinatario concreto.</span><span class="sxs-lookup"><span data-stu-id="be40f-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="be40f-126">Sin embargo, si el proveedor puede producir una entrada del destinatario que incluye más información, deberá hacerlo.</span><span class="sxs-lookup"><span data-stu-id="be40f-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="be40f-127">Por ejemplo, si un proveedor de transporte tiene suficiente información sobre el formato de un proveedor de la libreta de direcciones de destinatarios que puede crear un identificador de entrada válido para un destinatario para dicho formato, debe crear el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="be40f-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="be40f-128">Si se reciben las propiedades nontransmittable, el proveedor de transporte no debe almacenarlos en el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="be40f-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="be40f-129">Sin embargo, el proveedor de transporte debe almacenar todas las propiedades transmisible recibe en el mensaje de nuevo.</span><span class="sxs-lookup"><span data-stu-id="be40f-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="be40f-130">Si el mensaje entrante es un informe de entrega o un informe de no entrega y el proveedor de transporte es no se puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para generar el informe desde el mensaje original, el proveedor debe rellenar el mensaje con en Sí las propiedades adecuadas.</span><span class="sxs-lookup"><span data-stu-id="be40f-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="be40f-131">Sin embargo, el proveedor de transporte no puede establecer la propiedad del mensaje de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="be40f-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="be40f-132">Para guardar el mensaje entrante en el almacén de mensajes MAPI adecuado tras el procesamiento, el proveedor de transporte llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="be40f-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="be40f-133">Si el proveedor de transporte no tiene todos los mensajes que se pase a la cola de MAPI, puede detener el mensaje entrante mediante la devolución de la llamada **desea iniciar** sin llamar a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="be40f-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="be40f-134">Todos los objetos que se abre el proveedor de transporte durante una llamada **desea iniciar** deben liberarse antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="be40f-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="be40f-135">No obstante, el proveedor debe liberar el objeto de mensaje que la cola MAPI originalmente se pasa en el parámetro _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="be40f-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="be40f-136">Si **desea iniciar** devuelve un error, el mensaje en el proceso se libera sin necesidad de cambios guardados y se pierde.</span><span class="sxs-lookup"><span data-stu-id="be40f-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="be40f-137">En este caso, el proveedor de transporte debe pasar el indicador NOTIFY_CRITICAL_ERROR con una llamada al método [SpoolerNotify](imapisupport-spoolernotify.md) y llame al método [IXPLogon::Poll](ixplogon-poll.md) para notificar a la cola MAPI que se encuentra en una condición de error grave.</span><span class="sxs-lookup"><span data-stu-id="be40f-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="be40f-138">Para obtener más información, consulte [interactuar con la cola de MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="be40f-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be40f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="be40f-139">See also</span></span>



[<span data-ttu-id="be40f-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="be40f-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="be40f-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="be40f-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="be40f-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="be40f-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="be40f-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="be40f-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="be40f-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="be40f-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="be40f-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="be40f-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="be40f-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="be40f-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="be40f-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be40f-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

