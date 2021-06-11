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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435939"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Envía una notificación de un evento especificado a un origen de aviso que se registró originalmente para la notificación a través del [método IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
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
  
> [in] Puntero a la clave de notificación del objeto de origen advise. El  _parámetro lpKey_ no puede ser NULL. 
    
_cNotification_
  
> [in] Recuento de estructuras de notificación a las que apunta el _parámetro lpNotifications._ 
    
_lpNotifications_
  
> [in] Puntero a una matriz de estructuras [NOTIFICATION](notification.md) que describen notificaciones pendientes. 
    
_lpulFlags_
  
> [in, out] Máscara de bits de marcas que controla el proceso de notificación. En la entrada, se puede establecer la siguiente marca:
    
  - MAPI_UNICODE 
    
    > Las cadenas de las estructuras de notificación a las que  _apunta lpNotifications_ están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 

    En el resultado, MAPI puede establecer la siguiente marca:
        
  - NOTIFY_CANCELED 
    
    > Una función de devolución de llamada canceló una notificación sincrónica.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las notificaciones se generaron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::Notify** se implementa para todos los objetos de soporte técnico del proveedor de servicios. Los proveedores de servicios llaman a **Notify** para solicitar que MAPI genere una notificación para un receptor de notificaciones que se haya registrado previamente para la notificación a través del **método IMAPISupport::Subscribe.** 
  
**Notify** copia las estructuras a las que apunta el parámetro  _lpNotifications_ en la memoria y llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de notificaciones adecuado. Cuando **OnNotify** finaliza con la notificación, libera la memoria implicada. El autor de la llamada no necesita asignar memoria; MAPI realiza toda la asignación de memoria necesaria. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La clave de notificación pasada en el _parámetro lpKey_ debe ser idéntica a la clave pasada en _lpKey_ al **método IMAPISupport::Subscribe.** Muchos proveedores usan el identificador de entrada del origen de aviso como clave, pero se pueden usar otros datos, como una ruta de acceso de archivo. MAPI usa esta clave para buscar todos los registros de notificaciones en el origen de aviso identificado. 
  
Asegúrese de establecer el miembro **lpEntryID** de la estructura de notificaciones en un identificador de entrada a largo plazo. 
  
Si establece la marca NOTIFY_SYNC en la llamada **Subscribe** para cualquiera de las notificaciones pendientes, **Notify** llama a las funciones de devolución de llamada del método **IMAPIAdviseSink::OnNotify** antes de devolver. Un receptor de avisos se puede crear manualmente o llamando a [HrAllocAdviseSink](hrallocadvisesink.md). La **función HrAllocAdviseSink** permite a su autor de la llamada especificar una función de devolución de llamada que **Notify** llama como parte de la notificación. La función de devolución de llamada se ajusta al prototipo [NOTIFCALLBACK.](notifcallback.md) Las funciones de devolución de llamada implementadas por los clientes siempre devuelven S_OK; Las funciones de devolución de llamada implementadas por los proveedores de servicios pueden devolver CALLBACK_DISCONTINUE. 
  
Si una función de devolución de llamada devuelve CALLBACK_DISCONTINUE, MAPI deja de enviar notificaciones y devuelve NOTIFY_CANCELED en el parámetro _lpulFlags_ del método **Notify.** Puede asumir que el proceso está inactivo y dejar de generar notificaciones para ese proceso. Si **Notify** devuelve 0 en  _lpulFlags,_ el proceso sigue activo y debe continuar con el envío de notificaciones, según corresponda.
  
Cuando use notificaciones sincrónicas, tenga cuidado de evitar situaciones de interbloqueo.
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notificaci�n](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

