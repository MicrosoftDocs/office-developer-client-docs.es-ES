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
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada de la carpeta o mensaje sobre qué notificaciones se deben generar o **null**. Si  _lpEntryID_ se establece en NULL, **Advise** registra las notificaciones en todo el almacén de mensajes. 
    
 _ulEventMask_
  
> [in] Máscara de valores que indica los tipos de eventos de notificación que el autor de la llamada está interesado y debe incluirse en el registro. Hay una estructura [notification](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. Los siguientes son valores válidos para el _parámetro ulEventMask:_ 
    
 _fnevCriticalError_
  
> Registra las notificaciones sobre errores graves, como la memoria insuficiente.
    
 _fnevExtended_
  
> Registra notificaciones sobre eventos específicos del proveedor de almacén de mensajes en particular.
    
 _fnevNewMail_
  
> Registra las notificaciones sobre la llegada de nuevos mensajes. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de una nueva carpeta o mensaje.
    
 _fnevObjectCopied_
  
> Registra las notificaciones sobre una carpeta o mensaje que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra las notificaciones sobre una carpeta o mensaje que se va a eliminar.
    
 _fnevObjectModified_
  
> Registra las notificaciones sobre una carpeta o mensaje que se está modificando.
    
 _fnevObjectMoved_
  
> Registra las notificaciones sobre una carpeta o mensaje que se va a mover.
    
 _fnevSearchComplete_
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> [in] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso ya debe haber sido asignado.
    
 _lpulConnection_
  
> [salida] Puntero a un número distinto de cero que representa la conexión entre el objeto receptor de aviso del autor de la llamada y la sesión. 
    
 _lpAdviseSink_
  
> [in] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso ya debe haber sido asignado. 
    
 _lpulConnection_
  
> [salida] Puntero a un número de conexión distinto de cero que representa la conexión entre el objeto receptor de aviso del autor de la llamada y el almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se ha realizado correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor del almacén de mensajes no admite el registro para la notificación a través del almacén de mensajes.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::Advise** establece una conexión entre el objeto receptor de avisos del autor de la llamada y el almacén de mensajes o un objeto del almacén de mensajes. Esta conexión se usa para enviar notificaciones al receptor de notificaciones cuando se producen uno o varios eventos, como se especifica en el parámetro  _ulEventMask,_ al objeto de origen advise. Cuando el  _parámetro lpEntryID_ apunta a un identificador de entrada válido, el origen de aviso es el objeto identificado por este identificador de entrada. Cuando  _lpEntryID_ es NULL, el origen de aviso es el almacén de mensajes. 
  
Para enviar una notificación, el proveedor del almacén de mensajes o MAPI llama al método [IMAPIAdviseSink::OnNotify del](imapiadvisesink-onnotify.md) receptor de notificaciones registrado. Uno de los parámetros de **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir la notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de soporte técnico para ayudar a los proveedores de servicios a implementar notificaciones: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport::Notify](imapisupport-notify.md). Si decide usar los métodos de soporte técnico MAPI, llame a **Subscribe** cuando se llame al método **Advise** y libere el puntero _lpAdviseSink._ 
  
Si decide admitir la notificación usted mismo, llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del receptor advise representado por el parámetro  _lpAdviseSink_ para mantener una copia de este puntero. Mantenga esta copia hasta que se llame al [método IMsgStore::Unadvise](imsgstore-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo admita la notificación, asigne un número de conexión distinto de cero al registro de notificación y devolución en el _parámetro lpulConnection._ No libere este número de conexión hasta que se haya llamado **a Unadvise** y se haya completado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento. Si debe estar seguro de que las notificaciones se producen solo en un momento determinado en un subproceso determinado, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto de receptor de notificaciones que pase a **Advise**. 
  
Después de que una llamada a **Advise** se haya realizado correctamente y antes de que se llame a **Unadvise** para cancelar el registro, prepárese para que se liberará el objeto de receptor de aviso. Debe liberar el objeto de receptor de aviso después de **que Advise** devuelva a menos que tenga un uso específico a largo plazo para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Para obtener más información sobre cómo controlar las notificaciones, vea [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa el **método IMsgStore::Advise** para registrar las notificaciones en todo el almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

