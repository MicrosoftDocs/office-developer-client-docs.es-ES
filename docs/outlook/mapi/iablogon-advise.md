---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338580"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra el autor de la llamada para recibir una notificación de los eventos especificados que afectan a un contenedor, un usuario de mensajería o una lista de distribución.
  
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
  
> a Número de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del objeto sobre el que se deben generar las notificaciones.
    
 _ulEventMask_
  
> a Máscara de tipo de valores que indican los tipos de eventos de notificación en los que está interesado el autor de la llamada y deben incluirse en el registro. Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. En la siguiente tabla se enumeran los valores válidos para el parámetro _ulEventMask_ y las estructuras asociadas con cada valor. 
    
|**Tipo de evento de notificación**|**Estructura de **notificación** correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> a Un puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores.
    
 _lpulConnection_
  
> contempla Un puntero a un valor distinto de cero que representa el registro de la notificación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada pasado en el parámetro _lpEntryID_ no tiene el formato adecuado. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de la libreta de direcciones no admite la notificación, posiblemente porque no permite que se realicen cambios en sus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de la libreta de direcciones no puede controlar el identificador de entrada pasado en _lpEntryID_.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **IABLogon:: Advise** para registrar que el autor de la llamada recibirá una notificación cuando se produzca un cambio en un objeto de uno de sus contenedores. Los autores de llamadas pueden registrarse en las notificaciones sobre los usuarios de mensajería, las listas de distribución o los contenedores completos. 
  
Los clientes suelen llamar al método [IAddrBook:: Advise](iaddrbook-advise.md) para registrarse en las notificaciones de la libreta de direcciones. MAPI, a continuación **** , llama al método Advise del proveedor de la libreta de direcciones que es responsable del objeto representado por el identificador de entrada en _lpEntryID_.
  
Cuando se produce un cambio en el objeto indicado del tipo representado en _ulEventMask_, se realiza una llamada al método **BENOTIFY** del receptor de notificaciones apuntado por _lpAdviseSink_. Los datos que se pasan en la estructura de **notificación** a la rutina de **Notify** describen el evento. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede admitir la notificación con o sin ayuda de MAPI. MAPI tiene tres métodos de objeto de soporte para ayudar a los proveedores de servicios a implementar la notificación:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si decide usar los métodos de compatibilidad con MAPI, llame a **subscribe** cuando se llame al método Advise y suelte el puntero _lpAdviseSink_ . **** 
  
Si opta por admitir la notificación usted mismo, llame al método **AddRef** del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para conservar una copia de este puntero. Mantenga esta copia hasta que se llame al método [IABLogon:: Unadvise](iablogon-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo se admita la notificación, asigne un número de conexión distinto de cero al registro de notificaciones y devuelva el parámetro _lpulConnection_ . No libere este número de conexión hasta que se haya llamado al método **Unadvise** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El puntero para avisar al receptor que se pasa en el parámetro _lpAdviseSink_ a Advise puede apuntar a un objeto que haya creado o que haya creado MAPI mediante la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . **** Es posible que desee usar **HrThisThreadAdviseSink** si admite varios subprocesos de ejecución y desea asegurarse de que las llamadas posteriores al método de **Notify** se produzcan en el momento adecuado en un subproceso adecuado. 
  
Esté preparado para que el objeto receptor de notificaciones se publique en cualquier momento después de su llamada a adVise y antes de la llamada a Unadvise. **** **** Por lo tanto, debe liberar su objeto de notificación **** de notificaciones después de que se deVuelva Advise, a menos que tenga un uso específico a largo plazo. 
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). Para obtener información sobre cómo usar los métodos de **IMAPISupport** para admitir la notificación, consulte [support Event Notification](supporting-event-notification.md). Para obtener más información acerca del multiproceso y MAPI, vea el tema sobre el [procesamiento en MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

