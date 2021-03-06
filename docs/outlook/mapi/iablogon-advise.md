---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428231"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra al autor de la llamada para recibir una notificación de eventos especificados que afectan a un contenedor, un usuario de mensajería o una lista de distribución.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del objeto sobre qué notificaciones se deben generar.
    
 _ulEventMask_
  
> [in] Máscara de bits de valores que indican los tipos de eventos de notificación que el autor de la llamada está interesado y debe incluirse en el registro. Hay una estructura [notification](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. En la tabla siguiente se enumeran los valores válidos para  _el parámetro ulEventMask_ y las estructuras asociadas a cada valor. 
    
|**Tipo de evento Notification**|**Estructura **de NOTIFICACIÓN** correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores.
    
 _lpulConnection_
  
> [salida] Puntero a un valor distinto de cero que representa el registro de notificaciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación se ha realizado correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada pasado en el  _parámetro lpEntryID_ no tiene el formato adecuado. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de libreta de direcciones no admite notificaciones, posiblemente porque no permite que se realicen cambios en sus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de libreta de direcciones no puede controlar el identificador de entrada pasado  _en lpEntryID_.
    
## <a name="remarks"></a>Comentarios

Los proveedores de libreta de direcciones implementan el método **IABLogon::Advise** para registrar al autor de la llamada para recibir una notificación cuando se produce un cambio en un objeto en uno de sus contenedores. Los autores de llamadas pueden registrarse para recibir notificaciones sobre usuarios de mensajería, listas de distribución o contenedores completos. 
  
Normalmente, los clientes llaman al [método IAddrBook::Advise](iaddrbook-advise.md) para registrar las notificaciones de la libreta de direcciones. A continuación, MAPI llama al **método Advise** del proveedor de libreta de direcciones responsable del objeto representado por el identificador de entrada en  _lpEntryID_.
  
Cuando se produce un cambio en el objeto indicado del tipo representado en  _ulEventMask_, se realiza una llamada al método **OnNotify** del receptor de avisos señalado por  _lpAdviseSink_. Los datos pasados en la **estructura NOTIFICATION** a la **rutina OnNotify** describen el evento. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir la notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de soporte técnico para ayudar a los proveedores de servicios a implementar la notificación:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si decide usar los métodos de soporte técnico MAPI, llame a **Subscribe** cuando se llame al método **Advise** y libere el puntero _lpAdviseSink._ 
  
Si decide admitir la notificación usted mismo, llame al método **AddRef** del receptor advise representado por el parámetro  _lpAdviseSink_ para mantener una copia de este puntero. Mantenga esta copia hasta que se llame al [método IABLogon::Unadvise](iablogon-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo admita la notificación, asigne un número de conexión distinto de cero al registro de notificación y devolución en el _parámetro lpulConnection._ No libere este número de conexión hasta que se haya llamado al método **Unadvise.** 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El puntero del receptor de aviso que se pasa en el parámetro _lpAdviseSink_ a **Advise** puede apuntar a un objeto que haya creado o que MAPI haya creado a través de la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) Es posible que desee usar **HrThisThreadAdviseSink** si admite varios subprocesos de ejecución y desea asegurarse de que las llamadas posteriores al método **OnNotify** se produzcan en el momento adecuado en un subproceso adecuado. 
  
Esté preparado para que el objeto receptor de aviso se liberará en cualquier momento después de la llamada a **Advise** y antes de la llamada **a Unadvise**. Por lo tanto, debe liberar el objeto receptor advise después de **que advise** devuelva, a menos que tenga un uso específico a largo plazo para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). Para obtener información sobre cómo usar los métodos **IMAPISupport** para admitir la notificación, vea [Supporting Event Notification](supporting-event-notification.md). Para obtener más información sobre multithreading y MAPI, vea [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

