---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2837e5470729ae3cdd0b83e17d0342620c986e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592118"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica a la cola MAPI de un cambio de estado o una solicitud de servicio. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica el tipo de notificación. Los proveedores de transporte pueden establecer todas las marcas excepto NOTIFY_NEWMAIL_RECEIVED; sólo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de almacén de mensajes. Las siguientes marcas son válidas para el parámetro _ulFlags indicado_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Registra una solicitud para cambiar la configuración del proveedor de transporte. 
    
NOTIFY_CRITICAL_ERROR 
  
> Se ha producido un error irrecuperable al proveedor de transporte. Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ para las llamadas del proveedor de transporte, estos marcadores son mutuamente excluyentes. 
    
NOTIFY_CRITSEC 
  
> Solicita una sección crítica para el proveedor de transporte. El parámetro _lpvData_ no está definido y debe ser nulo. 
    
NOTIFY_NEWMAIL 
  
> La cola MAPI debe descargar todos los mensajes recibidos recientemente en la siguiente hora disponible. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Se ha recibido un mensaje nuevo en el almacén de mensajes. El parámetro _lpvData_ apunta a una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje. Este indicador se usa para los proveedores de almacén de mensajes que estén asociados estrechamente con los proveedores de transporte y se omite si el proveedor de almacenamiento se inició sesión con el conjunto de marca MAPI_NO_MAIL. 
    
NOTIFY_NONCRIT 
  
> Libera una sección crítica que se obtuvieron con una llamada anterior a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_CRITSEC. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_READYTOSEND 
  
> El proveedor de almacén de transporte o un mensaje está listo para enviar los mensajes. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Ahora se debe enviar un mensaje diferido anteriormente, y el proveedor de transporte debe recibir una notificación cuando el mensaje está listo para entregar mediante una llamada al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . El identificador de entrada del mensaje diferido se encuentra en una estructura [SBinary](sbinary.md) que señala _lpvData_. Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ , estos marcadores son mutuamente excluyentes. 
    
 _lpvData_
  
> [entrada] Un puntero a datos asociados aplicables a una notificación. El parámetro _lpvData_ apunta a datos válidos sólo cuando se establecen los siguientes indicadores (_lpvData_ es NULL cuando _ulFlags_ está establecida en los otros tipos de notificación): 
    
|**configuración de _ulFlags_**|**valor de _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Información sobre el error.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Una estructura **NEWMAIL_NOTIFICATION** que contiene información acerca del mensaje recién enviado.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Una estructura **SBinary** que contiene el identificador de entrada del mensaje diferido.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación fue correcta.
    
## <a name="remarks"></a>Comentarios

Se implementa el método **SpoolerNotify** para mensaje almacenar y objetos de soporte técnico del proveedor de transporte. Estos proveedores de llamadas **SpoolerNotify** para notificar a la cola MAPI de un cambio de estado o una solicitud de servicio. **SpoolerNotify** se denomina principalmente por proveedores de transporte y se puede llamar en cualquier momento durante la sesión. 
  
## <a name="notes-to-transport-providers"></a>Notas para los proveedores de transporte

Si ha cambiado la configuración del proveedor de transporte, llame **SpoolerNotify** y establezca _ulFlags_ en NOTIFY_CONFIG_CHANGED. **SpoolerNotify** responde llamando al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones compatibles. 
  
Si necesita una sección crítica para asegurar el procesamiento ininterrumpido, llame a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_CRITSEC. Al establecer este indicador informa a la cola de MAPI que no debe llamar a los métodos [IXPLogon::Idle](ixplogon-idle.md) y [IXPLogon::Poll](ixplogon-poll.md) . Mientras tenga abierta una sección crítica, devolver MAPI_E_BUSY cada vez que se llama al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . Cuando haya terminado con la sección crítica, realizar otra llamada a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_NONCRIT. 
  
Por ejemplo, si su proveedor de transporte remoto está en proceso de carga de los mensajes, es posible que necesite permitir que un usuario que escriba un número de teléfono para establecer la conexión remota. Antes de recorrer el procedimiento de cuadro de diálogo, se debe declarar una sección crítica. Cuando el usuario cierra el cuadro de diálogo, terminar el procedimiento de cuadro de diálogo, debe liberar la sección crítica.
  
Cuando se establece _ulFlags_ a NOTIFY_CRITICAL_ERROR, la cola MAPI hace que no hay más llamadas para el proveedor excepto al liberarlo. Si se llama **SpoolerNotify** con NOTIFY_CRITICAL_ERROR establecer uno de los métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) o [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , devolver con un valor de error apropiado desde el que **desea iniciar** o ** SubmitMessage ** de llamadas inmediatamente después de la llamada **SpoolerNotify** . 
  
Si su proveedor de transporte recupera de una condición que previamente ha provocado un error, llame a **SpoolerNotify** con _ulFlags_ establecida en NOTIFY_READYTOSEND. Esta marca indica que el proveedor de nuevo está listo para administrar los mensajes. 
  
## <a name="notes-to-message-store-providers"></a>Notas para los proveedores de almacén de mensajes

Llamar a **SpoolerNotify**, se pasa el indicador NOTIFY_READYTOSEND en _ulFlags_, antes de realizar su primera llamada a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) en **IMessage::SubmitMessage**. Esta llamada a **SpoolerNotify** debe realizarse sólo una vez por sesión. 
  
Si su proveedor de almacén de mensajes se complementa con un transporte de proveedor y llame a **SpoolerNotify** con conjunto de _ulFlags_ a NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el mensaje nuevo y comienza el procesamiento de la función de enlace de mensaje nuevo. Una vez completado el procesamiento, la cola MAPI llama al método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje nuevo. 
  
Para obtener más información sobre cómo llamar a **SpoolerNotify**, vea cualquiera de los siguientes temas:
  
- [Implementar el método FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interactuar con el administrador de trabajos en cola MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modelo de recepción del mensaje](message-reception-model.md)
    
## <a name="see-also"></a>Recursos adicionales



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

