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
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428861"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la ocurrencia de un evento sobre el cual el proveedor de transporte solicitó la notificación.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Máscara de máscara de marcadores que indica eventos de notificación. Las marcas siguientes se pueden establecer mediante la cola MAPI en la entrada y deben devolverse sin cambios en la salida:
    
NOTIFY_ABORT_DEFERRED 
  
> Notifica al proveedor de transporte que se ha aplazado un mensaje para el que la responsabilidad que aceptó la responsabilidad. Solo los proveedores de transporte que admiten el aplazamiento deben admitir esta marca. El parámetro _lppvData_ hace referencia al identificador de entrada del mensaje cancelado. Los mensajes que la cola MAPI no ha procesado todavía pueden aplazarse llamando al método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> La cola MAPI ahora puede aceptar mensajes entrantes para esta sesión del proveedor de transporte. La cola MAPI llama de forma regular al método [IXPLogon::P Oll](ixplogon-poll.md) si el proveedor de transporte estableció la marca LOGON_SP_POLL con la llamada [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) al iniciar sesión. Una vez que se establece la marca NOTIFY_BEGIN_INBOUND, la cola MAPI respeta la marca NOTIFY_NEWMAIL que se pasa en la llamada al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . La fila de la tabla de estado de la sesión del proveedor de transporte debe actualizarse antes de volver a llamar al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . Los indicadores NOTIFY_BEGIN_INBOUND y NOTIFY_END_INBOUND se excluyen mutuamente. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indica al proveedor de transporte que recorra los mensajes entrantes lo antes posible. Para cumplir con esta notificación, el proveedor de transporte debe establecer la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de la tabla de estado en cuanto pueda, mediante **ModifyStatusRow**. Un ciclo de mensajería entrante se completa cuando el proveedor ha descargado todo lo que puede o cuando ha recibido una llamada al método **TransportNotify** con el valor de marca NOTIFY_END_INBOUND_FLUSH establecido. Hasta el final del ciclo de mensajería entrante, el proveedor no debe llamar al método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) ni ceder ciclos al sistema operativo para acelerar la entrega de mensajes entrantes. Esto es aceptable porque la cola MAPI suele usar NOTIFY_BEGIN_INBOUND_FLUSH sólo en respuesta a una solicitud del usuario, a través de una aplicación cliente, para entregar todos los mensajes ahora. Al final de la operación de vaciado de entrada, el proveedor debe usar **SpoolerNotify** para borrar la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** de su fila de estado. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Las operaciones de salida ahora pueden producirse para esta sesión del proveedor de transporte. Si hay mensajes que se van a enviar para este proveedor, sigue una llamada al método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . La fila de la tabla de estado de esta sesión debe actualizarse antes de devolverla. Los indicadores NOTIFY_BEGIN_OUTBOUND y NOTIFY_END_OUTBOUND se excluyen mutuamente. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funciona de manera similar a la marca NOTIFY_BEGIN_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. El indicador de estado adecuado es STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> La cola MAPI debe cancelar la transferencia del mensaje para el que el parámetro _lppvData_ señala al valor 32 bits de la llamada al método **IXPLogon:: SubmitMessage** . La marca NOTIFY_CANCEL_MESSAGE se puede establecer sin que el proveedor de transporte se devuelva desde la llamada al método **SubmitMessage**, **IXPLogon:: StartMessage**o **IXPLogon:: EndMessage** asociada con el mensaje. El proveedor de transporte debe volver lo antes posible desde el punto de entrada que controla el mensaje cancelado. Para un mensaje entrante que se está procesando actualmente, el proveedor de transporte debe guardar el mensaje entrante en cualquier lugar en el que se almacene y entregarlo de nuevo en el siguiente momento conveniente. Se descartan los datos de objeto de mensaje que ya están almacenados para el mensaje entrante. Si el proveedor de transporte no actualiza este valor de 32 bits en el tiempo **StartMessage** o **SubmitMessage** , el valor es 0 para los mensajes salientes y 1 para los mensajes entrantes. 
    
NOTIFY_END_INBOUND 
  
> Las operaciones de entrada deben cesar en esta sesión de proveedor de transporte. La cola de MAPI deja de usar el método **** de sondeo y pasa por alto NOTIFY_NEWMAIL para esta sesión. Los mensajes en curso deben completarse. La fila de la tabla de estado de la sesión de transporte debe actualizarse mediante una llamada a [ModifyStatusRow](imapisupport-modifystatusrow.md) antes de devolverse. Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_INBOUND se excluyen mutuamente. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifica al proveedor de transporte salir del modo de vaciado de entrada. El proveedor de transporte no debe dejar de descargar, pero la descarga debe realizarse en segundo plano. La fila de la tabla de estado de la sesión de transporte debe actualizarse mediante una llamada a **ModifyStatusRow** cuando el proveedor de transporte puede cumplir con esta notificación. 
    
NOTIFY_END_OUTBOUND 
  
> Las operaciones de salida deben cesar en esta sesión de proveedor de transporte. La cola de MAPI deja de llamar a **SubmitMessage** e ignora la marca de NOTIFY_READYTOSEND **SpoolerNotify** . Si hay un mensaje saliente que se está enviando actualmente, no se debe detener; para detener la entrega de un mensaje, use la marca NOTIFY_CANCEL_MESSAGE. La fila de tabla de estado para esta sesión debe actualizarse mediante una llamada a **ModifyStatusRow** antes de devolverse. Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_OUTBOUND se excluyen mutuamente. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funciona de manera similar a NOTIFY_END_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. El indicador de estado adecuado es STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> contempla Un puntero a un puntero a datos específicos del evento. Para obtener más información sobre qué especifica _lppvData_ , vea la descripción del parámetro _lpulFlags_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon:: TransportNotify** para indicar al proveedor de transporte los eventos para los que se solicitó notificación. Estos eventos incluyen una solicitud de cola MAPI para cancelar una transferencia de mensajes, el principio o el final de operaciones de transporte de entrada o salida, y el principio o el final de una operación para borrar una cola de mensajes entrantes o salientes. 
  
Cuando el usuario intenta cancelar un mensaje que el proveedor de transporte ha aplazado anteriormente, la cola MAPI llama a **TransportNotify**, pasando los indicadores NOTIFY_ABORT_DEFERRED y NOTIFY_CANCEL_MESSAGE en _ulFlags_. Si la cola MAPI está cerrando la sesión y todavía tiene mensajes en la cola, sólo pasa NOTIFY_ABORT_DEFERRED en _ulFlags_ cuando llama a **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El proveedor debe sincronizar el acceso a sus datos en esta llamada, ya que la cola MAPI puede invocar este método desde otro subproceso de ejecución o desde un procedimiento para una ventana distinta. Esto probablemente ocurrirá cuando la cola MAPI señale la cancelación de un mensaje que el proveedor de transporte ha empezado a enviar.
  
## <a name="see-also"></a>Ver también

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

