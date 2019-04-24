---
title: Admitir notificación de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327429"
---
# <a name="supporting-event-notification"></a>Admitir notificación de eventos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como la notificación de eventos de admite puede ser complicada, MAPI proporciona tres métodos de objeto de compatibilidad que implementan las partes más difíciles del proceso. Estos métodos funcionan como una unidad y un proveedor debe usar los tres o ninguno de ellos.
  
Los métodos de compatibilidad con MAPI usan claves de notificación para administrar las conexiones entre los receptores de notificaciones y los objetos que generan las notificaciones. Una clave de notificación es una estructura [NOTIFKEY](notifkey.md) que contiene datos binarios que identifican un objeto a través de procesos. Normalmente, una clave de notificación se copia desde el identificador de entrada a largo plazo del objeto de origen Advise. Si el cliente ha proporcionado un identificador de entrada en la llamada a **Advise**, puede usarlo para la clave de notificación. Si el parámetro _lpEntryID_ a **Advise** es null, use el identificador de entrada del objeto contenedor más externo posible, como el almacén de mensajes. 
  
Para usar los métodos de soporte técnico, llame a [IMAPISupport:: subscribe](imapisupport-subscribe.md) siempre que **** un cliente llame a su método Advise para registrarse para obtener una notificación. Asigne una estructura [NOTIFKEY](notifkey.md) y cree una clave de notificación única para el objeto de origen Advise. Por ejemplo, un proveedor de almacenamiento de mensajes que se le solicita que notifique a un cliente cuando un mensaje se recibe en una carpeta determinada, crea una clave de notificación para dicha carpeta. Pase un puntero a la estructura **NOTIFKEY** en la llamada a **subscribe** junto con un puntero al receptor de notificaciones del cliente. **Subscribe** llama al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del receptor de notificación para incrementar su recuento de referencias y MAPI conserva el puntero hasta que se cancela el registro. 
  
Puede pasar la marca NOTIFY_SYNC para **suscribirse** para solicitar que la **notificación** se comporte de forma sincrónica y no se devuelva hasta que haya realizado todas las llamadas a los métodos [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) de los receptores de notificaciones registrados. Establezca esta marca solo para uso interno. No la establece cuando responde a una llamada de **aviso** de cliente. La notificación de eventos entre clientes y proveedores siempre es asincrónica. Es decir, MAPI garantiza que la llamada durante la que se produce un evento devolverá al cliente antes de que se realice alguna de las llamadas a **Notify** . 
  
Si establece la marca NOTIFY_SYNC, no realice ningún cambio en ninguno de los objetos del receptor de notificaciones y no pase un receptor de notificaciones de contenedor creado por [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para **suscribirse**. **HrThisThreadAdviseSink** crea una versión segura para subprocesos de un receptor de notificaciones para usarse solo con notificaciones asincrónicas. 
  
Si un receptor de notificaciones registrado para notificaciones sincrónicas devuelve de la **Notify** con el valor de la marca CALLBACK_DISCONTINUE, [IMAPISupport:: Notify](imapisupport-notify.md) establece la marca NOTIFY_CANCELED y devuelve sin realizar ninguna llamada a la **Notify**. 
  
Una vez que se ha devuelto la **suscripción** , ya no tendrá ninguna necesidad de retenerla en su copia del receptor de notificaciones del cliente. Llame a su método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberarlo. **Subscribe** devuelve un número de conexión distinto de cero que debe volver al cliente. El número de conexión representa el vínculo entre el origen de la notificación y el receptor de notificaciones. Sigue siendo válida hasta que el cliente realiza una llamada correcta **** a Advise. 
  
Cuando el cliente está listo para cancelar un registro, llama al método **** Advise. Pase el número de conexión de **** la llamada de desaconsejar a [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** llama al método **IUnknown:: Release** del receptor de aviso. Al igual que con **** **Advise** y Unadvise, las llamadas a **subscribe** y unsubscribe deben emparejarse. **** Debe realizar una llamada a **unsubscribe** para cada llamada que se realice a **subscribe**. Sin embargo, no es necesario llamar a **subscribe** cada vez que **** se llama al método Advise. Por el contrario, puede llamarlo para configurar notificaciones internas. 
  
Cuando se produzca un evento, asigne una o varias estructuras de [notificación](notification.md) del tipo adecuado para el evento y llame a [IMAPISupport:: Notify](imapisupport-notify.md). **Notify** genera una notificación para cada receptor de notificaciones registrado. Debe establecer todos los miembros sin usar de la estructura de [notificación](notification.md) en cero. Esta técnica para inicializar la estructura de **notificación** puede ayudar a los clientes a crear implementaciones de **Notify** más pequeñas, más rápidas y menos propensas a errores. 
  
Tenga en cuenta que es necesaria una estructura de **notificación** independiente para cada evento, incluso para varios eventos del mismo tipo. Por ejemplo, si se registran tres clientes para la notificación de tabla en una tabla concreta y se agregan cinco filas a la tabla, debe crear cinco estructuras **OBJECT_NOTIFICATION** para la llamada **Notify** . Una notificación por lotes como esta da como resultado un mejor rendimiento que la **notificación** de llamadas cinco veces. Para cada llamada a **Notify** , MAPI llama al método [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) de cada receptor de notificaciones registrado. Si no hay ningún receptor de notificaciones registrado, MAPI ignora la llamada. 
  
Los proveedores de servicios que envían notificaciones por lotes deben ordenarlos para que se puedan interpretar desde la primera notificación a la última. Esta ordenación es especialmente necesaria cuando un lote de notificaciones contiene una serie de eventos, como TABLE_ROW_ADDED con un evento que hace referencia a una fila anterior que se agregó en otro evento en el mismo lote.
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

