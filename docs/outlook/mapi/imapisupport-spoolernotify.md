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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326288"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica a la cola MAPI un cambio de estado o una solicitud de servicio. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que indica el tipo de notificación. Los proveedores de transporte pueden establecer todas las marcas excepto NOTIFY_NEWMAIL_RECEIVED; solo NOTIFY_NEWMAIL_RECEIVED y NOTIFY_READTOSEND son válidos para los proveedores de almacenamiento de mensajes. Las siguientes marcas son válidas para el parámetro _ulFlags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Registra una solicitud para cambiar la configuración del proveedor de transporte. 
    
NOTIFY_CRITICAL_ERROR 
  
> Se ha producido un error irrecuperable en el proveedor de transporte. Dado que tanto NOTIFY_SENTDEFERRED como NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ para las llamadas de proveedor de transporte, estas marcas se excluyen mutuamente. 
    
NOTIFY_CRITSEC 
  
> Solicita una sección crítica para el proveedor de transporte. El parámetro _lpvData_ no está definido y debe ser nulo. 
    
NOTIFY_NEWMAIL 
  
> La cola MAPI debe descargar los mensajes recibidos recientemente en el siguiente momento disponible. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Se ha recibido un mensaje nuevo en el almacén de mensajes. El parámetro _lpvData_ apunta a una estructura [NEWMAIL_NOTIFICATION](newmail_notification.md) que describe el mensaje. Esta marca se usa para los proveedores de almacenamiento de mensajes que están estrechamente asociados con los proveedores de transporte y se omite si el proveedor de almacenamiento inicia sesión con la marca MAPI_NO_MAIL establecida. 
    
NOTIFY_NONCRIT 
  
> Libera una sección crítica obtenida con una llamada anterior a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_CRITSEC. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_READYTOSEND 
  
> El proveedor de transporte o de almacenamiento de mensajes está preparado para enviar mensajes. El parámetro _lpvData_ no está definido y debe establecerse en NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Ahora debe enviarse un mensaje aplazado anteriormente y el proveedor de transporte debe recibir una notificación cuando el mensaje esté listo para entregarse mediante una llamada al método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . El identificador de entrada del mensaje aplazado está contenido en una estructura [SBinary](sbinary.md) a la que apunta _lpvData_. Como tanto NOTIFY_SENTDEFERRED como NOTIFY_CRITICAL_ERROR usan el parámetro _lpvData_ , estos indicadores se excluyen mutuamente. 
    
 _lpvData_
  
> a Un puntero a datos asociados aplicables a una notificación. El parámetro _lpvData_ apunta a datos válidos solo cuando se establecen los siguientes indicadores (_lpvData_ es NULL cuando _ulFlags_ se establece en los otros tipos de notificación): 
    
|**configuración de _ulFlags_**|**valor _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Información sobre el error.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Estructura **NEWMAIL_NOTIFICATION** que contiene información sobre el mensaje recién entregado.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Estructura **SBinary** que contiene el identificador de entrada del mensaje aplazado.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: SpoolerNotify** se implementa para los objetos de soporte de proveedor de transporte y almacén de mensajes. Estos proveedores llaman a **SpoolerNotify** para notificar a la cola de MAPI un cambio en el estado o una solicitud de servicio. Los proveedores de transporte llaman principalmente a **SpoolerNotify** , que pueden llamarse en cualquier momento durante la sesión. 
  
## <a name="notes-to-transport-providers"></a>Notas para los proveedores de transporte

Si ha cambiado la configuración de su proveedor de transporte, llame a **SpoolerNotify** y establezca _ulFlags_ en NOTIFY_CONFIG_CHANGED. **SpoolerNotify** responde llamando al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para consultar un cambio en los tipos de direcciones admitidos. 
  
Si necesita una sección crítica para garantizar un procesamiento sin interrupciones, llame a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_CRITSEC. Al establecer esta marca se informa a la cola MAPI de que no debe llamar a los métodos [IXPLogon:: idle](ixplogon-idle.md) y [IXPLogon::P Oll](ixplogon-poll.md) . Mientras tenga una sección crítica abierta, devuelva MAPI_E_BUSY cada vez que se llame al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . Cuando haya terminado con la sección crítica, realice otra llamada a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_NONCRIT. 
  
Por ejemplo, si el proveedor de transporte remoto se encuentra en el proceso de carga de mensajes, es posible que deba permitir a un usuario que escriba un número de teléfono para establecer la conexión remota. Antes de recorrer en bucle el procedimiento de cuadro de diálogo, debe declarar una sección crítica. Cuando el usuario cierra el cuadro de diálogo y finaliza el procedimiento de cuadro de diálogo, debe liberar la sección crítica.
  
Al establecer _ulFlags_ en NOTIFY_CRITICAL_ERROR, la cola MAPI no realiza más llamadas al proveedor excepto para liberarla. Si llama a **SpoolerNotify** con NOTIFY_CRITICAL_ERROR establecido desde los métodos [IXPLogon:: StartMessage](ixplogon-startmessage.md) o [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) , devuelve con un valor de error adecuado de la **StartMessage** o * * SubmitMessage * * llamada inmediatamente después de la llamada a **SpoolerNotify** . 
  
Si el proveedor de transporte se recuperó a partir de una condición que antes producía un error, llame a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_READYTOSEND. Esta marca indica que el proveedor está de nuevo preparado para controlar los mensajes. 
  
## <a name="notes-to-message-store-providers"></a>Notas a los proveedores de almacenamiento de mensajes

Llame a **SpoolerNotify**, pasando la marca NOTIFY_READYTOSEND en _ulFlags_, antes de realizar la primera llamada a [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) en **IMessage:: SubmitMessage**. Esta llamada a **SpoolerNotify** debe realizarse una sola vez por sesión. 
  
Si su proveedor de almacenamiento de mensajes está estrechamente acoplado a un proveedor de transporte y llama a **SpoolerNotify** con _ULFLAGS_ establecido en NOTIFY_NEWMAIL_RECEIVED, la cola MAPI abre el nuevo mensaje y comienza el procesamiento de la nueva función de enlace de mensaje. Una vez finalizado el procesamiento, la cola MAPI llama al método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para informarle de su propio mensaje. 
  
Para obtener más información acerca de cómo llamar a **SpoolerNotify**, vea cualquiera de los siguientes temas:
  
- [Implementar el método FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interacción con la cola MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modelo de recepción de mensajes](message-reception-model.md)
    
## <a name="see-also"></a>Vea también



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

