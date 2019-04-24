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
  
Registra un objeto con un proveedor de almacenamiento de mensajes para notificaciones sobre cambios en el almacén de mensajes. A continuación, el almacén de mensajes enviará notificaciones sobre los cambios en el objeto registrado.
  
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
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del objeto sobre el que se deben generar las notificaciones. Este objeto puede ser una carpeta, un mensaje o cualquier otro objeto en el almacén de mensajes. Como alternativa, si MAPI establece el parámetro _cbEntryID_ en 0 y pasa **null** para _lpEntryID_, el receptor de notificaciones proporcionará notificaciones sobre los cambios en el almacén de mensajes completo.
    
 _ulEventMask_
  
> a Una máscara de evento de los tipos de eventos de notificación que se producen para el objeto sobre el que MAPI generará notificaciones. La máscara filtra casos específicos. Cada tipo de evento tiene una estructura asociada que contiene información adicional sobre el evento. En la siguiente tabla se enumeran los tipos de eventos posibles junto con sus estructuras correspondientes.
    
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
  
> a Un puntero a un objeto receptor de notificaciones al que se llama cuando se produce un evento para el objeto Session sobre el que se ha solicitado notificación. Este objeto de receptor de notificaciones ya debe existir.
    
 _lpulConnection_
  
> contempla Un puntero a una variable que, tras una devolución correcta, contiene el número de conexión para el registro de la notificación. El número de conexión debe ser distinto de cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no es compatible con MAPI o con uno o más proveedores de servicios.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacenamiento de mensajes implementan el método **IMSLogon:: Advise** para registrar un objeto para las devoluciones de llamada de notificación. Siempre que se produce un cambio en el objeto indicado, el proveedor comprueba el bit de máscara de evento que se ha establecido en el parámetro _ulEventMask_ y, por lo tanto, el tipo de cambio que se ha producido. Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto de notificación de aviso indicado por el parámetro _lpAdviseSink_ para informar del evento. Los datos que se pasan en la estructura de notificación a la rutina de **Notify** describen el evento. 
  
La llamada a la **Notify** puede producirse durante la llamada que cambia el objeto o en cualquier momento posterior. En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** puede producirse en cualquier subproceso. Para controlar de forma segura una llamada a **BENOTIFY** que puede producirse en un momento inoportuno, una aplicación cliente debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para proporcionar notificaciones, el proveedor de almacenamiento de mensajes que **** implementa Advise necesita mantener una copia del puntero al objeto receptor de notificaciones de _lpAdviseSink_ ; para ello, el proveedor llama al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para que el receptor de notificaciones mantenga su puntero de objeto hasta que se cancele el registro de la notificación con una llamada al método [IMSLogon:: Unadvise](imslogon-unadvise.md) . La **** implementación de Advise debe asignar un número de conexión al registro de notificaciones y llamar a **AddRef** en este número de conexión antes de devolverlo en el parámetro _lpulConnection_ . Los proveedores de servicios pueden liberar el objeto del receptor de notificaciones antes de que se cancele el registro, pero no deben liberar el número de conexión hasta que se haya llamado a **Unadvise** . 
  
Después de llamar a **Advise** correctamente y antes **** de llamar a Unadvise, los proveedores deben estar preparados para que se pueda liberar el objeto receptor de notificaciones. Por lo tanto, un proveedor debe liberar su objeto Return Sink después de que se devuelva **Advise** , a menos que tenga un uso a largo plazo específico. 
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notificaci�n](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

