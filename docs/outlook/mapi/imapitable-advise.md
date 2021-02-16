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
  
Registra un objeto receptor de aviso para recibir una notificación de eventos especificados que afectan a la tabla.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulEventMask_
  
> [entrada] Valor que indica el tipo de evento que generará la notificación. Solo el siguiente valor es válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto receptor de aviso para recibir las notificaciones posteriores. Este objeto receptor de aviso debe haber sido ya asignado.
    
 _lpulConnection_
  
> [salida] Puntero a un valor distinto de cero que representa el registro de notificaciones correcto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación se completó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La implementación de la tabla no admite cambios en sus filas y columnas o no admite notificaciones.
    
## <a name="remarks"></a>Comentarios

Use el **método IMAPITable::Advise** para registrar un objeto de tabla implementado en el proveedor para las devoluciones de llamada de notificaciones. Siempre que se produce un cambio en el objeto de tabla, el proveedor comprueba qué bit de máscara de evento se estableció en el parámetro  _ulEventMask_ y, por lo tanto, qué tipo de cambio se produjo. Si se establece un bit, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor de aviso indicado por el parámetro  _lpAdviseSink_ para notificar el evento. Los datos pasados en la estructura de notificación a **la rutina OnNotify** describen el evento. 
  
La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto o en cualquier momento siguiente. En sistemas que admiten varios subprocesos de ejecución, la llamada a **OnNotify** puede producirse en cualquier subproceso. Para obtener una forma de convertir una llamada a **OnNotify** que puede ocurrir en un momento inoportuna en uno que sea más seguro de controlar, un proveedor debe usar la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Para proporcionar notificaciones, el proveedor que implementa **Advise** debe conservar una copia del puntero al objeto receptor _lpAdviseSink;_ para ello, llama al método **IUnknown::AddRef** para que el receptor de avisos mantenga su puntero de objeto hasta que se cancele el registro de notificación con una llamada al método [IMAPITable::Unadvise.](imapitable-unadvise.md) La implementación de **Advise** debe asignar un número de conexión al registro de notificación y llamar a **AddRef** en este número de conexión antes de devolverlo en el _parámetro lpulConnection._ Los proveedores de servicios pueden liberar el objeto receptor de avisos antes de cancelar el registro, pero no deben liberar el número de conexión hasta que se haya llamado a ** Unadvise **. 
  
Una vez que se ha realizado correctamente una llamada a **Advise** y antes de llamar a ** Unadvise **, los clientes deben estar preparados para que se pueda liberar el objeto receptor de avisos. Por lo tanto, un cliente debe liberar el objeto receptor de avisos después de que **advise** vuelva, a menos que tenga un uso específico a largo plazo para él. 
  
Debido al comportamiento asincrónico de las notificaciones, las implementaciones que cambian la configuración de las columnas de la tabla pueden recibir notificaciones con información organizada en un orden de columna anterior. Por ejemplo, se puede devolver una fila de tabla para un mensaje que se acaba de eliminar del contenedor. Dicha notificación se envía cuando se ha realizado el cambio de configuración de columna y se ha enviado información sobre ella, pero la vista de tabla de notificación aún no se ha actualizado con esa información.
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md). Para obtener información específica acerca de la notificación de tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md). Para obtener información acerca del uso **de los métodos IMAPISupport** para admitir notificaciones, vea [Notificación de eventos auxiliares.](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI usa el **método IMAPITable::Advise** para registrar notificaciones con el objeto de permitir que la vista de tabla permanezca actualizada.  <br/> |
   
## <a name="see-also"></a>Consulte también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

