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

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada de la libreta de direcciones o del objeto del almacén de mensajes sobre qué notificaciones se deben generar, o NULL, que indica que el cliente se está registrando para recibir notificaciones sobre eventos que afectan solo a la sesión. 
    
 _ulEventMask_
  
> [entrada] Máscara de valores que indica los tipos de eventos de notificación que el cliente está interesado y debe incluirse en el registro. Si  _lpEntryID_ es NULL, MAPI registra automáticamente el cliente para eventos de error crítico que afectan solo a la sesión. Cuando _lpEntryID_ apunta a un identificador de entrada, los siguientes valores son válidos para el _parámetro ulEventMask:_ 
    
fnevCriticalError 
  
> Registra las notificaciones sobre errores graves, como la memoria insuficiente.
    
fnevExtended 
  
> Se registra para notificaciones sobre eventos específicos de un proveedor de libreta de direcciones o almacén de mensajes en particular y sobre el cierre de sesión.
    
fnevNewMail 
  
> Se registra para recibir notificaciones sobre la llegada de mensajes nuevos. 
    
fnevObjectCreated 
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
fnevObjectCopied
  
> Registra las notificaciones sobre un objeto que se está copiando.
    
fnevObjectDeleted
  
> Registra las notificaciones sobre un objeto que se va a eliminar.
    
fnevObjectModified
  
> Registra notificaciones sobre un objeto que se está modificando.
    
fnevObjectMoved
  
> Registra las notificaciones sobre un objeto que se está trasladando.
    
fnevSearchComplete
  
> Se registra para recibir notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso ya debe haber sido asignado.
    
 _lpulConnection_
  
> [salida] Puntero a un número distinto de cero que representa la conexión entre el objeto receptor de aviso del autor de la llamada y la sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se ha realizado correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada al que  _apunta lpEntryID_ no representa un identificador de entrada válido. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de servicios responsable del identificador de entrada al que apunta  _lpEntryID_ no admite el tipo de eventos especificados en el parámetro  _ulEventMask_ o no admite la notificación. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada al que  _apunta lpEntryID_ no puede ser manipulado por ninguno de los proveedores de servicios del perfil. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::Advise** establece una conexión entre el objeto receptor de avisos del autor de la llamada, la sesión y, opcionalmente, un proveedor de servicios. Esta conexión se usa para enviar notificaciones al receptor de avisos cuando se producen uno o más eventos especificados en el parámetro  _ulEventMask_ al objeto al que  _apunta lpEntryID_. Cuando  _lpEntryID_ es NULL, el objeto de destino es la sesión y las notificaciones se envían solo para errores críticos y eventos extendidos. 
  
Cuando  _lpEntryID_ apunta a un identificador de entrada válido, MAPI llama al método **Advise** del objeto de inicio de sesión que pertenece al proveedor de servicios responsable. Por ejemplo, si  _lpEntryID_ apunta al identificador de entrada de una lista de distribución, MAPI llama al método [IABLogon::Advise](iablogon-advise.md) del proveedor de libreta de direcciones correspondiente. 
  
Para enviar una notificación, el proveedor de servicios o MAPI llama al método [IMAPIAdviseSink::OnNotify del](imapiadvisesink-onnotify.md) receptor de avisos registrado. Uno de los parámetros de **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento. Si necesita garantía de que las notificaciones se producirán solo en un momento determinado en un subproceso determinado, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto receptor de aviso que pase al método **Advise.** 
  
Para determinar cuándo un cliente ha cerrado sesión, regístrese para recibir notificaciones en el proveedor de servicios llamando a **Advise** con  _lpEntryID_ establecido en NULL y  _cbEntryID_ establecido en 0. Cuando se produzca el cierre de sesión, recibirás una notificación fnevExtended. 
  
Una vez que se haya realizado correctamente una llamada a **Advise** y antes de que se haya llamado a [IMAPISession::Unadvise](imapisession-unadvise.md) para cancelar el registro, libere el objeto receptor de aviso a menos que tenga un uso específico a largo plazo para él. 
  
Para obtener información general sobre el proceso de notificación, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
Para obtener más información acerca del control de notificaciones, vea [Control de notificaciones.](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa el **método IMAPISession::Advise** para registrar notificaciones en la sesión.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Notificación de eventos en MAPI](event-notification-in-mapi.md)

