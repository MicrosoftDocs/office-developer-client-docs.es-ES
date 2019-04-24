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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351600"
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpMessage_
  
> a Un puntero a un objeto de mensaje (que representa el mensaje entrante) que tiene el permiso de lectura y escritura, que el proveedor de transporte usa para tener acceso al mensaje y manipularlo. Este objeto sigue siendo válido hasta después de que el proveedor de transporte vuelva de la llamada a **IXPLogon:: StartMessage**.
    
 _lpulMsgRef_
  
> contempla Un puntero a un valor de referencia asignado al mensaje. La cola MAPI inicializa este valor en 1 antes de devolver el puntero al proveedor de transporte.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon:: StartMessage** para iniciar la transferencia de un mensaje entrante del proveedor de transporte a la cola MAPI. Antes de que el proveedor de transporte empiece a usar el mensaje al que señala _lpMessage_, debe almacenar una referencia de mensaje en el parámetro _lpulMsgRef_ para uso potencial mediante una llamada al método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) . 
  
Durante una llamada de **StartMessage** , el administrador de trabajos en cola MAPI procesa los métodos de los objetos abiertos durante la transferencia del mensaje y también procesa los datos adjuntos. Este proceso puede tardar mucho tiempo. Los proveedores de transporte pueden llamar a la función de devolución de llamada [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este procesamiento para liberar tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios de la tabla de destinatarios que el proveedor de transporte crea para el mensaje deben contener todas las propiedades de dirección necesarias. Si es necesario, el proveedor puede construir un destinatario personalizado para representar a un destinatario en particular. Sin embargo, si el proveedor puede producir una entrada de destinatario que incluya más información, debe hacerlo. Por ejemplo, si un proveedor de transporte tiene suficiente información sobre el formato de los destinatarios de un proveedor de libreta de direcciones que puede crear un identificador de entrada válido para un destinatario con ese formato, debe crear el identificador de entrada.
  
Si se reciben propiedades no transmitibles, el proveedor de transporte no debe almacenarlas en el nuevo mensaje. Sin embargo, el proveedor de transporte debe almacenar todas las propiedades transmitibles que recibe en el nuevo mensaje.
  
Si el mensaje entrante es un informe de entrega o un informe de no entrega y el proveedor de transporte no puede usar el método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para generar el informe del mensaje original, el proveedor debe rellenar el mensaje con las propiedades adecuadas. Sin embargo, el proveedor de transporte no puede establecer **** la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)del mensaje.
  
Para guardar el mensaje entrante en el almacén de mensajes MAPI correspondiente después de su procesamiento, el proveedor de transporte llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Si el proveedor de transporte no tiene ningún mensaje que pasar a la cola MAPI, puede detener el mensaje entrante volviendo de la llamada **StartMessage** sin llamar a **SaveChanges**.
  
Todos los objetos que el proveedor de transporte abre durante una llamada de **StartMessage** debe liberarse antes de devolverse. Sin embargo, el proveedor no debería liberar el objeto de mensaje que la cola MAPI pasó originalmente en el parámetro _lpMessage_ . 
  
Si **StartMessage** devuelve un error, el mensaje en proceso se suelta sin tener cambios guardados y perdidos. En este caso, el proveedor de transporte debe pasar la marca NOTIFY_CRITICAL_ERROR con una llamada al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) y llamar al método [IXPLogon::P Oll](ixplogon-poll.md) para notificar a la cola MAPI que se encuentra en una condición de error grave. 
  
Para obtener más información, consulte [interactuar con la cola MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

