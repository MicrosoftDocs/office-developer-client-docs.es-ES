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
ms.openlocfilehash: db23d1801bf32fd947a77dfd887c56f75ded5681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817519"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Hace referencia a**: Outlook 
  
Envía una notificación de un evento especificado a un origen de advise que registró originalmente para la notificación a través del método [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

_lpKey_
  
> [entrada] Un puntero a la clave de notificación para el objeto de origen advise. El parámetro _lpKey_ no puede ser NULL. 
    
_cNotification_
  
> [entrada] El recuento de las estructuras de notificación que señala el parámetro _lpNotifications_ . 
    
_lpNotifications_
  
> [entrada] Un puntero a una matriz de estructuras de [notificación](notification.md) que se describen las notificaciones pendientes. 
    
_lpulFlags_
  
> [entrada, salida] Una máscara de bits de indicadores que controla el proceso de notificación. En la entrada, se puede establecer la marca siguiente:
    
  - MAPI_UNICODE. 
    
    > Las cadenas en las estructuras de notificación que señala _lpNotifications_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 

    En la salida, MAPI puede establecer la marca siguiente:
        
  - NOTIFY_CANCELED 
    
    > Una función de devolución de llamada cancela una notificación sincrónica.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las notificaciones se han generado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::Notify** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamada **Notify** para solicitar que MAPI generar una notificación para un receptor de notificaciones que se ha registrado previamente para la notificación a través del método **IMAPISupport::Subscribe** . 
  
**Notify** copias las estructuras indicada por el parámetro _lpNotifications_ en la memoria y llama a método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor advise adecuado. Cuando finalice **OnNotify** con la notificación, libera la memoria implicados. El autor de la llamada no es necesario asignar memoria; MAPI realiza toda la asignación de memoria necesaria. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La clave de notificación que se pasa en el parámetro _lpKey_ debe ser idéntica a la clave pasada en _lpKey_ al método **IMAPISupport::Subscribe** . Muchos proveedores de utilizan el identificador de entrada del origen de advise como la clave, pero otros datos, como una ruta de acceso de archivo, se pueden usar. MAPI utiliza esta clave para buscar todos los registros para las notificaciones en el origen de advise identificados. 
  
Asegúrese de que establece al miembro **lpEntryID** de la estructura de notificación en un identificador de entrada a largo plazo. 
  
Si se establece el indicador NOTIFY_SYNC en la **suscripción** de llamadas para cualquiera de las notificaciones pendientes, **Notificar** llamadas las funciones de devolución de llamada de método **IMAPIAdviseSink::OnNotify** antes de devolver. Un receptor de notificaciones puede crearse manualmente o mediante una llamada a [HrAllocAdviseSink](hrallocadvisesink.md). La función **HrAllocAdviseSink** permite su autor de la llamada especificar una función de devolución de llamada que llama **Notify** como parte de la notificación. La función de devolución de llamada se ajusta al prototipo [NOTIFCALLBACK](notifcallback.md) . Funciones de devolución de llamada implementadas por los clientes siempre devuelven S_OK; funciones de devolución de llamada que se implementan los proveedores de servicio pueden devolver CALLBACK_DISCONTINUE. 
  
Si una función de devolución de llamada devuelve CALLBACK_DISCONTINUE, MAPI deja de enviar notificaciones y devuelve NOTIFY_CANCELED en el **Notify** parámetro del método _lpulFlags_ . Puede asumir que el proceso está inactivo y detención de generación de notificaciones para ese proceso. Si **Notify** devuelve 0 en _lpulFlags_, el proceso todavía está activo y se debe seguir enviar notificaciones, según corresponda.
  
Al usar notificaciones sincrónicas, tenga cuidado para evitar situaciones de interbloqueo.
  
Para obtener más información sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notificaci�n](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

