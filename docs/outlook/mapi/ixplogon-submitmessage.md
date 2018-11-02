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
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575878"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Indica que la cola MAPI tiene un mensaje para el proveedor de transporte entregar.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se envía el mensaje. Se puede establecer la marca siguiente:
    
BEGIN_DEFERRED 
  
> La cola MAPI llama a un proveedor de transporte con un mensaje que anteriormente se difirió. El identificador de entrada del mensaje es igual al que se difirió. El mensaje se difirió pasando su identificador de entrada a la cola MAPI mediante el método [SpoolerNotify](imapisupport-spoolernotify.md) con el indicador NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> [entrada] Un puntero a un objeto de mensaje (que representa el mensaje para entregar) que tiene permiso de lectura y escritura, que el proveedor de transporte que se usa para tener acceso y manipular ese mensaje. Este objeto sigue siendo válida hasta después de que el proveedor de transporte que se devuelve desde una llamada posterior al método [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> [out] Un puntero a una variable en el que el proveedor de transporte devuelve el valor de referencia asigna a este mensaje. La cola MAPI pasa este valor de referencia en las llamadas posteriores para este mensaje. La cola MAPI inicializa el valor en 0 antes de devolverlo al proveedor de transporte.
    
 _lpulReturnParm_
  
> [out] Un puntero a una variable que se corresponde con el valor de error MAPI_E_WAIT o MAPI_E_NETWORK_ERROR devuelto por **SubmitMessage**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
MAPI_E_BUSY 
  
> El proveedor de transporte no puede controlar el mensaje porque está realizando otra operación. Un proveedor debe usar el valor devuelto para indicar que se ha producido ningún procesamiento y que la cola MAPI no debe llamar a **EndMessage**. La cola MAPI se la llamada **SubmitMessage** a intentarlo más tarde. 
    
MAPI_E_CANCEL 
  
> Aunque el proveedor de transporte solicita que la cola MAPI volver a enviar el mensaje en una anterior llamada **SpoolerNotify** , se cambió el nombre de las condiciones y no se debe volver a enviar el mensaje. La cola MAPI se realizarán controlar algo más. 
    
MAPI_E_NETWORK_ERROR 
  
> Un error de red no se les permita la finalización correcta de la operación. El parámetro _lpulReturnParm_ debe establecerse en el número de segundos que deberá transcurrir antes de que la cola MAPI vuelve a enviar el mensaje. 
    
MAPI_E_NOT_ME 
  
> El proveedor de transporte no puede controlar este mensaje. La cola MAPI debe intentar encontrar a otro proveedor de transporte para el mismo. Un proveedor debe usar el valor devuelto para indicar que se ha producido ningún procesamiento y que la cola MAPI no debe llamar a **EndMessage**.
    
MAPI_E_WAIT 
  
> Un problema temporal impide que el proveedor de transporte de controlar el mensaje. El parámetro _lpulReturnParm_ debe establecerse en el número de segundos que deberá transcurrir antes de que la cola MAPI vuelve a enviar el mensaje. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::SubmitMessage** cuando tiene un mensaje para el proveedor de transporte entregar. El mensaje se pasa al proveedor de transporte mediante el parámetro _lpMessage_ . 
  
Si el proveedor está listo para aceptar el mensaje, debe devolver un valor de referencia con el parámetro _lpulMsgRef_ , el objeto pasado, de proceso y devolver el valor apropiado (normalmente S_OK). Si el proveedor no está preparado para controlar a la transferencia, debe devolver un valor de error y, opcionalmente, MAPI otro valor devuelto en _lpulReturnParm_ para indicar cuánto tiempo debe esperar la cola MAPI antes de volver a enviar el mensaje. 
  
Implementación del proveedor de transporte de este método puede hacer lo siguiente:
  
- Poner el mensaje en una cola interna que se debe esperar para la transmisión, copiar, posiblemente, el mensaje al almacenamiento local y devolver.
    
- Intente realizar la transmisión real y devolver una vez completada la transmisión, correctamente o no.
    
- Determine si desea enviar el mensaje después de comprobar los recursos necesarios para. En este caso, si el recurso es gratuito, el proveedor puede bloquear el recurso, preparar el mensaje y enviarlo. Si el recurso no está disponible, el proveedor puede preparar el mensaje y aplazar el envío a un momento posterior.
    
La técnica preferida para la transmisión de mensajes depende del proveedor de transporte y el número esperado de procesos compiten por los recursos del sistema. 
  
Durante una llamada **SubmitMessage** , el proveedor de transporte controla a la transferencia de datos de los mensajes desde el objeto de mensaje. Sin embargo, el proveedor de transporte debe asignar un valor de referencia para el mensaje, a la que devuelve un puntero en _lpulMsgRef_, antes de transferir los datos. Se lo debido a que en cualquier momento durante el proceso, la cola MAPI puede llamar al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) con la marca NOTIFY_CANCEL_MESSAGE establecer para señalar al proveedor que debe liberar todos los objetos abiertos y detener la transferencia de mensajes. 
  
El proveedor de transporte no debe enviar las propiedades nontransmittable del mensaje. Cuando se encuentre este tipo de propiedad, debe ir procesar la siguiente propiedad. El proveedor debe realizar todos los esfuerzos no se muestre información del destinatario MAPI_P1 como parte del contenido del mensaje transmitido; el proveedor debe usar esta información de destinatarios sólo para hacer frente a fines. Destinatarios de MAPI_P1 son los destinatarios generados internamente que se usan para volver a enviar mensajes; no debe ser transmitidos. En su lugar, use los otros destinatarios para transmitir información del destinatario. El propósito de este tipo de organización es permitir que los destinatarios de reenvío para ver la tabla de destinatarios misma exacta que los destinatarios originales.
  
Durante una llamada **SubmitMessage** , la cola MAPI procesa los métodos para los objetos que se abren durante la transferencia del mensaje y procesa los datos adjuntos. Este proceso puede tardar mucho tiempo. Los proveedores de transporte pueden llamar al método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para la cola MAPI con frecuencia durante este proceso para liberar el tiempo de CPU para otras tareas del sistema. 
  
Todos los destinatarios del mensaje son visibles en la tabla de destinatarios del mensaje que se pasó originalmente la cola de MAPI. El proveedor de transporte debe procesar solo aquellos destinatarios que pueden controlar — según el identificador de entrada, el tipo de dirección o ambos — y que aún no tiene su propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en TRUE. Si **PR_RESPONSIBILITY** ya está establecida en TRUE, otro proveedor de transporte ha controlado a que el destinatario. Cuando el proveedor complete el procesamiento suficiente de un destinatario para determinar si pueden administrar los mensajes para que el destinatario, debe establecer propiedad de ese destinatario **PR_RESPONSIBILITY** en TRUE en el mensaje pasado. Normalmente, el proveedor realiza esta determinación una vez finalizada la entrega del mensaje. 
  
Normalmente, el proveedor de transporte no devuelve desde una llamada de **SubmitMessage** hasta que se complete a la transferencia de datos de mensaje. Si se devuelve ningún error, la siguiente llamada desde la cola de MAPI para el proveedor es una llamada al método [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
  
Si **SubmitMessage** devuelve un error, la cola MAPI libera el mensaje en proceso sin guardar los cambios. Si el proveedor de transporte requiere que los cambios de mensaje que se guarde, debe llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje antes de devolver. 
  
En el caso de errores que se producen debido a problemas de transporte, la cola MAPI conserva el mensaje, pero retrasa el volver a enviar el mensaje para el proveedor de transporte basándose en el valor devuelto en _lpulReturnParm_. Si su valor devuelto desde **SubmitMessage** es MAPI_E_WAIT o MAPI_E_NETWORK_ERROR, debe rellenar el proveedor de transporte en ese valor. Si se produce una condición de error grave, el proveedor de transporte debe llamar al método [SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

