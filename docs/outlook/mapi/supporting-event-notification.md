---
title: Admitir notificaciones de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 45bfe9f9314a154bd5f096ac20f76f6bf4f259c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820774"
---
# <a name="supporting-event-notification"></a>Admitir notificaciones de eventos

  
  
**Hace referencia a**: Outlook 
  
Debido a que la compatibilidad con notificación de evento puede ser complicada, MAPI proporciona tres métodos de objeto de soporte técnico que implementan las partes más difíciles del proceso. Estos métodos funcionan como una unidad, y debe usar un proveedor de las tres o ninguno de ellos.
  
Los métodos de soporte técnico MAPI usan claves de notificación para administrar las conexiones entre los receptores advise y los objetos que generan las notificaciones. Una clave de notificación es una estructura [NOTIFKEY](notifkey.md) que contiene datos binarios que identifica un objeto a través de los procesos. Normalmente, una clave de notificación se copia desde el identificador de entrada a largo plazo del objeto de origen advise. Si el cliente ha suministrado un identificador de entrada en la llamada a **Advise**, puede utilizarlo para la clave de notificación. Si el parámetro _lpEntryID_ **Advise** es NULL, utilice el identificador de entrada del objeto contenedor posibles externo, como el almacén de mensajes. 
  
Para usar los métodos de soporte técnico, llame a [IMAPISupport::Subscribe](imapisupport-subscribe.md) cada vez que un cliente llama al método **Advise** se registre para una notificación. Asignar una estructura [NOTIFKEY](notifkey.md) y crear una clave de notificación único para el objeto de origen advise. Por ejemplo, un proveedor de almacén de mensajes que se le pide que notificar a un cliente cuando se recibe un mensaje en una carpeta determinada crea una clave de notificación para esa carpeta. Pase un puntero a la estructura **NOTIFKEY** en la llamada a **Subscribe** junto con un puntero para el cliente de aviso receptor. **SUBSCRIBE** llama al método [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del receptor de notificaciones para incrementar su recuento de referencia y MAPI conserva el puntero hasta que se cancela el registro. 
  
Puede pasar la marca NOTIFY_SYNC **suscribirse** para solicitar que se comportan los **Notify** devueltos de forma sincrónica y no hasta que haya realizado todas las llamadas a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del registrado receptores de aviso. Establezca esta marca sólo para su propio uso interno. No se establece al responder a un cliente **Advise** llamada. Notificación de eventos entre los clientes y proveedores siempre es asincrónico. Es decir, MAPI, garantiza que la llamada durante el cual se produce un evento devolverá al cliente antes de cualquiera de las llamadas de **OnNotify** se realizan. 
  
Si se establece la marca NOTIFY_SYNC, no realice ningún cambio en cualquiera de los objetos del receptor de advise y no se pasa un receptor de notificaciones de contenedor creado por [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) **suscribirse**. **HrThisThreadAdviseSink** crea una versión de subprocesos de un receptor de notificaciones que se usará con sólo la notificación asincrónica. 
  
Si un receptor de notificaciones que se registró para la notificación sincrónica devuelve de **OnNotify** con el conjunto de marca CALLBACK_DISCONTINUE, [IMAPISupport::Notify](imapisupport-notify.md) establece la marca NOTIFY_CANCELED y devuelve sin realizar todas las llamadas a **OnNotify**. 
  
Una vez que ha devuelto **Subscribe** , ya no tendrá ninguna necesidad de retener su copia del receptor de aviso del cliente. Llame a su método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberarlo. **SUBSCRIBE** devuelve un número distinto de cero de conexión que se debe devolver al cliente. El número de conexión representa el vínculo entre el origen de advise y el receptor de notificaciones. Sigue siendo válida hasta que el cliente realiza una llamada satisfactoria a **Unadvise**. 
  
Cuando el cliente está listo para cancelar un registro, se llama al método **Unadvise** . Pase el número de conexión de la llamada **Unadvise** a [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Cancelar suscripción** llama a método de **IUnknown:: Release** del receptor de notificaciones. Al igual que con **Advise** y **Unadvise**, las llamadas a ** **Subscribe** y** deben estar emparejadas. Debe realizar una llamada a **Unsubscribe** por cada llamada que se realiza a **Subscribe**. Sin embargo, no es necesario llamar a **Subscribe** cada vez que se llame al método **Advise** . Por el contrario, se puede llamar para configurar notificaciones internas. 
  
Cuando se produce un evento, asignar uno o más estructuras de [notificación](notification.md) del tipo apropiado para el evento y llame a [IMAPISupport::Notify](imapisupport-notify.md). **Notify** genera una notificación para cada receptor de notificaciones registrados. Debe establecer todos los miembros no usados de la estructura de [notificación](notification.md) en cero. Esta técnica para inicializar la estructura de **notificación** puede ayudar a los clientes a crear más pequeños, con mayor rapidez y menos propensas a errores implementaciones de **OnNotify** . 
  
Tenga en cuenta que es necesaria para cada evento, incluso para varios eventos del mismo tipo de una estructura de **notificación** independiente. Por ejemplo, si tres clientes se registran para la notificación de la tabla en una tabla determinada y cinco filas se agregan a la tabla, debe crear cinco estructuras **OBJECT_NOTIFICATION** para la llamada de **notificación** . Una notificación por lotes como esto da como resultado un mejor rendimiento que una llamada a **Notify** cinco veces. Para cada llamada **Notify** , MAPI llama al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de cada receptor de notificaciones registrados. Si hay no registrado de aviso receptores, MAPI, pasa por alto la llamada. 
  
Proveedores de servicios que envían notificaciones por lotes deben ordenarlas por lo que puede interpretar de la primera notificación a la última. En este orden es especialmente necesaria cuando un lote de notificación contiene una serie de eventos, como TABLE_ROW_ADDED con un evento que hace referencia a una fila anterior que se ha agregado en otro evento en el mismo lote.
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

