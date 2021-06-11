---
title: Notificación de eventos de soporte técnico
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
# <a name="supporting-event-notification"></a>Notificación de eventos de soporte técnico

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Dado que la notificación de eventos auxiliares puede ser complicada, MAPI proporciona tres métodos de objeto de soporte que implementan las partes más difíciles del proceso. Estos métodos funcionan como una unidad y un proveedor debe usar los tres o ninguno de ellos.
  
Los métodos de soporte técnico MAPI usan claves de notificación para administrar las conexiones entre los receptores de notificaciones y los objetos que generan las notificaciones. Una clave de notificación es una [estructura NOTIFKEY](notifkey.md) que contiene datos binarios que identifican un objeto en todos los procesos. Normalmente, se copia una clave de notificación del identificador de entrada a largo plazo del objeto de origen advise. Si el cliente ha proporcionado un identificador de entrada en la llamada a **Advise,** puede usarlo para la clave de notificación. Si el  _parámetro lpEntryID_ de **Advise** es NULL, use el identificador de entrada del objeto contenedor más externo posible, como el almacén de mensajes. 
  
Para usar los métodos de soporte técnico, llame a [IMAPISupport::Subscribe](imapisupport-subscribe.md) siempre que un cliente llame al método **Advise** para registrarse para una notificación. Asigne una [estructura NOTIFKEY](notifkey.md) y cree una clave de notificación única para el objeto de origen advise. Por ejemplo, un proveedor de almacén de mensajes al que se le pide que notifique a un cliente cuando se recibe un mensaje en una carpeta determinada crea una clave de notificación para esa carpeta. Pase un puntero a la **estructura NOTIFKEY** en la llamada a **Subscribe** junto con un puntero al receptor de avisos del cliente. **Subscribe** llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del receptor de aviso para incrementar su recuento de referencias y MAPI retiene el puntero hasta que se cancela el registro. 
  
Puede pasar la marca de NOTIFY_SYNC a **Subscribe** para solicitar que **Notify** se comporte de forma sincrónica y no vuelva hasta que haya realizado todas las llamadas a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de receptores de aviso registrados. Establezca esta marca solo para su propio uso interno. No lo establezca cuando responda a una llamada de **aviso de** cliente. La notificación de eventos entre clientes y proveedores siempre es asincrónica. Es decir, MAPI garantiza que la llamada durante la cual se produce un evento volverá al cliente antes de realizar cualquiera de las llamadas **OnNotify.** 
  
Si establece la marca NOTIFY_SYNC, no realice ningún cambio en ninguno de los objetos del receptor de aviso y no pase un receptor de aviso de contenedor creado por [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) a **Subscribe**. **HrThisThreadAdviseSink** crea una versión segura para subprocesos de un receptor de notificaciones que se usará únicamente con notificaciones asincrónicas. 
  
Si un receptor de notificaciones registrado para notificaciones sincrónicas devuelve de **OnNotify** con el conjunto de marcas de CALLBACK_DISCONTINUE, [IMAPISupport::Notify](imapisupport-notify.md) establece la marca NOTIFY_CANCELED y devuelve sin realizar ninguna llamada a **OnNotify**. 
  
Una **vez** que Subscribe haya devuelto, ya no tendrá que retener la copia del receptor de avisos del cliente. Llama a [su método IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberarlo. **Subscribe** devuelve un número de conexión distinto de cero que debe devolver al cliente. El número de conexión representa el vínculo entre el origen del aviso y el receptor de avisos. Permanece válido hasta que el cliente realiza una llamada correcta a **Unadvise**. 
  
Cuando el cliente está listo para cancelar un registro, llama al **método Unadvise.** Pase el número de conexión de la llamada **Unadvise** a [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** llama al método **IUnknown::Release** del receptor de avisos. Al igual **que con Advise** y **Unadvise,** las llamadas a **Subscribe** y **Unsubscribe** deben emparejarse. Debe realizar una llamada a **Unsubscribe** por cada llamada que se realice a **Subscribe**. Sin embargo, no es necesario llamar a **Subscribe** cada vez que se llama **al método Advise.** Por el contrario, puede llamarlo para configurar notificaciones internas. 
  
Cuando se produzca un evento, asigne una o más estructuras [de NOTIFICACIÓN](notification.md) del tipo adecuado para el evento y llame a [IMAPISupport::Notify](imapisupport-notify.md). **Notify** genera una notificación para cada receptor de notificaciones registrado. Debe establecer todos los miembros no usados de la [estructura NOTIFICATION](notification.md) en cero. Esta técnica para inicializar la estructura **notification** puede ayudar a los clientes a crear implementaciones **onNotify** más pequeñas, rápidas y menos propensas a errores. 
  
Tenga en cuenta que es **necesaria una** estructura notification independiente para cada evento, incluso para varios eventos del mismo tipo. Por ejemplo, si tres clientes están registrados para la notificación de tabla en una tabla determinada y se agregan cinco filas a la tabla, debe crear cinco **estructuras OBJECT_NOTIFICATION** para la llamada **notify.** Una notificación por lotes como esta da como resultado un mejor rendimiento que llamar **a Notify** cinco veces. Para cada **llamada Notify,** MAPI llama al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de todos los receptores de notificaciones registrados. Si no hay receptores de aviso registrados, MAPI omite la llamada. 
  
Los proveedores de servicios que envían notificaciones por lotes deben ordenarlas para que se puedan interpretar desde la primera notificación hasta la última. Este orden es especialmente necesario cuando un lote de notificaciones contiene una serie de eventos, como TABLE_ROW_ADDED con un evento que hace referencia a una fila anterior que se agregó en otro evento del mismo lote.
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

