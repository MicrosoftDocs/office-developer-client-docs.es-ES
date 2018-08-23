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
ms.openlocfilehash: f0c5cd70595ea43a0957e764150ee4d5153e32c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589689"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la aparición de un evento sobre el que el proveedor de transporte solicita la notificación.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada, salida] Una máscara de bits de marcadores que indica los eventos de notificación. Las siguientes marcas se pueden establecer mediante la cola MAPI en la entrada y deben devolverse sin cambios en la salida:
    
NOTIFY_ABORT_DEFERRED 
  
> Notifica al proveedor de transporte que se ha aplazado un mensaje para el que acepta responsabilidad. Sólo los proveedores de transporte que admiten aplazamiento deben admitir esta marca. El parámetro _lppvData_ apunta el identificador de entrada del mensaje cancelado. Los mensajes que no haya procesado la cola MAPI aún se pueden aplazar llamando al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> La cola MAPI ahora puede aceptar mensajes entrantes para esta sesión de proveedor de transporte. La cola MAPI con regularidad llama al método de [IXPLogon::Poll](ixplogon-poll.md) si el proveedor de transporte establece la marca LOGON_SP_POLL con la llamada a [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) al iniciar sesión. Una vez que se establece la marca NOTIFY_BEGIN_INBOUND, la cola MAPI respeta la marca NOTIFY_NEWMAIL que se pasan en la llamada al método [SpoolerNotify](imapisupport-spoolernotify.md) . La fila de la tabla de estado de la sesión de proveedor de transporte debe actualizarse antes de devolverlo al llamar al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Los indicadores NOTIFY_BEGIN_INBOUND y NOTIFY_END_INBOUND son mutuamente excluyentes. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indica el proveedor de transporte para recorrer los mensajes entrantes lo más rápido posible. Para cumplir con esta notificación, el proveedor de transporte debe establecer la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de la tabla de estado tan pronto como puede, mediante el uso de **ModifyStatusRow**. Un ciclo de mensajería entrante finalizada cuando el proveedor determina que ha descargado todo que lo posible o cuando ha recibido una llamada al método **TransportNotify** con el conjunto de marca NOTIFY_END_INBOUND_FLUSH. Hasta el final del ciclo de mensajería entrante, el proveedor no debe llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) o en caso contrario, ceder ciclos en el sistema operativo a la entrega de velocidad de los mensajes entrantes. Esto es aceptable porque la cola MAPI utiliza normalmente NOTIFY_BEGIN_INBOUND_FLUSH sólo en respuesta a una solicitud de un usuario, a través de una aplicación cliente, para entregar todos los mensajes ahora. Al final de la operación de vaciado entrante, el proveedor debe usar **SpoolerNotify** para borrar la marca STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** de la fila de estado correspondiente. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ahora pueden producirse las operaciones de salida para esta sesión de proveedor de transporte. Si existen todos los mensajes que se envíen para este proveedor, sigue una llamada al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . La fila de la tabla de estado para esta sesión debe actualizarse antes de devolverlo. Los indicadores NOTIFY_BEGIN_OUTBOUND y NOTIFY_END_OUTBOUND son mutuamente excluyentes. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funciona de manera similar a la marca NOTIFY_BEGIN_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. El indicador de estado correspondiente es STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> La cola MAPI debe cancelar la transferencia del mensaje para el que llame los puntos de parámetro _lppvData_ en el valor de 32 bits desde el método **IXPLogon::SubmitMessage** . Sin el proveedor de transporte que ha devuelto desde el **SubmitMessage**, **IXPLogon::StartMessage**o llamada al método **IXPLogon::EndMessage** que está asociada con el mensaje, se puede establecer la marca NOTIFY_CANCEL_MESSAGE. El proveedor de transporte debe devolver tan pronto como sea posible desde el punto de entrada que se encarga del mensaje cancelado. Para un mensaje entrante que se está procesando actualmente, el proveedor de transporte debe guardar el mensaje entrante dondequiera que actualmente se encuentra almacenada y entregar nuevo a la siguiente hora conveniente. Se descartan los datos del objeto de mensaje ya almacenados para el mensaje entrante. Si el proveedor de transporte no se actualizó este valor de 32 bits en el momento **desea iniciar** o **SubmitMessage** , el valor es 0 para los mensajes salientes y 1 para los mensajes entrantes. 
    
NOTIFY_END_INBOUND 
  
> Deben dejar de las operaciones de entrada para esta sesión de proveedor de transporte. La cola MAPI se deja de utilizar el método de **sondeo** y omite NOTIFY_NEWMAIL para esta sesión. Deben realizarse en procesar los mensajes. La fila de la tabla de estado de la sesión de transporte debe actualizarse mediante una llamada a [ModifyStatusRow](imapisupport-modifystatusrow.md) antes de devolverlo. Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_INBOUND son mutuamente excluyentes. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifica al proveedor de transporte para salir de modo de vaciado entrante. El proveedor de transporte debe detener la descarga, pero descarga debe realizarse en segundo plano. La fila de la tabla de estado de la sesión de transporte debe actualizarse al llamar a **ModifyStatusRow** cuando el proveedor de transporte puede cumplir con esta notificación. 
    
NOTIFY_END_OUTBOUND 
  
> Deben dejar de operaciones de salida para esta sesión de proveedor de transporte. La cola MAPI deja de llamar a **SubmitMessage** y pasa por alto la marca NOTIFY_READYTOSEND **SpoolerNotify** . Si hay un mensaje de salida que se está enviando actualmente, no debe detener; Para detener la entrega de un mensaje, use la marca NOTIFY_CANCEL_MESSAGE. La fila de la tabla de estado para esta sesión debe actualizarse mediante una llamada a **ModifyStatusRow** antes de devolverlo. Los indicadores NOTIFY_END_INBOUND y NOTIFY_BEGIN_OUTBOUND son mutuamente excluyentes. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funciona de forma similar a NOTIFY_END_INBOUND_FLUSH, pero hace referencia a los mensajes salientes. El indicador de estado correspondiente es STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Un puntero a un puntero a datos específicos del evento. Para obtener más información acerca de qué _lppvData_ especifica, vea la descripción para el parámetro _lpulFlags_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::TransportNotify** para indicar el proveedor de transporte acerca de los eventos para el que se ha solicitado la notificación. Estos eventos incluyen una solicitud de cola de impresión MAPI para cancelar la transferencia de un mensaje, el principio o final de las operaciones de transporte de entrada y salida y principio o al final de una operación para borrar una cola de mensajes entrantes o salientes. 
  
Cuando el usuario intenta cancelar un mensaje que el proveedor de transporte ha aplazado anteriormente, la cola MAPI llama a **TransportNotify**, pasando el NOTIFY_ABORT_DEFERRED y la NOTIFY_CANCEL_MESSAGE marcas en _ulFlags_. Si la cola MAPI es cerrar la sesión y aún tiene los mensajes en la cola, se pasa NOTIFY_ABORT_DEFERRED sólo en _ulFlags_ cuando llama a **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

El proveedor debe sincronizar el acceso a sus datos en esta llamada, debido a que la cola MAPI puede invocar este método desde otro subproceso de ejecución o desde un procedimiento para una ventana diferente. Esto es muy probable que se producirá cuando la cola MAPI señala la cancelación de un mensaje que el proveedor de transporte ha empezado a enviar.
  
## <a name="see-also"></a>Recursos adicionales

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

