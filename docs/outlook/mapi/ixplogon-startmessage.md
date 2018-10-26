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
ms.openlocfilehash: d9235da7e7ec6ec244ee1a75f4795e9c77ec28bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579952"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Inicia a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpMessage_
  
> [entrada] Un puntero a un objeto de mensaje (que representa el mensaje entrante) que tiene el permiso de lectura y escritura, que se usa el proveedor de transporte para obtener acceso y gestionar ese mensaje. Este objeto sigue siendo válida hasta después de que devuelve el proveedor de transporte de la llamada a **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Un puntero a un valor de referencia asignado al mensaje. La cola MAPI inicializa en este valor en 1 antes de devolver el puntero para el proveedor de transporte.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::StartMessage** para iniciar a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI. Antes de que el proveedor de transporte comienza a usar el mensaje que apunta _lpMessage_, debería almacenar una referencia de mensaje en el parámetro _lpulMsgRef_ para su uso posible mediante una llamada al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) . 
  
Durante una llamada **desea iniciar** , la cola MAPI procesa los métodos de objetos abiertos durante la transferencia del mensaje, y también procesa los datos adjuntos. Este proceso puede tardar mucho tiempo. Los proveedores de transporte pueden llamar a la función de devolución de llamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este proceso para liberar el tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios en la tabla de destinatarios que crea el proveedor de transporte para el mensaje deben contener todas las propiedades de direccionamiento necesarias. Si es necesario, el proveedor puede construir un destinatario personalizado para representar a un destinatario concreto. Sin embargo, si el proveedor puede producir una entrada del destinatario que incluye más información, deberá hacerlo. Por ejemplo, si un proveedor de transporte tiene suficiente información sobre el formato de un proveedor de la libreta de direcciones de destinatarios que puede crear un identificador de entrada válido para un destinatario para dicho formato, debe crear el identificador de entrada.
  
Si se reciben las propiedades nontransmittable, el proveedor de transporte no debe almacenarlos en el nuevo mensaje. Sin embargo, el proveedor de transporte debe almacenar todas las propiedades transmisible recibe en el mensaje de nuevo.
  
Si el mensaje entrante es un informe de entrega o un informe de no entrega y el proveedor de transporte es no se puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para generar el informe desde el mensaje original, el proveedor debe rellenar el mensaje con en Sí las propiedades adecuadas. Sin embargo, el proveedor de transporte no puede establecer la propiedad del mensaje de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Para guardar el mensaje entrante en el almacén de mensajes MAPI adecuado tras el procesamiento, el proveedor de transporte llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Si el proveedor de transporte no tiene todos los mensajes que se pase a la cola de MAPI, puede detener el mensaje entrante mediante la devolución de la llamada **desea iniciar** sin llamar a **SaveChanges**.
  
Todos los objetos que se abre el proveedor de transporte durante una llamada **desea iniciar** deben liberarse antes de devolverlo. No obstante, el proveedor debe liberar el objeto de mensaje que la cola MAPI originalmente se pasa en el parámetro _lpMessage_ . 
  
Si **desea iniciar** devuelve un error, el mensaje en el proceso se libera sin necesidad de cambios guardados y se pierde. En este caso, el proveedor de transporte debe pasar el indicador NOTIFY_CRITICAL_ERROR con una llamada al método [SpoolerNotify](imapisupport-spoolernotify.md) y llame al método [IXPLogon::Poll](ixplogon-poll.md) para notificar a la cola MAPI que se encuentra en una condición de error grave. 
  
Para obtener más información, consulte [interactuar con la cola de MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

