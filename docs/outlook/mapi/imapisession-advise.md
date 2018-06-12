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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817446"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Se aplica a**: Outlook 
  
Se registra para recibir notificaciones de los eventos que afectan a la sesión.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Sintaxis

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la libreta de direcciones o mensaje almacén de objeto sobre el que se deben generar notificaciones o NULL, que indica que el cliente se está registrando para recibir notificaciones sobre los eventos que afectan a la sesión de sólo. 
    
 _ulEventMask_
  
> [entrada] Una máscara de valores que se indican los tipos de eventos de notificación que el cliente está interesado en y se debe incluir en el registro. Si _lpEntryID_ es NULL, MAPI registra automáticamente el cliente para los eventos de error crítico que afectan a sólo la sesión. Cuando _lpEntryID_ apunta a un identificador de entrada, los valores siguientes son válidos para el parámetro _ulEventMask_ : 
    
fnevCriticalError 
  
> Registra las notificaciones acerca de los errores graves, como memoria insuficiente.
    
fnevExtended 
  
> Registra las notificaciones sobre los eventos específicos de una libreta de direcciones determinada o un mensaje de proveedor de almacén y acerca de la sesión de apagado.
    
fnevNewMail 
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
fnevObjectCreated 
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
fnevObjectCopied
  
> Registra las notificaciones sobre un objeto que se está copiando.
    
fnevObjectDeleted
  
> Registra las notificaciones sobre un objeto que se va a eliminar.
    
fnevObjectModified
  
> Registra las notificaciones sobre un objeto que se va a modificar.
    
fnevObjectMoved
  
> Registra las notificaciones sobre un objeto que se va a mover.
    
fnevSearchComplete
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores. Este objeto de receptor advise debe ya se han asignado.
    
 _lpulConnection_
  
> [out] Un puntero a un número distinto de cero que representa la conexión entre el autor de la llamada de aviso objeto receptor y la sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada que señala _lpEntryID_ no representa un identificador de entrada válido. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de servicio responsable para el identificador de entrada que señala _lpEntryID_ no admite el tipo de eventos especificado en el parámetro _ulEventMask_ o no admite la notificación. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada que señala _lpEntryID_ no se puede controlar mediante cualquiera de los proveedores de servicios en el perfil. 
    
## <a name="remarks"></a>Notas

El método **IMAPISession::Advise** establece una conexión entre el autor de la llamada del objeto de receptor, la sesión y, opcionalmente, un proveedor de servicios de avisos. Esta conexión se utiliza para enviar las notificaciones para el receptor de notificaciones cuando uno o más eventos especificados en el parámetro _ulEventMask_ se producen en el objeto al que señala por _lpEntryID_. Cuando _lpEntryID_ es NULL, el objeto de destino es la sesión y se envían únicamente para los errores críticos y eventos extendidos. 
  
Cuando _lpEntryID_ apunta a un identificador de entrada válido, MAPI llama al método **Advise** del objeto de inicio de sesión que pertenece al proveedor de servicios responsable. Por ejemplo, si _lpEntryID_ puntos para el identificador de entrada de una lista de distribución, MAPI llama (método [IABLogon::Advise](iablogon-advise.md) ) del proveedor de la libreta de dirección adecuada. 
  
Para enviar una notificación, el proveedor de servicios o MAPI llama (método) [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor advise registrados. Uno de los parámetros para **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En los sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento. Si necesita garantía de que las notificaciones se producen sólo en un momento determinado en un subproceso concreto, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de receptor advise que se pasa al método **Advise** . 
  
Para determinar cuando un cliente ha cerrado la sesión, registrar para las notificaciones en su proveedor de servicios mediante una llamada a **Advise** con _lpEntryID_ establecido en NULL y _cbEntryID_ establece en 0. Cuando se produce el cierre de sesión, recibirá una notificación de fnevExtended. 
  
Después de que se ha realizado correctamente una llamada a **Advise** y antes de que se ha llamado a [IMAPISession::Unadvise](imapisession-unadvise.md) para cancelar el registro, versión de su objeto de receptor advise a menos que tengan un uso específico a largo plazo para él. 
  
Para obtener información general del proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
Para obtener más información acerca de cómo controlar las notificaciones, vea [Controlar notificaciones](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utiliza el método **IMAPISession::Advise** para registrar para notificaciones de la sesión.  <br/> |
   
## <a name="see-also"></a>Ver también



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Notificación de eventos en MAPI](event-notification-in-mapi.md)

