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
  
Indica que la cola MAPI tiene un mensaje para que el proveedor de transporte entregue.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se envía el mensaje. Se puede establecer la siguiente marca:
    
BEGIN_DEFERRED 
  
> La cola MAPI llama a un proveedor de transporte con un mensaje que se aplazó anteriormente. El identificador de entrada del mensaje es el mismo que cuando se aplazó. El mensaje se aplazó pasando su identificador de entrada de nuevo a la cola MAPI mediante el método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_SENTDEFERRED entrada. 
    
 _lpMessage_
  
> [entrada] Puntero a un objeto de mensaje (que representa el mensaje que se va a entregar) que tiene permiso de lectura y escritura, que el proveedor de transporte usa para obtener acceso a ese mensaje y manipularlo. Este objeto permanece válido hasta que el proveedor de transporte vuelve de una llamada posterior al método [IXPLogon::EndMessage.](ixplogon-endmessage.md) 
    
 _lpulMsgRef_
  
> [salida] Puntero a una variable en la que el proveedor de transporte devuelve el valor de referencia asignado a este mensaje. La cola MAPI pasa este valor de referencia en llamadas posteriores para este mensaje. La cola MAPI inicializa el valor en 0 antes de devolverlo al proveedor de transporte.
    
 _lpulReturnParm_
  
> [salida] Puntero a una variable que corresponde al valor MAPI_E_WAIT o MAPI_E_NETWORK_ERROR error devuelto por **SubmitMessage**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_BUSY 
  
> El proveedor de transporte no puede controlar el mensaje porque está realizando otra operación. Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar **a EndMessage**. La cola MAPI volverá a intentar la llamada **SubmitMessage** más adelante. 
    
MAPI_E_CANCEL 
  
> Aunque el proveedor de transporte solicitó que la cola MAPI vuelva a enviar el mensaje en una llamada **SpoolerNotify** anterior, las condiciones han cambiado desde entonces y el mensaje no debe reenviarse. La cola MAPI pasará a controlar otra cosa. 
    
MAPI_E_NETWORK_ERROR 
  
> Un error de red impidió que la operación se completara correctamente. El  _parámetro lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI vuelva a enviar el mensaje. 
    
MAPI_E_NOT_ME 
  
> El proveedor de transporte no puede controlar este mensaje. La cola MAPI debe intentar encontrar otro proveedor de transporte para él. Un proveedor debe usar este valor devuelto para indicar que no se ha producido ningún procesamiento y que la cola MAPI no debe llamar **a EndMessage**.
    
MAPI_E_WAIT 
  
> Un problema temporal impide que el proveedor de transporte controle el mensaje. El  _parámetro lpulReturnParm_ debe establecerse en el número de segundos que transcurrirán antes de que la cola MAPI vuelva a enviar el mensaje. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::SubmitMessage** cuando tiene un mensaje para que el proveedor de transporte entregue. El mensaje se pasa al proveedor de transporte mediante el parámetro _lpMessage._ 
  
Si el proveedor está listo para aceptar el mensaje, debe devolver un valor de referencia mediante el parámetro  _lpulMsgRef,_ procesar el objeto pasado y devolver el valor apropiado (normalmente S_OK). Si el proveedor no está preparado para controlar la transferencia, debe devolver un valor de error y, opcionalmente, otro valor devuelto de MAPI en  _lpulReturnParm_ para indicar cuánto tiempo debe esperar la cola MAPI antes de volver a enviar el mensaje. 
  
La implementación de este método por parte de un proveedor de transporte puede hacer lo siguiente:
  
- Coloque el mensaje en una cola interna para esperar la transmisión, posiblemente copiando el mensaje en el almacenamiento local y devolviendo.
    
- Intente realizar la transmisión real y volver cuando la transmisión finalice, ya sea correcta o incorrectamente.
    
- Determinar si se va a enviar el mensaje después de comprobar el recurso implicado. En este caso, si el recurso es gratuito, el proveedor puede bloquear el recurso, preparar el mensaje y enviarlo. Si el recurso está ocupado, el proveedor puede preparar el mensaje y aplazar el envío más adelante.
    
La técnica preferida para la transmisión de mensajes depende del proveedor de transporte y del número esperado de procesos que compiten por los recursos del sistema. 
  
Durante una **llamada SubmitMessage,** el proveedor de transporte controla la transferencia de datos del mensaje desde el objeto de mensaje. Sin embargo, el proveedor de transporte debe asignar un valor de referencia al mensaje, al que devuelve un puntero en  _lpulMsgRef_, antes de transferir datos. Lo hace porque, en cualquier momento durante el proceso, la cola MAPI puede llamar al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) con la marca NOTIFY_CANCEL_MESSAGE establecida para indicar al proveedor que debe liberar los objetos abiertos y detener la transferencia de mensajes. 
  
El proveedor de transporte no debe enviar ninguna propiedad notransmitible del mensaje. Cuando encuentre dicha propiedad, debe seguir procesando la siguiente propiedad. El proveedor debe hacer todo lo posible para no mostrar MAPI_P1 de destinatarios como parte del contenido del mensaje transmitido; el proveedor debe usar esta información de destinatario solo con fines de direccionamiento. MAPI_P1 destinatarios son destinatarios generados internamente que se usan para reenviar mensajes; no deben transmitirse. En su lugar, use los demás destinatarios para transmitir información del destinatario. El propósito de este acuerdo es permitir que los destinatarios que vuelvan a enviar vean exactamente la misma tabla de destinatarios que los destinatarios originales.
  
Durante una **llamada SubmitMessage,** la cola MAPI procesa métodos para objetos que se abren durante la transferencia del mensaje y procesa los datos adjuntos. Este procesamiento puede tardar mucho tiempo. Los proveedores de transporte pueden llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este procesamiento para liberar tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios del mensaje están visibles en la tabla de destinatarios del mensaje que pasó originalmente la cola MAPI. El proveedor de transporte debe procesar solo los destinatarios que pueda controlar , en función del identificador de entrada, el tipo de dirección o ambos, y que aún no tengan la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en TRUE. Si **PR_RESPONSIBILITY** está establecido en TRUE, otro proveedor de transporte controla ese destinatario. Cuando el proveedor complete el procesamiento suficiente de un destinatario para determinar si puede controlar los mensajes de ese destinatario, debe establecer la propiedad **PR_RESPONSIBILITY** del destinatario en TRUE en el mensaje pasado. Normalmente, el proveedor toma esta determinación una vez completada la entrega del mensaje. 
  
Normalmente, el proveedor de transporte no vuelve de una llamada **SubmitMessage** hasta que completa la transferencia de datos del mensaje. Si no se devuelve ningún error, la siguiente llamada de la cola MAPI al proveedor es una llamada al método [IXPLogon::EndMessage.](ixplogon-endmessage.md) 
  
Si **SubmitMessage** devuelve un error, la cola MAPI libera el mensaje en proceso sin guardar los cambios. Si el proveedor de transporte requiere que se guarden los cambios de mensajes, debe llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje antes de devolverlo. 
  
En caso de errores que se producen debido a problemas de transporte, la cola MAPI conserva el mensaje, pero retrasa el reenvío del mensaje al proveedor de transporte en función del valor devuelto en  _lpulReturnParm_. El proveedor de transporte debe rellenar ese valor si su valor devuelto de **SubmitMessage** es MAPI_E_WAIT o MAPI_E_NETWORK_ERROR. Si se produce una condición de error grave, el proveedor de transporte debe llamar al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_CRITICAL_ERROR datos. 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

