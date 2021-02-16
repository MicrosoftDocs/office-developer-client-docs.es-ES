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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419929"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un receptor de avisos para recibir notificaciones a través de MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parámetros

 _lpKey_
  
> [entrada] Puntero a una clave de notificación que representa el objeto de origen de aviso. El  _parámetro lpKey_ no puede ser NULL. 
    
 _ulEventMask_
  
> [entrada] Máscara de valores que indica los tipos de eventos de notificación que el autor de la llamada está interesado y debe incluirse en el registro. Los siguientes valores son válidos:
    
 _fnevCriticalError_
  
> Registra las notificaciones sobre errores graves, como la memoria insuficiente.
    
 _fnevExtended_
  
> Se registra para notificaciones sobre eventos específicos del proveedor de libreta de direcciones o almacén de mensajes en particular.
    
 _fnevNewMail_
  
> Se registra para recibir notificaciones sobre la llegada de nuevos mensajes. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
 _fnevObjectCopied_
  
> Registra las notificaciones sobre un objeto que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra las notificaciones sobre un objeto que se va a eliminar.
    
 _fnevObjectModified_
  
> Registra notificaciones sobre un objeto que se está modificando.
    
 _fnevObjectMoved_
  
> Registra las notificaciones sobre un objeto que se está trasladando.
    
 _fnevSearchComplete_
  
> Se registra para recibir notificaciones sobre la finalización de una operación de búsqueda.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se produce la notificación. Se puede establecer la siguiente marca:
    
NOTIFY_SYNC 
  
> Cuando el autor de la llamada llama al método [IMAPISupport::Notify](imapisupport-notify.md) para generar notificaciones para este receptor de aviso, **notify** debe realizar todas las llamadas necesarias para avisar a los receptores antes de volver. Si no se establece esta marca, la notificación es asincrónica y las devoluciones de llamada se ponen en cola en los procesos que se han suscrito e iniciado cuando esos procesos obtienen el control de la CPU. 
    
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto receptor de aviso. 
    
 _lpulConnection_
  
> [salida] Puntero a un número de conexión distinto de cero que representa el registro.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::Subscribe** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios **llaman a Subscribe** desde uno de sus **métodos Advise** para permitir que MAPI administre las notificaciones. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para usar los métodos de soporte de MAPI para la notificación, cree una clave para el origen del aviso el objeto sobre qué notificaciones se deben generar. El valor de la clave debe ser único y debe regenerarse fácilmente cada vez que cambie el objeto. 
  
MAPI usa la clave de notificación para buscar cualquier función de devolución de llamada registrada a través de la función [HrAllocAdviseSink](hrallocadvisesink.md) para el origen de aviso correspondiente. Pase esta clave a **IMAPISupport::Notify** siempre que necesite generar una notificación para el origen de aviso correspondiente. 
  
El NOTIFY_SYNC marca afecta al funcionamiento de las llamadas subsiguientes a **Notify**. Cuando estableces NOTIFY_SYNC, **Notify** no vuelve hasta que termina de enviar todas las notificaciones necesarias. Cuando no estableces la NOTIFY_SYNC, **notify** funciona de forma asincrónica, posiblemente devolviendo antes de que se hayan enviado todas las notificaciones. 
  
## <a name="see-also"></a>Consulte también



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

