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
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423772"
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

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que indica el tipo de notificación. Los proveedores de transporte pueden establecer todas las marcas excepto las NOTIFY_NEWMAIL_RECEIVED; solo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de al almacenamiento de mensajes. Las siguientes marcas son válidas para el _parámetro ulFlags:_ 
    
NOTIFY_CONFIG_CHANGE 
  
> Registra una solicitud para cambiar la configuración del proveedor de transporte. 
    
NOTIFY_CRITICAL_ERROR 
  
> Se ha producido un error irrecuperable al proveedor de transporte. Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro  _lpvData_ para las llamadas del proveedor de transporte, estas marcas son mutuamente excluyentes. 
    
NOTIFY_CRITSEC 
  
> Solicita una sección crítica para el proveedor de transporte. El  _parámetro lpvData_ no está definido y debe ser NULL. 
    
NOTIFY_NEWMAIL 
  
> La cola MAPI debe descargar los mensajes recién recibidos en la próxima hora disponible. El  _parámetro lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Se ha recibido un nuevo mensaje en el almacén de mensajes. El  _parámetro lpvData_ apunta a una [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje. Esta marca se usa para los proveedores de almacenamiento de mensajes estrechamente asociados con los proveedores de transporte y se omite si el proveedor de almacenamiento ha iniciado sesión con la marca MAPI_NO_MAIL establecida. 
    
NOTIFY_NONCRIT 
  
> Libera una sección crítica que se obtuvo con una llamada anterior a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_CRITSEC. El  _parámetro lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_READYTOSEND 
  
> El proveedor de transporte o almacén de mensajes está listo para enviar mensajes. El  _parámetro lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Ahora se debe enviar un mensaje aplazado anteriormente y se debe notificar al proveedor de transporte cuando el mensaje esté listo para entregarse mediante una llamada al método [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) El identificador de entrada del mensaje diferido está contenido en una estructura [SBinary](sbinary.md) a la que  _apunta lpvData_. Dado que NOTIFY_SENTDEFERRED y NOTIFY_CRITICAL_ERROR usan el parámetro  _lpvData,_ estas marcas son mutuamente excluyentes. 
    
 _lpvData_
  
> [entrada] Puntero a los datos asociados aplicables a una notificación. El  _parámetro lpvData_ apunta a datos válidos solo cuando se establecen las siguientes marcas (_lpvData_ es NULL cuando  _ulFlags_ se establece en los otros tipos de notificación): 
    
|**_Configuración de ulFlags_**|**_Valor lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Información sobre el error.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Una **NEWMAIL_NOTIFICATION** que contiene información sobre el mensaje recién entregado.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Estructura **SBinary** que contiene el identificador de entrada del mensaje diferido.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::SpoolerNotify** se implementa para objetos de soporte de almacén de mensajes y proveedor de transporte. Estos proveedores llaman **a SpoolerNotify para** notificar a la cola MAPI de un cambio de estado o una solicitud de servicio. Los proveedores de transporte llaman principalmente a SpoolerNotify y se puede llamar a **SpoolerNotify** en cualquier momento durante la sesión. 
  
## <a name="notes-to-transport-providers"></a>Notas para proveedores de transporte

Si ha cambiado la configuración del proveedor de transporte, llame a **SpoolerNotify** y establezca  _ulFlags_ en NOTIFY_CONFIG_CHANGED. **SpoolerNotify** responde llamando al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones admitidos. 
  
Si necesita una sección crítica para garantizar un procesamiento ininterrumpido, llame a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_CRITSEC. Al establecer esta marca se informa a la cola MAPI de que no debe llamar a los métodos [IXPLogon::Idle](ixplogon-idle.md) e [IXPLogon::P oll.](ixplogon-poll.md) Mientras tenga abierta una sección crítica, MAPI_E_BUSY cada vez que se llame al método [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Cuando haya terminado con la sección crítica, realice otra llamada a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_NONCRIT. 
  
Por ejemplo, si su proveedor de transporte remoto está cargando mensajes, es posible que tenga que permitir que un usuario escriba un número de teléfono para establecer la conexión remota. Antes de recorrer en bucle el procedimiento del cuadro de diálogo, debe declarar una sección crítica. Cuando el usuario cierre el cuadro de diálogo, finalizando el procedimiento del cuadro de diálogo, debe liberar la sección crítica.
  
Cuando se establece  _ulFlags_ en NOTIFY_CRITICAL_ERROR, la cola MAPI no realiza ninguna otra llamada al proveedor excepto para liberarla. Si llama NOTIFY_CRITICAL_ERROR **SpoolerNotify** con un conjunto desde los métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) o [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) vuelva con un valor de error apropiado de la llamada **StartMessage** o ** SubmitMessage ** inmediatamente después de la llamada **SpoolerNotify.** 
  
Si el proveedor de transporte se recuperó de una condición que anteriormente causó un error, llame a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_READYTOSEND. Esta marca indica que el proveedor está de nuevo listo para administrar los mensajes. 
  
## <a name="notes-to-message-store-providers"></a>Notas para proveedores de almacén de mensajes

Llame a **SpoolerNotify**, pasando la marca NOTIFY_READYTOSEND en  _ulFlags_, antes de realizar la primera llamada a [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) en **IMessage::SubmitMessage**. Esta llamada a **SpoolerNotify** solo debe realizarse una vez por sesión. 
  
Si el proveedor de almacenamiento de mensajes está estrechamente unido a un proveedor de transporte y llama a **SpoolerNotify** con  _ulFlags_ establecido en NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el nuevo mensaje y comienza a procesar la nueva función de enlace de mensajes. Una vez completado el procesamiento, la cola MAPI llama al método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje nuevo. 
  
Para obtener más información acerca de **cómo llamar a SpoolerNotify,** consulte cualquiera de los siguientes temas:
  
- [Implementación del método FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interactuar con la cola MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modelo de recepción de mensajes](message-reception-model.md)
    
## <a name="see-also"></a>Consulte también



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

