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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418816"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un objeto de receptor de notificaciones para recibir una notificación de eventos especificados que afectan a la tabla.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulEventMask_
  
> [in] Valor que indica el tipo de evento que generará la notificación. Solo el siguiente valor es válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso debe haber sido ya asignado.
    
 _lpulConnection_
  
> [salida] Puntero a un valor distinto de cero que representa el registro de notificaciones correcto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación se completó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La implementación de la tabla no admite cambios en sus filas y columnas o no admite notificaciones.
    
## <a name="remarks"></a>Comentarios

Use el **método IMAPITable::Advise** para registrar un objeto table implementado en el proveedor para las devoluciones de llamada de notificación. Siempre que se produce un cambio en el objeto table, el proveedor comprueba qué bits de máscara de evento se estableció en el parámetro  _ulEventMask_ y, por lo tanto, qué tipo de cambio se produjo. Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor advise indicado por el parámetro  _lpAdviseSink_ para notificar el evento. Los datos pasados en la estructura de notificación a la **rutina OnNotify** describen el evento. 
  
La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto o en cualquier momento siguiente. En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso. Para una forma de convertir una llamada a **OnNotify** que puede ocurrir en un momento inoportuna en uno que sea más seguro de controlar, un proveedor debe usar la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Para proporcionar notificaciones, el proveedor que implementa **Advise** debe mantener una copia del puntero al objeto receptor _lpAdviseSink_ advise; para ello, llama al método **IUnknown::AddRef** para que el receptor de notificaciones mantenga su puntero de objeto hasta que se cancele el registro de notificaciones con una llamada al método [IMAPITable::Unadvise.](imapitable-unadvise.md) La **implementación advise** debe asignar un número de conexión al registro de notificación y llamar a **AddRef** en este número de conexión antes de devolverlo en el _parámetro lpulConnection._ Los proveedores de servicios pueden liberar el objeto receptor de aviso antes de cancelar el registro, pero no deben liberar el número de conexión hasta que se llame a ** Unadvise **. 
  
Después de que una llamada a **Advise** se haya realizado correctamente y antes de que se haya llamado a ** Unadvise ** , los clientes deben estar preparados para que el objeto receptor de aviso se liberará. Por lo tanto, un cliente debe liberar su objeto de receptor advise después de **que Advise** devuelva a menos que tenga un uso específico a largo plazo para él. 
  
Debido al comportamiento asincrónico de la notificación, las implementaciones que cambian la configuración de columna de tabla pueden recibir notificaciones con información organizada en un orden de columna anterior. Por ejemplo, es posible que se devuelva una fila de tabla para un mensaje que acaba de eliminarse del contenedor. Dicha notificación se envía cuando se ha realizado el cambio de configuración de columna y se ha enviado información sobre ella, pero la vista de tabla de notificación aún no se ha actualizado con esa información.
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). Para obtener información específica acerca de la notificación de tabla, vea [About Table Notifications](about-table-notifications.md). Para obtener información acerca del uso de los **métodos IMAPISupport** para admitir notificaciones, vea [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI usa el **método IMAPITable::Advise** para registrar las notificaciones para permitir que la vista de tabla permanezca actualizada.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

