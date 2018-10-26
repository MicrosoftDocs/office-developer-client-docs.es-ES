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
ms.openlocfilehash: beeca6ba958c38e12fba7dbc2884c81e58bdf3c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590123"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _lpKey_
  
> [entrada] Un puntero a una clave de notificación que representa el objeto de origen advise. El parámetro _lpKey_ no puede ser NULL. 
    
 _ulEventMask_
  
> [entrada] Una máscara de valores que se indican los tipos de eventos de notificación que el autor de la llamada está interesado en y se debe incluir en el registro. Los valores siguientes son válidos:
    
 _fnevCriticalError_
  
> Registra las notificaciones acerca de los errores graves, como memoria insuficiente.
    
 _fnevExtended_
  
> Proveedor de almacén de registros para las notificaciones sobre los eventos específicos de la libreta de direcciones determinada o mensaje.
    
 _fnevNewMail_
  
> Registra las notificaciones sobre la llegada de mensajes nuevos. 
    
 _fnevObjectCreated_
  
> Registra las notificaciones sobre la creación de un nuevo objeto.
    
 _fnevObjectCopied_
  
> Registra las notificaciones sobre un objeto que se está copiando.
    
 _fnevObjectDeleted_
  
> Registra las notificaciones sobre un objeto que se va a eliminar.
    
 _fnevObjectModified_
  
> Registra las notificaciones sobre un objeto que se va a modificar.
    
 _fnevObjectMoved_
  
> Registra las notificaciones sobre un objeto que se va a mover.
    
 _fnevSearchComplete_
  
> Registra las notificaciones sobre la finalización de una operación de búsqueda.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se produce la notificación. Se puede establecer la marca siguiente:
    
NOTIFY_SYNC 
  
> Cuando el autor de la llamada, llama al método de [IMAPISupport::Notify](imapisupport-notify.md) para generar las notificaciones para este receptor de notificaciones, **Notify** debe realizar todas las llamadas necesarias para avisar a los receptores antes de devolverlo. Si no se establece este marcador, notificación es asincrónica y se ponen en cola devoluciones de llamada a los procesos que se han suscrito y se inicia cuando estos procesos obtienen el control de la CPU. 
    
 _lpAdviseSink_
  
> [entrada] Un puntero a un objeto de receptor advise. 
    
 _lpulConnection_
  
> [out] Un puntero a un número distinto de cero de conexión que representa el registro.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación el registro se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::Subscribe** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamar a **Subscribe** desde uno de sus métodos **Advise** para permitir MAPI administrar las notificaciones. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para usar los métodos de soporte técnico MAPI para la notificación, cree una clave para el origen de advise se debería generar el objeto acerca de las notificaciones. El valor de la clave debe ser único y debe ser fácilmente vuelve a generar cada vez que cambia el objeto. 
  
MAPI utiliza la clave de notificación para buscar todas las funciones de devolución de llamada registradas a través de la función [HrAllocAdviseSink](hrallocadvisesink.md) para el origen de advise correspondiente. Pase esta clave a **IMAPISupport::Notify** cada vez que se necesita generar una notificación para el origen de advise correspondiente. 
  
El indicador NOTIFY_SYNC afecta a la operación de las llamadas subsiguientes a **Notify**. Cuando se establece NOTIFY_SYNC, **Notificar** no devuelve hasta que ha terminado de enviar todas las notificaciones necesarias. Cuando no se establece NOTIFY_SYNC, **Notify** funciona de forma asincrónica, devolución, posiblemente, antes de que todas las notificaciones se han enviado. 
  
## <a name="see-also"></a>Vea también



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

