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
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que la cola MAPI tiene un mensaje para que lo entregue el proveedor de transporte.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se envía el mensaje. Se puede establecer la siguiente marca:
    
BEGIN_DEFERRED 
  
> La cola MAPI llama a un proveedor de transporte con un mensaje previamente aplazado. El identificador de entrada del mensaje es el mismo que cuando se aplazó. El mensaje se ha aplazado pasando su identificador de entrada de vuelta a la cola MAPI mediante el método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> a Un puntero a un objeto de mensaje (que representa el mensaje que se va a entregar) que tiene permiso de lectura y escritura, que el proveedor de transporte usa para tener acceso y manipular el mensaje. Este objeto sigue siendo válido hasta después de que el proveedor de transporte vuelva de una llamada posterior al método [IXPLogon:: EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> contempla Un puntero a una variable en la que el proveedor de transporte devuelve el valor de referencia asignado a este mensaje. La cola MAPI pasa este valor de referencia en llamadas posteriores para este mensaje. La cola MAPI inicializa el valor en 0 antes de devolverlo al proveedor de transporte.
    
 _lpulReturnParm_
  
> contempla Un puntero a una variable que corresponde al valor de error MAPI_E_WAIT o MAPI_E_NETWORK_ERROR devuelto por **SubmitMessage**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_BUSY 
  
> El proveedor de transporte no puede controlar el mensaje porque está realizando otra operación. Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar a **EndMessage**. La cola de impresión MAPI volverá a intentar la llamada de **SubmitMessage** más adelante. 
    
MAPI_E_CANCEL 
  
> Aunque el proveedor de transporte solicitó que la cola MAPI reenviara el mensaje en una llamada de **SpoolerNotify** anterior, las condiciones se cambiaban desde entonces y no se debía reenviar el mensaje. La cola de impresión MAPI continuará para controlar otras acciones. 
    
MAPI_E_NETWORK_ERROR 
  
> Un error de red impidió la finalización correcta de la operación. El parámetro _lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI reenvíe el mensaje. 
    
MAPI_E_NOT_ME 
  
> El proveedor de transporte no puede controlar este mensaje. La cola MAPI debe intentar encontrar otro proveedor de transporte. Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar a **EndMessage**.
    
MAPI_E_WAIT 
  
> Un problema temporal impide que el proveedor de transporte controle el mensaje. El parámetro _lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI reenvíe el mensaje. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon:: SubmitMessage** cuando tiene un mensaje para que el proveedor de transporte lo entregue. El mensaje se pasa al proveedor de transporte mediante el parámetro _lpMessage_ . 
  
Si el proveedor está listo para aceptar el mensaje, debe devolver un valor de referencia mediante el parámetro _lpulMsgRef_ , procesar el objeto que se ha pasado y devolver el valor apropiado (normalmente S_OK). Si el proveedor no está preparado para controlar la transferencia, debe devolver un valor de error y, opcionalmente, otro valor devuelto por MAPI en _lpulReturnParm_ para indicar cuánto tiempo debe esperar la cola MAPI antes de volver a enviar el mensaje. 
  
La implementación de este método de un proveedor de transporte puede hacer lo siguiente:
  
- Poner el mensaje en una cola interna para esperar la transmisión, posiblemente copiar el mensaje al almacenamiento local y volver.
    
- Intente realizar la transmisión y devolución reales cuando se complete la transmisión, ya sea correctamente o sin éxito.
    
- DeTermine si desea enviar el mensaje después de comprobar el recurso implicado. En este caso, si el recurso es gratuito, el proveedor puede bloquear el recurso, preparar el mensaje y enviarlo. Si el recurso está ocupado, el proveedor puede preparar el mensaje y postergar el envío a un momento posterior.
    
La técnica preferida para la transmisión de mensajes depende del proveedor de transporte y del número previsto de procesos que compiten por los recursos del sistema. 
  
Durante una llamada de **SubmitMessage** , el proveedor de transporte controla la transferencia de datos del mensaje desde el objeto de mensaje. Sin embargo, el proveedor de transporte debe asignar un valor de referencia al mensaje, al que devuelve un puntero en _lpulMsgRef_, antes de transferir datos. Esto se debe a que, en cualquier momento durante el proceso, la cola MAPI puede llamar al método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) con la marca NOTIFY_CANCEL_MESSAGE establecida para indicar al proveedor que debe liberar todos los objetos abiertos y detener la transferencia de mensajes. 
  
El proveedor de transporte no debe enviar ninguna propiedad no transmitible del mensaje. Cuando encuentra una propiedad de este tipo, debe continuar para procesar la siguiente propiedad. El proveedor debe hacer todo lo posible para no mostrar la información del destinatario de MAPI_P1 como parte del contenido del mensaje transmitido; el proveedor debe usar esta información de destinatarios solo para propósitos de dirección. MAPI_P1 los destinatarios son destinatarios generados internamente que se usan para reenviar mensajes; no deben transmitirse. En su lugar, use los otros destinatarios para transmitir la información del destinatario. El propósito de esta disposición es permitir a los destinatarios reenviar para ver exactamente la misma tabla de destinatarios que los destinatarios originales.
  
Durante una llamada de **SubmitMessage** , el administrador de trabajos en cola MAPI procesa los métodos de los objetos que se abren durante la transferencia del mensaje y procesa los datos adjuntos. Este proceso puede tardar mucho tiempo. Los proveedores de transporte pueden llamar al método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este procesamiento para liberar tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios del mensaje están visibles en la tabla de destinatarios del mensaje que la cola MAPI pasó originalmente. El proveedor de transporte debe procesar solo los destinatarios que puede administrar (según el identificador de entrada, el tipo de dirección o ambos) y que todavía no tienen su propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en true. Si **PR_RESPONSIBILITY** ya está establecido en true, otro proveedor de transporte ha controlado a ese destinatario. Cuando el proveedor completa el procesamiento suficiente de un destinatario para determinar si puede procesar mensajes para ese destinatario, debe establecer la propiedad **PR_RESPONSIBILITY** del destinatario en true en el mensaje pasado. Normalmente, el proveedor realiza esta determinación una vez finalizada la entrega del mensaje. 
  
Normalmente, el proveedor de transporte no vuelve de una llamada **SubmitMessage** hasta completar la transferencia de datos del mensaje. Si no se devuelve ningún error, la siguiente llamada de la cola MAPI al proveedor es una llamada al método [IXPLogon:: EndMessage](ixplogon-endmessage.md) . 
  
Si **SubmitMessage** devuelve un error, la cola MAPI libera el mensaje en proceso sin guardar los cambios. Si el proveedor de transporte requiere que se guarden los cambios de los mensajes, debe llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en el mensaje antes de devolverlo. 
  
En caso de que se produzcan errores debidos a problemas de transporte, la cola MAPI conserva el mensaje, pero retrasa el reenvío del mensaje al proveedor de transporte según el valor devuelto en _lpulReturnParm_. El proveedor de transporte debe rellenar ese valor si su valor devuelto de **SubmitMessage** es MAPI_E_WAIT o MAPI_E_NETWORK_ERROR. Si se produce una condición de error grave, el proveedor de transporte debe llamar al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Ver también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

