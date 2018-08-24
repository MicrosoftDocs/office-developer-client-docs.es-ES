---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9cd0442a715fb5441ab8efefb9574f09f2e2c1ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587862"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Registra un objeto con un proveedor de almacén de mensajes para las notificaciones sobre cambios en el almacén de mensajes. El almacén de mensajes, a continuación, enviará las notificaciones sobre cambios en el objeto registrado.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto sobre el que se deben generar notificaciones. Este objeto puede ser una carpeta, un mensaje o cualquier otro objeto en el almacén de mensajes. Como alternativa, si MAPI establece el parámetro _cbEntryID_ en 0 y pasa **null** para _lpEntryID_, el receptor de notificaciones proporciona notificaciones sobre cambios en el almacén de todo el mensaje.
    
 _ulEventMask_
  
> [entrada] Una máscara de eventos de los tipos de eventos de notificación que se producen para el objeto sobre qué MAPI generará notificaciones. La máscara de los filtros específicos de los casos. Cada tipo de evento tiene una estructura asociada que contiene información adicional sobre el evento. En la siguiente tabla enumera los tipos de evento posibles junto con las estructuras de sus correspondientes.
    
|**Tipo de evento de notificación**|**Estructura correspondiente**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise que se llama cuando se produce un evento para el objeto de sesión acerca de qué se ha solicitado la notificación. Este objeto de receptor advise ya debe existir.
    
 _lpulConnection_
  
> [out] Un puntero a una variable que, tras una devolución es correcta, contiene el número de conexión para el registro de notificación. El número de conexión debe ser distinto de cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no se admite por MAPI o por uno o más proveedores de servicio.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::Advise** para registrar un objeto para realizar devoluciones de llamadas de notificación. Cada vez que se produce un cambio en el objeto indicado, el proveedor comprueba qué bit de máscara de eventos se estableció en el parámetro _ulEventMask_ y, por lo tanto, ¿qué tipo de cambio se ha producido. Si un bit está establecido, el proveedor llama al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise indicado por el parámetro _lpAdviseSink_ para notificar el evento. Datos que se pasan en la estructura de notificación a la rutina de **OnNotify** describen el evento. 
  
La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto, o en cualquier momento posterior. En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso. Para administrar de forma segura una llamada a **OnNotify** que puede suceder en un momento inoportuno, una aplicación de cliente debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para proporcionar notificaciones, el proveedor de almacenamiento de mensajes que implementa las necesidades de **Advise** para mantener una copia del puntero a la _lpAdviseSink_ aviso objeto receptor; Para ello, el proveedor llama al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para el receptor de notificaciones mantener su puntero del objeto hasta que se cancele el registro de la notificación con una llamada al método [IMSLogon::Unadvise](imslogon-unadvise.md) . La implementación de **Advise** debe asignar a un número de conexión para el registro de la notificación y llamar a **AddRef** en este número de conexión antes de devolver en el parámetro _lpulConnection_ . Proveedores de servicios pueden liberar el objeto de receptor de advise antes de que se ha cancelado el registro, pero no debe liberar el número de conexión hasta que se ha llamado al **Unadvise** . 
  
Después de que se ha realizado correctamente una llamada a **Advise** y antes de que se ha llamado al **Unadvise** , es preciso preparar los proveedores para que el objeto de receptor advise que liberar. Por lo tanto, un proveedor debe liberar su objeto de receptor advise después **Advise** devuelve, a menos que tenga un uso a largo plazo específico para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

