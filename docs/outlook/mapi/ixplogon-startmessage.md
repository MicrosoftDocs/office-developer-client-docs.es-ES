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
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427608"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia la transferencia de un mensaje entrante del proveedor de transporte a la cola MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpMessage_
  
> [entrada] Puntero a un objeto de mensaje (que representa el mensaje entrante) que tiene permiso de lectura y escritura, que usa el proveedor de transporte para tener acceso a ese mensaje y manipularlo. Este objeto permanece válido hasta que el proveedor de transporte vuelve de la llamada a **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [salida] Puntero a un valor de referencia asignado al mensaje. La cola MAPI inicializa este valor en 1 antes de devolver el puntero al proveedor de transporte.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::StartMessage** para iniciar la transferencia de un mensaje entrante del proveedor de transporte a la cola MAPI. Antes de que el proveedor de transporte empiece a usar el mensaje al que apunta _lpMessage_, debe almacenar una referencia de mensaje en el parámetro _lpulMsgRef_ para que pueda usarla una llamada al método [IXPLogon::TransportNotify.](ixplogon-transportnotify.md) 
  
Durante una **llamada StartMessage,** la cola MAPI procesa métodos para objetos abiertos durante la transferencia del mensaje y también procesa los datos adjuntos. Este procesamiento puede tardar mucho tiempo. Los proveedores de transporte pueden llamar a la función de devolución de llamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este procesamiento para liberar tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios de la tabla de destinatarios que crea el proveedor de transporte para el mensaje deben contener todas las propiedades de direccionamiento necesarias. Si es necesario, el proveedor puede crear un destinatario personalizado para representar a un destinatario determinado. Sin embargo, si el proveedor puede producir una entrada de destinatario que incluya más información, debe hacerlo. Por ejemplo, si un proveedor de transporte tiene información suficiente sobre el formato de destinatario de un proveedor de libreta de direcciones que puede crear un identificador de entrada válido para un destinatario para ese formato, debe crear el identificador de entrada.
  
Si se recibe alguna propiedad notransmitible, el proveedor de transporte no debe almacenarlas en el nuevo mensaje. Sin embargo, el proveedor de transporte debe almacenar todas las propiedades transmitibles que recibe en el nuevo mensaje.
  
Si el mensaje entrante es un informe de entrega o un informe de no entrega y el proveedor de transporte no puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para generar el informe a partir del mensaje original, el propio proveedor debe rellenar el mensaje con las propiedades adecuadas. Sin embargo, el proveedor de transporte no puede establecer la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del mensaje.
  
Para guardar el mensaje entrante en el almacén de mensajes MAPI adecuado después de su procesamiento, el proveedor de transporte llama al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Si el proveedor de transporte no tiene ningún mensaje para pasar a la cola MAPI, puede detener el mensaje entrante devolviendo desde la llamada **StartMessage** sin llamar a **SaveChanges**.
  
Todos los objetos que abre el proveedor de transporte durante una **llamada StartMessage** deben liberarse antes de volver. Sin embargo, el proveedor no debe liberar el objeto de mensaje que la cola MAPI pasó originalmente en el _parámetro lpMessage._ 
  
Si **StartMessage** devuelve un error, el mensaje en proceso se libera sin tener cambios guardados y se pierde. En este caso, el proveedor de transporte debe pasar la marca NOTIFY_CRITICAL_ERROR con una llamada al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) y llamar al método [IXPLogon::P oll](ixplogon-poll.md) para notificar a la cola MAPI que se encuentra en una condición de error grave. 
  
Para obtener más información, vea [Interactuar con la cola MAPI.](interacting-with-the-mapi-spooler.md) 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

