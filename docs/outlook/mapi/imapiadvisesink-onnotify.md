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
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407364"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Responde a una notificación realizando una o varias tareas. Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _cNotif_
  
> [in] Recuento de estructuras [NOTIFICATION](notification.md) a las que apunta el _parámetro lpNotifications._ 
    
 _lpNotifications_
  
> [in] Puntero a una o más estructuras **de NOTIFICACIÓN** que proporcionan información sobre los eventos que se han producido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha procesado correctamente.
    
## <a name="remarks"></a>Comentarios

El proceso de notificación se inicia cuando un cliente o MAPI realiza una llamada al método **Advise** de un proveedor de servicios para registrarse para recibir una notificación de un tipo determinado para un objeto determinado. Uno de los parámetros del método **Advise** es un puntero a un objeto receptor de aviso que implementa la interfaz [IMAPIAdviseSink.](imapiadvisesinkiunknown.md) Cuando se produce un evento en el objeto de destino que corresponde a la notificación registrada, el proveedor de servicios, ya sea directa o indirectamente a través de MAPI, llama al método **OnNotify** del receptor de notificaciones. 
  
La llamada a **OnNotify** puede producirse durante la llamada MAPI que está provocando el evento o en algún momento posterior. En sistemas que admiten varios subprocesos de ejecución, se puede llamar a **OnNotify** en el mismo subproceso que se usó para el registro o en un subproceso diferente. Los clientes pueden asegurarse de que la llamada **OnNotify** se realiza en el mismo subproceso que se usa para llamar a **Advise** mediante la creación del receptor de avisos que pasan a **Advise** con la función [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
El  _parámetro lpNotifications_ apunta a una o más estructuras **NOTIFICATION** que describen lo que ha cambiado durante el evento. Hay un tipo diferente de estructura **DE NOTIFICACIÓN** para cada tipo de evento. 
  
En la tabla siguiente se enumeran los valores que se usan para representar los posibles tipos de eventos y las estructuras asociadas a cada valor:
  
|**Tipo de evento Notification**|**Estructura correspondiente**|
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
   
Para obtener más información sobre cómo configurar y detener notificaciones, vea las entradas de referencia para los métodos **Advise** y **Unadvise** para cualquiera de las interfaces siguientes: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md). 
  
Para obtener información general sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La **implementación de OnNotify** normalmente constará de uno o más bloques de código para cada tipo de notificación que espera recibir. Dentro de estos bloques de código, realice las tareas que considere necesarias como respuesta a la notificación. Por ejemplo, supongamos que se registra para recibir **notificaciones fnevObjectModified** en una carpeta que se incluye en una presentación de cuadro de diálogo. En el bloque de código que incluya en el método **OnNotify** para controlar las notificaciones **fnevObjectModified,** puede enviar un mensaje de Windows al cuadro de diálogo para solicitar una presentación actualizada. 
  
No modifique ni libera la estructura **notification** que se pasa a **OnNotify**. Los datos de la estructura solo son válidos hasta que **OnNotify devuelve.** 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se producen cambios en varios objetos, puede notificar a un receptor de aviso registrado en una sola llamada a **OnNotify** o en varias llamadas según las restricciones de memoria. Esto es así independientemente de si los cambios son el resultado de una llamada de método o de varios. Por ejemplo, una llamada a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) puede afectar a varios mensajes y carpetas. Como proveedor de almacén de mensajes, puede realizar una llamada a **OnNotify** con un tipo de evento **fnevObjectModified** para la carpeta de destino o muchas llamadas, una para cada mensaje afectado. Del mismo modo, si un cliente realiza llamadas repetidas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), estas llamadas se pueden combinar en un evento **fnevObjectModified** para la carpeta o separarse en eventos **fnevObjectCreated** individuales para cada nuevo mensaje. 
  
Para obtener más información sobre cómo y cuándo generar notificaciones, vea [Event Notification in MAPI](event-notification-in-mapi.md) y [Supporting Event Notification](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AdviseSink.h y AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |La clase CAdviseSink se implementa para controlar todas las notificaciones de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

