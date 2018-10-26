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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594246"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Registra un objeto de receptor advise para recibir notificaciones de los eventos que afectan a la tabla.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulEventMask_
  
> [entrada] Valor que indica el tipo de evento que se va a generar la notificación. Sólo el valor siguiente es válido:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [entrada] Puntero a un objeto de receptor advise para recibir las notificaciones posteriores. Debe se han asignado ya este objeto de receptor advise.
    
 _lpulConnection_
  
> [out] Puntero a un valor distinto de cero que representa el registro de notificación correcta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación que se ha completado correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La implementación de la tabla no es compatible con los cambios realizados en sus filas y columnas o no admite la notificación.
    
## <a name="remarks"></a>Comentarios

Utilice el método **IMAPITable::Advise** para registrar un objeto de tabla implementado en el proveedor para realizar devoluciones de llamadas de notificación. Cada vez que se produce un cambio en el objeto table, el proveedor comprueba qué bit de máscara de eventos se estableció en el parámetro _ulEventMask_ y, por tanto, ¿qué tipo de cambio se ha producido. Si un bit está establecido, a continuación, el proveedor llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise indicado por el parámetro _lpAdviseSink_ para notificar el evento. Datos que se pasan en la estructura de notificación a la rutina de **OnNotify** describen el evento. 
  
La llamada a **OnNotify** puede producirse durante la llamada que cambia el objeto, o en cualquier momento siguiente. En los sistemas que admiten varios subprocesos de ejecución, puede producirse la llamada a **OnNotify** en cualquier subproceso. Para que una forma de convertir una llamada a **OnNotify** que puede suceder en un momento inoportuno en uno que es más seguro administrar, un proveedor debe usar la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para proporcionar notificaciones, de las necesidades de **Advise** implementación del proveedor para mantener una copia del puntero a la _lpAdviseSink_ aviso objeto receptor; Para ello, se llama al método **IUnknown:: AddRef** para el receptor de notificaciones mantener su puntero del objeto hasta que se cancele el registro de la notificación con una llamada al método [IMAPITable::Unadvise](imapitable-unadvise.md) . La implementación de **Advise** debe asignar a un número de conexión para el registro de la notificación y llamar a **AddRef** en este número de conexión antes de devolver en el parámetro _lpulConnection_ . Proveedores de servicios pueden liberar el objeto de receptor de advise antes de que se ha cancelado el registro, pero no debe liberar el número de conexión hasta ** Unadvise ** se ha llamado. 
  
Después de que se ha realizado correctamente una llamada a **Advise** y antes de ** Unadvise ** ha sido llamado, es preciso preparar los clientes para que el objeto de receptor advise que liberar. Un cliente, por tanto, debe liberar su objeto de receptor advise después **Advise** devuelve a menos que tenga un uso a largo plazo específico para él. 
  
Debido al comportamiento asincrónico de notificación, las implementaciones que cambiar la configuración de columna de tabla pueden recibir notificaciones con información organizada en un orden de la columna anterior. Por ejemplo, es posible que devuelve una fila de tabla para un mensaje que sólo se ha eliminado del contenedor. Se envía una notificación cuando se ha realizado el cambio de configuración de columna y envía información acerca de él, pero la vista de tabla de notificación no se ha actualizado con esa información todavía.
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). Para obtener información específica acerca de la notificación de la tabla, vea [Acerca de las notificaciones de tabla](about-table-notifications.md). Para obtener información acerca del uso de los métodos **IMAPISupport** para admitir la notificación, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI utiliza el método **IMAPITable::Advise** para registrar para que las notificaciones permitir la vista de tabla para mantenerse al día.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

