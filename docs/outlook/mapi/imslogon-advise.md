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
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317314"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un objeto con un proveedor de almacén de mensajes para recibir notificaciones sobre los cambios en el almacén de mensajes. A continuación, el almacén de mensajes enviará notificaciones sobre los cambios realizados en el objeto registrado.
  
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
  
> [in] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del objeto sobre qué notificaciones se deben generar. Este objeto puede ser una carpeta, un mensaje o cualquier otro objeto del almacén de mensajes. Como alternativa, si MAPI establece el  _parámetro cbEntryID_ en 0 y pasa **null** para  _lpEntryID,_ el receptor de notificaciones proporciona notificaciones sobre los cambios en todo el almacén de mensajes.
    
 _ulEventMask_
  
> [in] Máscara de evento de los tipos de eventos de notificación que se producen para el objeto sobre el que MAPI generará notificaciones. La máscara filtra casos específicos. Cada tipo de evento tiene una estructura asociada que contiene información adicional sobre el evento. En la tabla siguiente se enumeran los tipos de eventos posibles junto con sus estructuras correspondientes.
    
|**Tipo de evento Notification**|**Estructura correspondiente**|
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
  
> [in] Puntero a un objeto receptor de aviso al que se llamará cuando se produzca un evento para el objeto de sesión sobre el que se ha solicitado la notificación. Esto aconseja que el objeto receptor ya debe existir.
    
 _lpulConnection_
  
> [salida] Puntero a una variable que, tras una devolución correcta, contiene el número de conexión para el registro de notificación. El número de conexión debe ser distinto de cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> Mapi o uno o varios proveedores de servicios no admiten la operación.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::Advise** para registrar un objeto para las devoluciones de llamada de notificación. Siempre que se produce un cambio en el objeto indicado, el proveedor comprueba qué bit de máscara de evento se estableció en el parámetro  _ulEventMask_ y, por lo tanto, qué tipo de cambio se produjo. Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor advise indicado por el parámetro  _lpAdviseSink_ para notificar el evento. Los datos pasados en la estructura de notificación a la **rutina OnNotify** describen el evento. 
  
La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto o en cualquier momento posterior. En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso. Para controlar de forma segura una llamada a **OnNotify** que puede ocurrir en un momento inoportuna, una aplicación cliente debe usar la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Para proporcionar notificaciones, el proveedor del almacén de mensajes que implementa **Advise** debe mantener una copia del puntero al objeto receptor _lpAdviseSink_ advise; para ello, el proveedor llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para que el receptor de notificaciones mantenga su puntero de objeto hasta que se cancele el registro de notificaciones con una llamada al método [IMSLogon::Unadvise.](imslogon-unadvise.md) La **implementación advise** debe asignar un número de conexión al registro de notificación y llamar a **AddRef** en este número de conexión antes de devolverlo en el _parámetro lpulConnection._ Los proveedores de servicios pueden liberar el objeto receptor de aviso antes de cancelar el registro, pero no deben liberar el número de conexión hasta que se llame **a Unadvise.** 
  
Después de que una llamada **a Advise** se haya realizado correctamente y antes de llamar a **Unadvise,** los proveedores deben estar preparados para que el objeto de receptor de aviso se liberará. Por lo tanto, un proveedor debe liberar el objeto de receptor advise después de **que advise** devuelva, a menos que tenga un uso específico a largo plazo para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

