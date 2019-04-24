---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334758"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un cliente o un proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.
  
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
  
> a Un puntero al identificador de entrada del contenedor de la libreta de direcciones, el usuario de mensajería o la lista de distribución que generarán una notificación cuando se produzca un cambio del tipo o de los tipos descritos en el parámetro _ulEventMask_ . 
    
 _ulEventMask_
  
> a Uno o más eventos de notificación que el autor de la llamada está registrando para recibirlos. Cada evento está asociado a una estructura de notificación determinada que contiene información sobre el cambio que se ha producido. En la siguiente tabla se enumeran los valores válidos para _ulEventMask_ y sus estructuras correspondientes. 
    
|**Evento de notificación**|**Estructura correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> a Un puntero al objeto del receptor de notificaciones al que se llamará cuando se produzca el evento para el que se ha solicitado notificación.
    
 _lpulConnection_
  
> contempla Un puntero a un número de conexión distinto de cero que representa el registro de la notificación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El proveedor de la libreta de direcciones responsable del identificador de entrada pasado en _lpEntryID_ no pudo registrar una notificación para la entrada correspondiente. 
    
MAPI_E_NO_SUPPORT 
  
> La notificación no es compatible con el proveedor de la libreta de direcciones responsable del objeto identificado por el identificador de entrada pasado en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> No se puede controlar el identificador de entrada que se ha pasado en _lpEntryID_ por ninguno de los proveedores de la libreta de direcciones en el perfil. 
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de **** servicios llaman al método Advise para registrar un tipo determinado o tipos de notificación en una entrada de la libreta de direcciones. Los tipos de notificación se indican mediante la máscara de eventos que se pasa con el parámetro _ulEventMask_ . 
  
MAPI reenvía **** esta llamada a Adviser al proveedor de la libreta de direcciones que es responsable de la entrada indicada por el identificador de entrada en el parámetro _lpEntryID_ . El proveedor de la libreta de direcciones administra el registro en sí o llama al método support, [IMAPISupport:: subscribe](imapisupport-subscribe.md), para pedir a MAPI que registre al autor de la llamada. Se devuelve un número de conexión distinto de cero para representar el registro correcto.
  
Siempre que se produce un cambio en la entrada del tipo indicado por el registro de la notificación, el proveedor de la libreta de direcciones llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto del receptor de notificaciones especificado en el parámetro _lpAdviseSink_ . El método **NotifyTo** incluye una estructura de [notificación](notification.md) como un parámetro de entrada que contiene datos para describir el evento. 
  
Según el proveedor de la libreta de direcciones, la llamada a la **Notify** puede producirse inmediatamente después del cambio en el objeto registrado o en un momento posterior. En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** puede producirse en cualquier subproceso. Los clientes pueden solicitar que estas notificaciones se produzcan en un subproceso determinado llamando a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto de notificación de notificaciones que se pasa a Advise. **** 
  
Debido a que un proveedor de libretas de direcciones puede liberar el objeto de notificación de notificaciones que pasan los clientes en **** cualquier momento después de la finalización correcta de la llamada a Advise y antes de una llamada a [IAddrBook:: Unadvise](iaddrbook-unadvise.md) para cancelar la notificación, los clientes deben liberar sus objetos de notificación de **** notificaciones cuando se devuelve Advise. 
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

