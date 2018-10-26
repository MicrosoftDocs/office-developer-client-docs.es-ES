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
ms.openlocfilehash: 43569b22cace7b2700d37ace49fd734b45fec73c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580883"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Registra un proveedor de servicio o cliente para recibir notificaciones sobre los cambios realizados en una o más entradas en la libreta de direcciones.
  
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
  
> [entrada] Un puntero al identificador de entrada del contenedor de libreta de direcciones, usuario o lista de distribución que genere una notificación cuando se produce un cambio del tipo o tipos que se describen en el parámetro _ulEventMask_ de mensajería. 
    
 _ulEventMask_
  
> [entrada] Uno o más eventos de notificación que el autor de la llamada se está registrando para recibir. Cada evento se asocia con una estructura de notificación en particular que contiene información sobre el cambio que se produjo. En la siguiente tabla se enumera los valores válidos para _ulEventMask_ y las estructuras de sus correspondientes. 
    
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
  
> [entrada] Un puntero al objeto receptor advise que se llama cuando se produce el evento para el que se ha solicitado la notificación.
    
 _lpulConnection_
  
> [out] Un puntero a un número distinto de cero de conexión que representa el registro de la notificación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación el registro se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID 
  
> El proveedor de libreta de direcciones responsable para el identificador de entrada que se pasan en _lpEntryID_ no pudo registrar una notificación de la entrada correspondiente. 
    
MAPI_E_NO_SUPPORT 
  
> Notificación no es compatible con el proveedor de libreta de direcciones responsable del objeto identificado por el identificador de entrada que se pasa en el parámetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada que se pasan en _lpEntryID_ no se puede controlar mediante cualquiera de los proveedores de la libreta de direcciones en el perfil. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llaman al método **Advise** se registre para un determinado tipo o tipos de notificación en una entrada de la libreta de direcciones. Los tipos de notificación se indican mediante la máscara de eventos pasada con el parámetro _ulEventMask_ . 
  
MAPI reenvía esta llamada **Advise** para el proveedor de libreta de direcciones que es responsable de la entrada indicada por el identificador de entrada en el parámetro _lpEntryID_ . El proveedor de la libreta de direcciones que administra el registro propio o que llama al método de soporte técnico, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para que solicite MAPI para registrar el autor de la llamada. Se devuelve un número de conexión distinto de cero para representar el registro correcto.
  
Cada vez que se produce un cambio a la entrada del tipo indicado por el registro de la notificación, en el proveedor de la libreta de direcciones se llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise especificado en el parámetro _lpAdviseSink_ . El método **OnNotify** incluye una estructura de [notificación](notification.md) como un parámetro de entrada que contiene los datos para describir el evento. 
  
Según el proveedor de la libreta de direcciones, la llamada a **OnNotify** puede ocurrir inmediatamente tras el cambio en el objeto registrado o en un momento posterior. En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso. Los clientes pueden solicitar que estas notificaciones se producen en un subproceso concreto mediante una llamada a la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear el objeto de receptor advise que se pasa al **Advise**. 
  
Debido a que un proveedor de la libreta de direcciones puede liberar el objeto de receptor advise que se pasan por los clientes en cualquier momento después de la finalización correcta de la **Advise** y antes de una [IAddrBook::Unadvise](iaddrbook-unadvise.md) de llamadas para cancelar la notificación, deben liberar los clientes los objetos del receptor advise cuando **Advise** devuelve. 
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notificaci�n](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

