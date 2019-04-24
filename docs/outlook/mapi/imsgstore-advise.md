---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317328"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se registra para recibir una notificación de eventos especificados que afectan al almacén de mensajes.
  
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
  
> a Un puntero al identificador de entrada de la carpeta o mensaje sobre qué notificaciones se deben generar o **null**. Si _lpEntryID_ se establece en null, **Advise** registra las notificaciones en todo el almacén de mensajes. 
    
 _ulEventMask_
  
> a Máscara de valores que indican los tipos de eventos de notificación en los que está interesado el autor de la llamada y que deben incluirse en el registro. Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. Los siguientes son valores válidos para el parámetro _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Registra las notificaciones sobre errores graves, como memoria insuficiente.
    
 _fnevExtended_
  
> Registra notificaciones sobre eventos específicos del proveedor de almacén de mensajes en particular.
    
 _fnevNewMail_
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de una nueva carpeta o mensaje.
    
 _fnevObjectCopied_
  
> Registra notificaciones sobre una carpeta o un mensaje que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra notificaciones sobre una carpeta o un mensaje que se está eliminando.
    
 _fnevObjectModified_
  
> Registra notificaciones sobre una carpeta o un mensaje que se está modificando.
    
 _fnevObjectMoved_
  
> Registra notificaciones sobre una carpeta o un mensaje que se está moviendo.
    
 _fnevSearchComplete_
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores. Este objeto de receptor de notificaciones debe haber sido asignado ya.
    
 _lpulConnection_
  
> contempla Un puntero a un número distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y la sesión. 
    
 _lpAdviseSink_
  
> a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores. Este objeto de receptor de notificaciones debe haber sido asignado ya. 
    
 _lpulConnection_
  
> contempla Un puntero a un número de conexión distinto de cero que representa la conexión entre el objeto de aviso de aviso del autor de la llamada y el almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se realizó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de almacenamiento de mensajes no admite el registro para la notificación a través del almacén de mensajes.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: Advise** establece una conexión entre el objeto de notificación de notificaciones del receptor del autor de la llamada y el almacén de mensajes o un objeto en el almacén de mensajes. Esta conexión se usa para enviar notificaciones al receptor de notificaciones cuando uno o más eventos, tal como se especifica en el parámetro _ulEventMask_ , se producen en el objeto de origen Advise. Cuando el parámetro _lpEntryID_ apunta a un identificador de entrada válido, el origen Advise es el objeto identificado por este identificador de entrada. Cuando _lpEntryID_ es null, el origen de Advise es el almacén de mensajes. 
  
Para enviar una notificación, el proveedor de almacenamiento de mensajes o MAPI llama al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor registrado. Uno de los parámetros para **BENOTIFY**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir la notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de soporte para ayudar a los proveedores de servicios a implementar la notificación: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport:: Notify](imapisupport-notify.md). Si decide usar los métodos de compatibilidad con MAPI, llame a **subscribe** cuando se llame al método Advise y suelte el puntero _lpAdviseSink_ . **** 
  
Si opta por admitir la notificación usted mismo, llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para conservar una copia de este puntero. Mantenga esta copia hasta que se llame al método [IMsgStore:: Unadvise](imsgstore-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo se admita la notificación, asigne un número de conexión distinto de cero al registro de notificaciones y devuelva el parámetro _lpulConnection_ . No libere este número de conexión hasta que se haya llamado a **Unadvise** y haya finalizado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** también puede producirse en cualquier subproceso en cualquier momento. Si tiene la certeza de que las notificaciones solo se producen en un momento determinado en un determinado subproceso, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de notificación de aviso que pasa a Advise. **** 
  
Después de llamar a **Advise** correctamente y antes **** de llamar a Unadvise para cancelar el registro, prepárese para que se publique el objeto receptor de notificaciones. Debe liberar su objeto de notificación de notificaciones después de que se devuelva **Advise** a menos que tenga un uso específico a largo plazo. 
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
Para obtener más información sobre el control de notificaciones, consulte [control](handling-notifications.md)de notificaciones. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI usa el método **IMsgStore:: Advise** para registrarse en las notificaciones en todo el almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

