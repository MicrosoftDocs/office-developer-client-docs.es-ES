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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406279"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un cliente o proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.
  
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
  
> [in] Puntero al identificador de entrada del contenedor de la libreta de direcciones, el usuario de mensajería o la lista de distribución que generará una notificación cuando se produzca un cambio del tipo o los tipos descritos en el parámetro _ulEventMask._ 
    
 _ulEventMask_
  
> [in] Uno o varios eventos de notificación que el autor de la llamada está registrando para recibir. Cada evento está asociado a una estructura de notificación determinada que contiene información sobre el cambio que se ha producido. En la tabla siguiente se enumeran los valores válidos  _para ulEventMask_ y sus estructuras correspondientes. 
    
|**Evento Notification**|**Estructura correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Puntero al objeto receptor advise al que se llamará cuando se produzca el evento para el que se ha solicitado la notificación.
    
 _lpulConnection_
  
> [salida] Puntero a un número de conexión distinto de cero que representa el registro de notificaciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación se ha realizado correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El proveedor de la libreta de direcciones responsable del identificador de entrada pasado en  _lpEntryID_ no pudo registrar una notificación para la entrada correspondiente. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de libreta de direcciones responsable del objeto identificado por el identificador de entrada pasado en el  _parámetro lpEntryID_ no admite la notificación. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada pasado en  _lpEntryID_ no puede ser manipulado por ninguno de los proveedores de libreta de direcciones en el perfil. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman **al método Advise** para registrarse para un tipo o tipo concreto de notificación en una entrada de libreta de direcciones. Los tipos de notificación se indican mediante la máscara de evento pasada con el _parámetro ulEventMask._ 
  
MAPI reenvía esta llamada **Advise** al proveedor de libreta de direcciones responsable de la entrada, tal como indica el identificador de entrada en el _parámetro lpEntryID._ El proveedor de libreta de direcciones controla el registro en sí o llama al método de soporte [técnico, IMAPISupport::Subscribe](imapisupport-subscribe.md), para solicitar a MAPI que registre al autor de la llamada. Se devuelve un número de conexión distinto de cero para representar el registro correcto.
  
Siempre que se produce un cambio en la entrada del tipo indicado por el registro de notificaciones, el proveedor de libreta de direcciones llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor advise especificado en el parámetro _lpAdviseSink._ El **método OnNotify** incluye una [estructura NOTIFICATION](notification.md) como un parámetro de entrada que contiene datos para describir el evento. 
  
Según el proveedor de libreta de direcciones, la llamada a **OnNotify** puede producirse inmediatamente después del cambio en el objeto registrado o en un momento posterior. En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso. Los clientes pueden solicitar que estas notificaciones se produzcan en un subproceso determinado llamando a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto de receptor de notificaciones que se pasa a **Advise**. 
  
Dado que un proveedor de libreta de direcciones puede liberar el objeto de receptor de notificaciones pasado por los clientes en cualquier momento después de la finalización correcta de la llamada **advise** y antes de una llamada [IAddrBook::Unadvise](iaddrbook-unadvise.md) para cancelar la notificación, los clientes deben liberar sus objetos receptores de aviso cuando **advise** devuelve. 
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

