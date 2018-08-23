---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d052e7590ee502b55f2076d698587ab68820ca56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576704"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Responde a una notificación mediante la realización de una o varias tareas. Las tareas que realiza dependen del tipo de evento y el objeto que genera la notificación. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parámetros

 _cNotif_
  
> [entrada] El recuento de las estructuras de [notificación](notification.md) que señala el parámetro _lpNotifications_ . 
    
 _lpNotifications_
  
> [entrada] Un puntero a una o más estructuras de **notificación** que proporcionan información sobre los eventos que se han producido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se procesó correctamente.
    
## <a name="remarks"></a>Comentarios

El proceso de notificación se inicia cuando un cliente o MAPI realiza una llamada al método **Advise** de un proveedor de servicios a Regístrese para recibir una notificación de un tipo determinado de un objeto determinado. Uno de los parámetros para el método **Advise** es un puntero a un objeto de receptor advise que implementa la interfaz [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Cuando se produce un evento para el objeto de destino que corresponde a la notificación registrada, el proveedor de servicios, directa o indirectamente a través de MAPI, se llama a método de **OnNotify** del receptor de notificaciones. 
  
La llamada a **OnNotify** puede producirse durante la llamada MAPI que está provocando el evento o en algún momento posterior. En los sistemas que admiten varios subprocesos de ejecución, se puede llamar **OnNotify** en el mismo subproceso que se usó para el registro o en un subproceso diferente. Los clientes pueden asegurarse de que la llamada de **OnNotify** se realiza en el mismo subproceso utilizado para llamar a **Advise** creando el receptor de notificaciones que pasan al **Advise** con la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
El parámetro _lpNotifications_ apunta a uno o más estructuras de **notificación** que describen lo que ha cambiado durante el evento. No hay un tipo diferente de la estructura de **notificación** para cada tipo de evento. 
  
En la siguiente tabla se enumera los valores que se utilizan para representar los posibles tipos de eventos y las estructuras de asociado a cada valor:
  
|**Tipo de evento de notificación**|**Estructura correspondiente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
Para obtener más información acerca de cómo configurar y dejar de recibir notificaciones, vea las entradas de referencia para los métodos **Advise** y **Unadvise** para cualquiera de las siguientes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)y [IMSLogon](imslogoniunknown.md). 
  
Para obtener información general sobre el proceso de notificación, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

La implementación de **OnNotify** normalmente consistirá en uno o más bloques de código para cada tipo de notificación que espera recibir. Dentro de estos bloques de código, realice las tareas que considere necesarias como respuesta a la notificación. Por ejemplo, suponga que registrar para recibir notificaciones de **fnevObjectModified** en una carpeta que se incluye en una presentación del cuadro de diálogo. En el bloque de código que incluya en el método **OnNotify** para controlar las notificaciones de **fnevObjectModified** , es posible que envíe un mensaje de Windows para el cuadro de diálogo para solicitar una pantalla actualizado. 
  
No modifique o libre la estructura de **notificación** que se pasan a **OnNotify**. Los datos de la estructura son válidos sólo hasta que **OnNotify** devuelve. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se producen cambios a varios objetos, se puede notificar a un receptor de notificaciones registrados en una sola llamada a **OnNotify** o en varias llamadas según las restricciones de memoria. Esto es así independientemente de si los cambios son el resultado de una llamada al método o en varios. Por ejemplo, una llamada a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) puede afectar a varios mensajes y carpetas. Como un proveedor de almacén de mensajes, puede realizar una llamada a **OnNotify** con un tipo de evento **fnevObjectModified** para la carpeta de destino o cuántas llamadas, uno para cada afectan a los mensajes. De forma similar, si un cliente realiza llamadas repetidas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), estas llamadas se pueden combinar en un evento **fnevObjectModified** para la carpeta o dividirse en eventos individuales **fnevObjectCreated** para cada mensaje nuevo. 
  
Para que obtener más información acerca de cómo y cuándo se debe generar notificaciones, vea [Compatibilidad con notificación de eventos](supporting-event-notification.md)y [Notificación de eventos en MAPI](event-notification-in-mapi.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|AdviseSink.h y AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |La clase CAdviseSink se implementa para controlar todas las notificaciones en MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

