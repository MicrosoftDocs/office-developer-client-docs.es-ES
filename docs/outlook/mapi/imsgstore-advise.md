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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388249"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Se registra para recibir notificaciones de los eventos que afectan el almacén de mensajes.
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la carpeta o un mensaje acerca de qué notificaciones se deben generar o **null**. Si _lpEntryID_ se establece en NULL, **Advise** se registra para recibir notificaciones en el almacén de todo el mensaje. 
    
 _ulEventMask_
  
> [entrada] Una máscara de valores que se indican los tipos de eventos de notificación que el autor de la llamada está interesado en y se debe incluir en el registro. Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. Las siguientes son valores válidos para el parámetro _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Registra las notificaciones acerca de los errores graves, como memoria insuficiente.
    
 _fnevExtended_
  
> Proveedor de almacén de registros para las notificaciones sobre los eventos específicos para el mensaje concreto.
    
 _fnevNewMail_
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de una nueva carpeta o mensaje.
    
 _fnevObjectCopied_
  
> Registra las notificaciones sobre una carpeta o un mensaje que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra las notificaciones sobre una carpeta o un mensaje que se va a eliminar.
    
 _fnevObjectModified_
  
> Registra las notificaciones sobre una carpeta o un mensaje que se va a modificar.
    
 _fnevObjectMoved_
  
> Registra las notificaciones sobre una carpeta o un mensaje que se va a mover.
    
 _fnevSearchComplete_
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores. Este objeto de receptor advise debe ya se han asignado.
    
 _lpulConnection_
  
> [out] Un puntero a un número distinto de cero que representa la conexión entre el autor de la llamada de aviso objeto receptor y la sesión. 
    
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores. Este objeto de receptor advise debe ya se han asignado. 
    
 _lpulConnection_
  
> [out] Un puntero a un número distinto de cero de conexión que representa la conexión entre el autor de la llamada de aviso objeto receptor y el almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se realizó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de almacén de mensajes no es compatible con el registro de notificación mediante el almacén de mensajes.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::Advise** establece una conexión entre el autor de la llamada del aviso objeto receptor y el almacén de mensajes o un objeto en el almacén de mensajes. Esta conexión se utiliza para enviar las notificaciones para el receptor de notificaciones cuando uno o más eventos, tal como se especifica en el parámetro _ulEventMask_ , se producen en el objeto de origen advise. Cuando los puntos de parámetro _lpEntryID_ a un identificador de entrada válido, el origen de advise es el objeto identificado por este identificador de entrada. Cuando _lpEntryID_ es NULL, el origen de advise es el almacén de mensajes. 
  
Para enviar una notificación, el proveedor de almacén de mensajes o MAPI llama (método) [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor advise registrados. Uno de los parámetros para **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de soporte técnico para ayudar a los proveedores de servicios a implementar notificación: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport::Notify](imapisupport-notify.md). Si decide utilizar los métodos de soporte técnico MAPI, llamar a **Subscribe** cuando se llame al método **Advise** y liberar el puntero _lpAdviseSink_ . 
  
Si decide admitir la notificación usted mismo, llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del receptor advise representado por el parámetro _lpAdviseSink_ para mantener una copia de este puntero. Mantener esta copia hasta que se llama al método [IMsgStore::Unadvise](imsgstore-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo se admite la notificación, asigne a un número distinto de cero de conexión para el registro de la notificación y devolver en el parámetro _lpulConnection_ . No número de versión de esta conexión hasta que se ha llamado al **Unadvise** y se ha completado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En los sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento. Si debe estar seguro de que las notificaciones se producen sólo en un momento determinado en un subproceso concreto, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de receptor advise que pase a **Advise**. 
  
Después de llamar a **Advise** se ha realizado correctamente y esté preparado antes de que se ha llamado al **Unadvise** para cancelar el registro, para que el objeto de receptor advise que liberar. Debe liberar el objeto de receptor advise después **Advise** devuelve a menos que tengan un uso específico a largo plazo para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
Para obtener más información acerca de cómo controlar las notificaciones, vea [Controlar notificaciones](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI, utiliza el método **IMsgStore::Advise** para registrar las notificaciones de en el almacén de todo el mensaje.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

