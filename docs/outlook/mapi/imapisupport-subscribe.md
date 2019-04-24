---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328970"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un receptor de notificaciones para recibir notificaciones a través de MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _lpKey_
  
> a Un puntero a una clave de notificación que representa el objeto de origen Advise. El parámetro _lpKey_ no puede ser nulo. 
    
 _ulEventMask_
  
> a Máscara de valores que indican los tipos de eventos de notificación en los que está interesado el autor de la llamada y que deben incluirse en el registro. Los siguientes valores son válidos:
    
 _fnevCriticalError_
  
> Registra las notificaciones sobre errores graves, como memoria insuficiente.
    
 _fnevExtended_
  
> Registra las notificaciones sobre eventos específicos de la libreta de direcciones o del proveedor de almacenamiento de mensajes en particular.
    
 _fnevNewMail_
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
 _fnevObjectCopied_
  
> Registra notificaciones sobre un objeto que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra notificaciones sobre un objeto que se está eliminando.
    
 _fnevObjectModified_
  
> Registra notificaciones sobre un objeto que se está modificando.
    
 _fnevObjectMoved_
  
> Registra notificaciones sobre un objeto que se está moviendo.
    
 _fnevSearchComplete_
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se produce la notificación. Se puede establecer la siguiente marca:
    
NOTIFY_SYNC 
  
> Cuando el autor de la llamada llama al método [IMAPISupport:: Notify](imapisupport-notify.md) para generar notificaciones para este receptor de notificaciones, **Notify** debe realizar todas las llamadas necesarias para informar a los receptores antes de devolverse. Si no se establece esta marca, la notificación es asincrónica y las devoluciones de llamada se ponen en cola para los procesos que se han suscrito e iniciado cuando dichos procesos controlan la CPU. 
    
 _lpAdviseSink_
  
> a Un puntero a un objeto de receptor de notificaciones. 
    
 _lpulConnection_
  
> contempla Un puntero a un número de conexión distinto de cero que representa el registro.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: subscribe** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios llaman a **subscribe** desde **** uno de sus métodos de notificación para permitir que MAPI administre las notificaciones. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para utilizar los métodos de compatibilidad con MAPI para la notificación, cree una clave para el origen del aviso el objeto sobre el que se deben generar las notificaciones. El valor de la clave debe ser único y se debe volver a generar fácilmente cada vez que cambie el objeto. 
  
MAPI usa la clave de notificación para buscar cualquier función de devolución de llamada registrada a través de la función [HrAllocAdviseSink](hrallocadvisesink.md) para el origen de Advise correspondiente. Pase esta clave a **IMAPISupport:: Notify** siempre que necesite generar una notificación para el origen Advise correspondiente. 
  
La marca NOTIFY_SYNC afecta al funcionamiento de llamadas posteriores para **notificar**. Cuando se establece NOTIFY_SYNC, **Notify** no devuelve ningún valor hasta que haya finalizado el envío de todas las notificaciones necesarias. Cuando no se establece NOTIFY_SYNC, **Notify** funciona de forma asincrónica, posiblemente devolviendo antes de que se hayan enviado todas las notificaciones. 
  
## <a name="see-also"></a>Vea también



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

