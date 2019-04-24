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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351446"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Responde a una notificación realizando una o más tareas. Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _cNotif_
  
> a El número de estructuras de [notificación](notification.md) a las que apunta el parámetro _lpNotifications_ . 
    
 _lpNotifications_
  
> a Puntero a una o varias estructuras **** de notificaciones que proporcionan información sobre los eventos que se han producido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha procesado correctamente.
    
## <a name="remarks"></a>Comentarios

El proceso de notificación se inicia cuando un cliente o MAPI realiza una llamada al método **Advise** de un proveedor de servicios para registrarse para recibir una notificación de un tipo determinado para un objeto determinado. Uno de los parámetros del método **Advise** es un puntero a un objeto de receptor de notificaciones que implementa la interfaz [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Cuando se produce un evento en el objeto de destino que corresponde a la notificación registrada, el proveedor de servicios, ya sea directa o indirectamente a través de MAPI, llama al método **Notify** del receptor de notificaciones. 
  
La llamada a **BENOTIFY** puede producirse durante la llamada MAPI que está causando el evento o en algún momento posterior. En los sistemas que admiten varios subprocesos de ejecución, se puede llamar a **BENOTIFY** en el mismo subproceso que se usó para el registro o en un subproceso diferente. Los clientes pueden asegurarse de que la llamada a la **Notify** se realiza en el mismo subproceso **** usado para llamar a Advise creando el receptor de notificaciones que pasan a Advise con la función [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . **** 
  
El parámetro _lpNotifications_ apunta a una o varias estructuras de **notificaciones** que describen lo que ha cambiado durante el evento. Hay un tipo de estructura de **notificación** diferente para cada tipo de evento. 
  
En la siguiente tabla se enumeran los valores que se usan para representar los posibles tipos de eventos y las estructuras asociadas con cada valor:
  
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
   
Para obtener más información sobre cómo configurar y detener las notificaciones, vea las entradas de referencia para los métodos **** Advise y **Unadvise** para cualquiera de las interfaces siguientes: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md) [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)y [IMSLogon](imslogoniunknown.md). 
  
Para obtener información general sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de la **Notify** se compone normalmente de uno o más bloques de código para cada tipo de notificación que se espera recibir. Dentro de estos bloques de código, realice las tareas que considere necesarias como respuesta a la notificación. Por ejemplo, supongamos que se registra para recibir notificaciones de **fnevObjectModified** en una carpeta incluida en una presentación de cuadro de diálogo. En el bloque de código que incluya en el método **NotifyTo** para controlar las notificaciones de **fnevObjectModified** , puede enviar un mensaje de Windows al cuadro de diálogo para solicitar una presentación actualizada. 
  
No modifique ni libere la estructura de **notificación** que se ha pasado a la **Notify**. Los datos de la estructura solo son válidos **** hasta que se deVuelvan notificaciones. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se producen cambios en varios objetos, puede notificar a un receptor de notificaciones registradas en una sola llamada a **BENOTIFY** o en varias llamadas en función de las restricciones de memoria. Esto es así independientemente de si los cambios son el resultado de una llamada de método o varias. Por ejemplo, una llamada a [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) puede afectar a varios mensajes y carpetas. Como proveedor de almacenamiento de mensajes, puede realizar una llamada a **BENOTIFY** con un tipo de evento **fnevObjectModified** para la carpeta de destino o muchas llamadas, una para cada mensaje afectado. De forma similar, si un cliente realiza llamadas repetidas a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), estas llamadas pueden combinarse en un **fnevObjectModified** evento para la carpeta o separarse en eventos individuales **fnevObjectCreated** para cada nuevo mensaje. 
  
Para obtener más información sobre cómo y cuándo generar notificaciones, consulte [notificación de eventos en MAPI](event-notification-in-mapi.md) y [notificación de eventos de soporte](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AdviseSink. h y AdviseSink. cpp  <br/> |CAdviseSink:: OnNotifyDesc  <br/> |La clase CAdviseSink se implementa para controlar todas las notificaciones de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notificaci�n](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

