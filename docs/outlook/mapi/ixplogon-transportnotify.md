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
  
Indica la aparición de un evento sobre el que el proveedor de transporte solicitó la notificación.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Máscara de bits de marcas que indica eventos de notificación. La cola MAPI puede establecer las siguientes marcas en la entrada y deben devolverse sin cambios en el resultado:
    
NOTIFY_ABORT_DEFERRED 
  
> Notifica al proveedor de transporte que se aplaza un mensaje del que aceptó la responsabilidad. Solo los proveedores de transporte que admiten el aplazamiento deben admitir esta marca. El  _parámetro lppvData_ apunta al identificador de entrada del mensaje cancelado. Los mensajes que la cola MAPI no ha procesado aún se pueden aplazar llamando al [método IMsgStore::AbortSubmit.](imsgstore-abortsubmit.md) 
    
NOTIFY_BEGIN_INBOUND 
  
> La cola MAPI ahora puede aceptar mensajes entrantes para esta sesión del proveedor de transporte. La cola MAPI llama regularmente al método [IXPLogon::P oll](ixplogon-poll.md) si el proveedor de transporte establece la marca LOGON_SP_POLL con la llamada [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) al iniciar sesión. Una vez NOTIFY_BEGIN_INBOUND marca, la cola MAPI respeta la marca NOTIFY_NEWMAIL pasada en la llamada al método [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) La fila de tabla de estado de la sesión del proveedor de transporte debe actualizarse antes de devolver llamando al [método IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) Las NOTIFY_BEGIN_INBOUND y NOTIFY_END_INBOUND son mutuamente excluyentes. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indica al proveedor de transporte que se desvía por los mensajes entrantes lo antes posible. Para cumplir con esta notificación, el proveedor de transporte debe establecer la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de tabla de estado tan pronto como pueda, mediante **ModifyStatusRow**. Un ciclo de mensajería entrante se completa cuando el proveedor determina que ha descargado todo lo que puede, o cuando ha recibido una llamada al método **TransportNotify** con el NOTIFY_END_INBOUND_FLUSH marca establecida. Hasta el final del ciclo de mensajería entrante, el proveedor no debe llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) ni, de lo contrario, renunciar a los ciclos al sistema operativo para acelerar la entrega de mensajes entrantes. Esto es aceptable porque la cola MAPI normalmente usa NOTIFY_BEGIN_INBOUND_FLUSH solo en respuesta a la solicitud de un usuario, a través de una aplicación cliente, para entregar todos los mensajes ahora. Al final de la operación de vaciado de entrada, el proveedor debe usar **SpoolerNotify** para borrar la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** de su fila de estado. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ahora pueden producirse operaciones salientes para esta sesión del proveedor de transporte. Si hay algún mensaje que enviar para este proveedor, se sigue una llamada al método [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) La fila de la tabla de estado de esta sesión debe actualizarse antes de devolver. Las NOTIFY_BEGIN_OUTBOUND y NOTIFY_END_OUTBOUND son mutuamente excluyentes. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funciona de forma similar a la NOTIFY_BEGIN_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. La marca de estado adecuada es STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> La cola MAPI debe cancelar la transferencia del mensaje para el que el parámetro _lppvData_ apunta al valor de 32 bits de la llamada al método **IXPLogon::SubmitMessage.** La marca NOTIFY_CANCEL_MESSAGE se puede establecer sin que el proveedor de transporte haya devuelto de la llamada al método **SubmitMessage**, **IXPLogon::StartMessage** o **IXPLogon::EndMessage** asociada al mensaje. El proveedor de transporte debe devolver lo antes posible desde el punto de entrada que administra el mensaje cancelado. Para un mensaje entrante que se está procesando actualmente, el proveedor de transporte debe guardar el mensaje entrante siempre que esté almacenado y volver a entregarlo en el siguiente momento conveniente. Se descartan los datos del objeto de mensaje que ya están almacenados para el mensaje entrante. Si el proveedor de transporte no actualizo este valor de 32 bits en el momento **de StartMessage** o **SubmitMessage,** el valor es 0 para los mensajes salientes y 1 para los mensajes entrantes. 
    
NOTIFY_END_INBOUND 
  
> Las operaciones entrantes deben cesar para esta sesión del proveedor de transporte. La cola MAPI deja de usar el **método Poll** y omite NOTIFY_NEWMAIL para esta sesión. Los mensajes en proceso deben completarse. La fila de tabla de estado de la sesión de transporte debe actualizarse llamando a [ModifyStatusRow antes](imapisupport-modifystatusrow.md) de devolver. Las NOTIFY_END_INBOUND y NOTIFY_BEGIN_INBOUND son mutuamente excluyentes. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifica al proveedor de transporte que salga del modo de vaciado entrante. El proveedor de transporte no debe dejar de descargar, pero la descarga debe realizarse en segundo plano. La fila de tabla de estado de la sesión de transporte debe actualizarse llamando a **ModifyStatusRow** cuando el proveedor de transporte pueda cumplir con esta notificación. 
    
NOTIFY_END_OUTBOUND 
  
> Las operaciones salientes deben cesar para esta sesión del proveedor de transporte. La cola MAPI deja de llamar a **SubmitMessage** e omite la **marca de NOTIFY_READYTOSEND SpoolerNotify.** Si hay un mensaje saliente que se envía actualmente, no debe detenerse; para detener la entrega de un mensaje, use NOTIFY_CANCEL_MESSAGE marca. La fila de tabla de estado de esta sesión debe actualizarse llamando a **ModifyStatusRow antes** de devolver. Las NOTIFY_END_INBOUND y NOTIFY_BEGIN_OUTBOUND son mutuamente excluyentes. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funciona de forma similar a NOTIFY_END_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. La marca de estado adecuada es STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [salida] Puntero a un puntero a datos específicos del evento. Para obtener más información acerca de _lo que lppvData_ especifica, vea la descripción del parámetro _lpulFlags._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::TransportNotify** para indicar al proveedor de transporte los eventos para los que se ha solicitado la notificación. Estos eventos incluyen una solicitud de cola MAPI para cancelar una transferencia de mensajes, el principio o el final de las operaciones de transporte entrante o saliente, y el principio o el final de una operación para borrar una cola de mensajes entrantes o salientes. 
  
Cuando el usuario intenta cancelar un mensaje que el proveedor de transporte ha aplazado anteriormente, la cola MAPI llama a **TransportNotify**, pasando las marcas NOTIFY_ABORT_DEFERRED y NOTIFY_CANCEL_MESSAGE en  _ulFlags_. Si la cola MAPI está iniciando sesión y todavía tiene mensajes en la cola, solo pasa NOTIFY_ABORT_DEFERRED en  _ulFlags_ cuando llama a **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El proveedor debe sincronizar el acceso a sus datos en esta llamada, ya que la cola MAPI puede invocar este método desde otro subproceso de ejecución o desde un procedimiento para una ventana diferente. Lo más probable es que esto ocurra cuando la cola MAPI señale la cancelación de un mensaje que el proveedor de transporte ha comenzado a enviar.
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

