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
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817109"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Hace referencia a**: Outlook 
  
Registra el autor de la llamada para recibir notificaciones de los eventos que afectan a un contenedor, usuario o lista de distribución de mensajería.
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto sobre el que se deben generar notificaciones.
    
 _ulEventMask_
  
> [entrada] Una máscara de bits de valores que se indican los tipos de eventos de notificación que el autor de la llamada está interesado en y se debe incluir en el registro. Hay una estructura de [notificación](notification.md) correspondiente asociada a cada tipo de evento que contiene información sobre el evento. En la siguiente tabla se enumera los valores válidos para el parámetro _ulEventMask_ y las estructuras de asociado a cada valor. 
    
|**Tipo de evento de notificación**|**Estructura de **notificación** correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise para recibir las notificaciones posteriores.
    
 _lpulConnection_
  
> [out] Un puntero a un valor distinto de cero que representa el registro de la notificación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación el registro se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El identificador de entrada que se pasa en el parámetro _lpEntryID_ no está en el formato adecuado. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de la libreta de direcciones no admite la notificación, posiblemente porque no permite que se realicen cambios en sus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de la libreta de direcciones no puede controlar el identificador de entrada que se pasó _lpEntryID_.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **IABLogon::Advise** para registrar el autor de la llamada para recibir una notificación cuando se produce un cambio a un objeto en uno de sus contenedores. Los autores de llamadas pueden registrarse para notificaciones en relación con los usuarios de mensajería, las listas de distribución o contenedores todo. 
  
Los clientes normalmente llaman al método de [IAddrBook::Advise](iaddrbook-advise.md) para registrar para las notificaciones de la libreta de direcciones. MAPI, a continuación, llama el método **Advise** del proveedor de libreta de direcciones que se encarga del objeto representado por el identificador de entrada en _lpEntryID_.
  
Cuando se produce un cambio en el objeto del tipo representado en _ulEventMask_indicado, se realiza una llamada al método **OnNotify** del receptor de notificaciones que señala _lpAdviseSink_. Datos que se pasan en la estructura de **notificación** a la rutina de **OnNotify** describen el evento. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede admitir notificación con o sin ayuda de MAPI. MAPI tiene tres métodos del objeto de soporte técnico para ayudar a los proveedores de servicios de implementar la notificación de:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Si decide utilizar los métodos de soporte técnico MAPI, llamar a **Subscribe** cuando se llame al método **Advise** y liberar el puntero _lpAdviseSink_ . 
  
Si decide admitir la notificación usted mismo, llame al método **AddRef** del receptor de notificaciones representado por el parámetro _lpAdviseSink_ para mantener una copia de este puntero. Mantener esta copia hasta que se llama al método [IABLogon::Unadvise](iablogon-unadvise.md) para cancelar el registro. 
  
Independientemente de cómo se admite la notificación, asigne a un número distinto de cero de conexión para el registro de la notificación y devolver en el parámetro _lpulConnection_ . No número de versión de esta conexión hasta que se ha llamado al método **Unadvise** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El puntero de receptor advise que se pasa en el parámetro _lpAdviseSink_ a **Advise** puede apuntar a un objeto que haya creado o que ha creado MAPI a través de la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Es posible que desee usar **HrThisThreadAdviseSink** si desea admite varios subprocesos de ejecución y asegúrese de que las llamadas posteriores al método **OnNotify** se producen en un momento adecuado en un subproceso adecuado. 
  
Esté preparado para que su objeto de receptor advise liberarse en cualquier momento después de la llamada a **Advise** y antes de la llamada a **Unadvise**. Por lo tanto, debe liberar su objeto de receptor advise después **Advise** devuelve, a menos que tengan un uso específico a largo plazo para él. 
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). Para obtener información acerca de cómo usar los métodos **IMAPISupport** para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md). Para obtener más información acerca de subprocesamiento múltiple y MAPI, vea [subprocesamiento en MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

