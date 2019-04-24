---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326372"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Envía una notificación de un evento especificado a un origen de notificaciones que se registró originalmente para la notificación a través del método [IMAPISupport:: subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

_lpKey_
  
> a Un puntero a la clave de notificación para el objeto de origen Advise. El parámetro _lpKey_ no puede ser nulo. 
    
_cNotification_
  
> a El número de estructuras de notificación a las que apunta el parámetro _lpNotifications_ . 
    
_lpNotifications_
  
> a Un puntero a una matriz de estructuras de [notificación](notification.md) que describe las notificaciones pendientes. 
    
_lpulFlags_
  
> [in, out] Máscara de máscara de marcadores que controla el proceso de notificación. En la entrada, se puede establecer la siguiente marca:
    
  - MAPI_UNICODE 
    
    > Las cadenas de las estructuras de notificación a las que apunta _lpNotifications_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 

    En la salida, MAPI puede establecer la siguiente marca:
        
  - NOTIFY_CANCELED 
    
    > Una función de devolución de llamada canceló una notificación sincrónica.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las notificaciones se generaron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: Notify** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios llaman a **Notify** para solicitar que MAPI genere una notificación para un receptor de notificaciones previamente registrado para la notificación a través del método **IMAPISupport:: subscribe** . 
  
**Notify** copia en la memoria las estructuras señaladas por el parámetro _lpNotifications_ y llama al m? todo [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) del receptor adecuado. Cuando **Notify** termina con la notificación, libera la memoria implicada. El autor de la llamada no necesita asignar memoria; MAPI realiza toda la asignación de memoria necesaria. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La clave de notificación que se pasa en el parámetro _lpKey_ debe ser idéntica a la clave pasada en _LpKey_ al método **IMAPISupport:: subscribe** . Muchos proveedores usan el identificador de entrada del origen Advise como la clave, pero se pueden usar otros datos, como una ruta de acceso de archivo. MAPI usa esta clave para buscar todos los registros de notificaciones en el origen de Advise identificado. 
  
Asegúrese de establecer el miembro **lpEntryID** de la estructura de notificación en un identificador de entrada a largo plazo. 
  
Si establece la marca NOTIFY_SYNC en la llamada **subscribe** para cualquiera de las notificaciones pendientes, **Notify** llama a las funciones de devolución de llamada del método **IMAPIAdviseSink:: BENOTIFY** antes de devolverse. Un receptor de notificaciones se puede crear manualmente o llamando a [HrAllocAdviseSink](hrallocadvisesink.md). La función **HrAllocAdviseSink** permite al autor de la llamada especificar una función de devolución de llamada que **notifica** las llamadas como parte de la notificación. La función de devolución de llamada se ajusta al prototipo [NOTIFCALLBACK](notifcallback.md) . Las funciones de devolución de llamada implementadas por los clientes siempre devuelven S_OK; las funciones de devolución de llamada implementadas por proveedores de servicios pueden devolver CALLBACK_DISCONTINUE. 
  
Si una función de devolución de llamada devuelve CALLBACK_DISCONTINUE, MAPI deja de enviar notificaciones y devuelve NOTIFY_CANCELED en el parámetro _lpulFlags_ del método **Notify** . Puede dar por hecho que el proceso está inactivo y dejar de generar notificaciones para ese proceso. Si **Notify** devuelve 0 en _lpulFlags_, el proceso sigue activo y debe seguir enviando notificaciones, según corresponda.
  
Cuando use notificaciones sincrónicas, procure evitar situaciones de interbloqueo.
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notificaci�n](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

