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

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la carpeta o mensaje sobre qué notificaciones se deben generar, o **null**. Si  _lpEntryID_ se establece en NULL, **Advise** se registra para notificaciones en todo el almacén de mensajes. 
    
 _ulEventMask_
  
> [entrada] Máscara de valores que indica los tipos de eventos de notificación que el autor de la llamada está interesado y debe incluirse en el registro. Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. Los siguientes son valores válidos para _el parámetro ulEventMask:_ 
    
 _fnevCriticalError_
  
> Registra las notificaciones sobre errores graves, como la memoria insuficiente.
    
 _fnevExtended_
  
> Se registra para notificaciones sobre eventos específicos del proveedor de almacenamiento de mensajes en particular.
    
 _fnevNewMail_
  
> Se registra para recibir notificaciones sobre la llegada de nuevos mensajes. 
    
 _fnevObjectCreated_
  
> Se registra para recibir notificaciones sobre la creación de una nueva carpeta o mensaje.
    
 _fnevObjectCopied_
  
> Se registra para recibir notificaciones sobre una carpeta o un mensaje que se está copiando.
    
 _fnevObjectDeleted_
  
> Se registra para recibir notificaciones sobre una carpeta o un mensaje que se va a eliminar.
    
 _fnevObjectModified_
  
> Se registra para recibir notificaciones sobre una carpeta o un mensaje que se está modificando.
    
 _fnevObjectMoved_
  
> Se registra para recibir notificaciones sobre una carpeta o un mensaje que se está trasladando.
    
 _fnevSearchComplete_
  
> Se registra para recibir notificaciones sobre la finalización de una operación de búsqueda.
    
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso ya debe haber sido asignado.
    
 _lpulConnection_
  
> [salida] Puntero a un número distinto de cero que representa la conexión entre el objeto receptor de aviso del autor de la llamada y la sesión. 
    
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso ya debe haber sido asignado. 
    
 _lpulConnection_
  
> [salida] Puntero a un número de conexión distinto de cero que representa la conexión entre el objeto receptor de aviso del autor de la llamada y el almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se ha realizado correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor del almacén de mensajes no admite el registro de notificaciones a través del almacén de mensajes.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::Advise** establece una conexión entre el objeto receptor de avisos del autor de la llamada y el almacén de mensajes o un objeto del almacén de mensajes. Esta conexión se usa para enviar notificaciones al receptor de avisos cuando uno o más eventos, como se especifica en el parámetro  _ulEventMask,_ se producen en el objeto de origen de aviso. Cuando el  _parámetro lpEntryID_ apunta a un identificador de entrada válido, el origen de aviso es el objeto identificado por este identificador de entrada. Cuando  _lpEntryID_ es NULL, el origen del aviso es el almacén de mensajes. 
  
Para enviar una notificación, el proveedor del almacén de mensajes o MAPI llama al método [IMAPIAdviseSink::OnNotify del](imapiadvisesink-onnotify.md) receptor de avisos registrado. Uno de los parámetros de **OnNotify**, una estructura de notificación, contiene información que describe el evento específico.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir la notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de compatibilidad para ayudar a los proveedores de servicios a implementar la notificación: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport::Notify](imapisupport-notify.md). Si opta por usar los métodos de soporte de MAPI, llame a **Subscribe** cuando se llame al método **Advise** y libere el puntero _lpAdviseSink._ 
  
Si opta por admitir la notificación usted mismo, llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del receptor de avisos representado por el parámetro  _lpAdviseSink_ para guardar una copia de este puntero. Mantenga esta copia hasta que se llame al [método IMsgStore::Unadvise](imsgstore-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo admita la notificación, asigne un número de conexión distinto de cero al registro de notificación y retírlo en el _parámetro lpulConnection._ No libere este número de conexión hasta que se haya llamado a **Unadvise** y se haya completado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** también puede producirse en cualquier subproceso en cualquier momento. Si debe estar seguro de que las notificaciones se producen solo en un momento determinado en un subproceso determinado, llame a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para generar el objeto receptor de aviso que pase a **Advise**. 
  
Una vez que se haya realizado correctamente una llamada a **Advise** y antes de llamar a **Unadvise** para cancelar el registro, esté preparado para que el objeto receptor de aviso se liberará. Debe liberar el objeto receptor de avisos después de que **advise** vuelva, a menos que tenga un uso específico a largo plazo para él. 
  
Para obtener más información acerca del proceso de notificación, vea [Notificación de eventos en MAPI.](event-notification-in-mapi.md) 
  
Para obtener más información acerca del control de notificaciones, consulta [Control de notificaciones.](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa el **método IMsgStore::Advise** para registrar notificaciones en todo el almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Consulte también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

