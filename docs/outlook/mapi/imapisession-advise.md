---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419838"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se registra para recibir una notificación de eventos especificados que afectan a la sesión.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada de la libreta de direcciones o del objeto de almacén de mensajes sobre qué notificaciones se deben generar, o NULL, que indica que el cliente se está registrando para recibir notificaciones sobre eventos que afectan solo a la sesión. 
    
 _ulEventMask_
  
> a Máscara de valores que indican los tipos de eventos de notificación en los que está interesado el cliente y deben incluirse en el registro. Si _lpEntryID_ es null, MAPI registra automáticamente el cliente para los eventos de error críticos que afectan solo a la sesión. Cuando _lpEntryID_ apunta a un identificador de entrada, los siguientes valores son válidos para el parámetro _ulEventMask_ : 
    
fnevCriticalError 
  
> Registra las notificaciones sobre errores graves, como memoria insuficiente.
    
fnevExtended 
  
> Registra las notificaciones sobre eventos específicos de una libreta de direcciones o un proveedor de almacenamiento de mensajes determinados y sobre el cierre de sesión.
    
fnevNewMail 
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
fnevObjectCreated 
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
fnevObjectCopied
  
> Registra notificaciones sobre un objeto que se está copiando.
    
fnevObjectDeleted
  
> Registra notificaciones sobre un objeto que se está eliminando.
    
fnevObjectModified
  
> Registra notificaciones sobre un objeto que se está modificando.
    
fnevObjectMoved
  
> Registra notificaciones sobre un objeto que se está moviendo.
    
fnevSearchComplete
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores. Este objeto de receptor de notificaciones debe haber sido asignado ya.
    
 _lpulConnection_
  
> contempla Un puntero a un número distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y la sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada al que apunta _lpEntryID_ no representa un identificador de entrada válido. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de servicios responsable del identificador de entrada al que apunta _lpEntryID_ no admite el tipo de eventos especificados en el parámetro _ulEventMask_ o no admite la notificación. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Ninguno de los proveedores de servicios del perfil puede controlar el identificador de entrada al que apunta _lpEntryID_ . 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: Advise** establece una conexión entre el objeto de notificación de notificaciones del receptor del autor de la llamada, la sesión y, opcionalmente, un proveedor de servicios. Esta conexión se usa para enviar notificaciones al receptor de notificaciones cuando se producen uno o más eventos especificados en el parámetro _ulEventMask_ en el objeto al que señala _lpEntryID_. Cuando _lpEntryID_ es null, el objeto de destino es la sesión y las notificaciones se envían solo para errores críticos y eventos extendidos. 
  
Cuando _lpEntryID_ apunta a un identificador de entrada válido, MAPI llama al **** método Advise del objeto de inicio de sesión que pertenece al proveedor de servicios responsable. Por ejemplo, si _lpEntryID_ apunta al identificador de entrada de una lista de distribución, MAPI llama al método [IABLogon:: Advise](iablogon-advise.md) del proveedor de la libreta de direcciones correspondiente. 
  
Para enviar una notificación, el proveedor de servicios o MAPI llama al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor registrado. Uno de los parámetros para **BENOTIFY**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** también puede producirse en cualquier subproceso en cualquier momento. Si necesita asegurarse de que las notificaciones solo se producirán en un momento determinado de un subproceso en particular, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de notificación de aviso que se pasa al método Advise. **** 
  
Para determinar cuándo un cliente ha cerrado la sesión, registre las notificaciones en su proveedor de servicios **** llamando a Advise con _LPENTRYID_ establecido en NULL y _cbEntryID_ establecido en 0. Cuando se produzca el cierre de sesión, recibirá una notificación de fnevExtended. 
  
Después de que una **** llamada a Advise se haya realizado correctamente y antes de que se haya llamado a [IMAPISession:: Unadvise](imapisession-unadvise.md) para cancelar el registro, libere el objeto de notificación de avisos a menos que tenga un uso específico a largo plazo. 
  
Para obtener información general sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
Para obtener más información sobre el control de notificaciones, consulte [control](handling-notifications.md)de notificaciones. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI usa el método **IMAPISession:: Advise** para registrarse en las notificaciones en la sesión.  <br/> |
   
## <a name="see-also"></a>Ver también



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Notificación de eventos en MAPI](event-notification-in-mapi.md)

