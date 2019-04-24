---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329025"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un objeto receptor de notificaciones para recibir una notificación de los eventos especificados que afectan a la tabla.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulEventMask_
  
> a Valor que indica el tipo de evento que va a generar la notificación. Solo el siguiente valor es válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> a Puntero a un objeto receptor de notificaciones para recibir las notificaciones posteriores. Este objeto de receptor de notificaciones debe haber sido asignado ya.
    
 _lpulConnection_
  
> contempla Puntero a un valor distinto de cero que representa el registro de notificación correcto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se completó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La implementación de la tabla no admite cambios en sus filas y columnas, o no admite la notificación.
    
## <a name="remarks"></a>Comentarios

Use el método **IMAPITable:: Advise** para registrar un objeto Table implementado en el proveedor para las devoluciones de llamada de notificación. Siempre que se produce un cambio en el objeto Table, el proveedor comprueba el bit de máscara de evento que se ha establecido en el parámetro _ulEventMask_ y, por tanto, el tipo de cambio que se ha producido. Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto de notificación de aviso indicado por el parámetro _lpAdviseSink_ para informar del evento. Los datos que se pasan en la estructura de notificación a la rutina de **Notify** describen el evento. 
  
La llamada a la **Notify** puede producirse durante la llamada que cambia el objeto, o en cualquier momento siguiente. En los sistemas que admiten varios subprocesos de ejecución, la llamada a **BENOTIFY** puede producirse en cualquier subproceso. Para una forma de convertir una llamada a **BENOTIFY** que puede ocurrir en un momento inoportuno en uno que sea más seguro de administrar, un proveedor debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para proporcionar notificaciones, el proveedor que **** implementa Advise necesita mantener una copia del puntero al objeto receptor de notificaciones de _lpAdviseSink_ ; para ello, llama al método **IUnknown:: AddRef** para que el receptor de notificaciones mantenga su puntero de objeto hasta que se cancele el registro de la notificación con una llamada al método [IMAPITable:: Unadvise](imapitable-unadvise.md) . La **** implementación de Advise debe asignar un número de conexión al registro de notificaciones y llamar a **AddRef** en este número de conexión antes de devolverlo en el parámetro _lpulConnection_ . Los proveedores de servicios pueden liberar el objeto de receptor de notificaciones antes de que se cancele el registro, pero no deben liberar el número de conexión hasta que se haya llamado a * * sin informar de * *. 
  
Después de llamar a **Advise** correctamente y antes de llamar a * *, los clientes deben estar preparados para que se pueda liberar el objeto receptor de notificaciones. Por lo tanto, un cliente debe liberar su objeto **** reconocer el receptor después de que se deVuelva Advise, a menos que tenga un uso específico a largo plazo. 
  
Debido al comportamiento asincrónico de la notificación, las implementaciones que cambian la configuración de la columna de tabla pueden recibir notificaciones con información organizada en un orden de columna anterior. Por ejemplo, es posible que se devuelva una fila de tabla para un mensaje que se acaba de eliminar del contenedor. Una notificación de este tipo se envía cuando se ha realizado el cambio de configuración de columna y se ha enviado la información sobre el mismo, pero aún no se ha actualizado la vista de tabla de notificaciones con esa información.
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). Para obtener información específica acerca de las notificaciones de tabla, consulte [about table Notifications](about-table-notifications.md). Para obtener información acerca del uso de los métodos de **IMAPISupport** para admitir la notificación, consulte [admitir notificaciones de eventos](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContestTableListCtrl:: Notificationon  <br/> |MFCMAPI usa el método **IMAPITable:: Advise** para registrarse en las notificaciones para permitir que la vista de tabla esté actualizada.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

