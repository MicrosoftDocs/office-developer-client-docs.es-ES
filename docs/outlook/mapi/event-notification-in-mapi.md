---
title: Notificación de eventos en MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389977"
---
# <a name="event-notification-in-mapi"></a>Notificación de eventos en MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Notificación de eventos es la comunicación de la información entre dos objetos MAPI. A través de uno de los objetos, un proveedor de servicio o cliente se registra para la notificación de un cambio o error, llamado a un evento, que es posible que tienen lugar en el otro objeto. Una vez que se produce el evento, el primer objeto se notifica el cambio o error. Objeto que recibe la notificación se denomina el receptor de notificaciones; el objeto responsable de la notificación se denomina el origen advise.
  
Hay tres tipos de advise objetos del receptor (todos los tipos son objetos estándar de MAPI):
  
- Objetos del receptor de aviso.   
- Formulario de aviso objetos del receptor.  
- Vista de aviso objetos del receptor.
    
Objetos de receptor son el tipo más común de aviso. Aviso receptores normalmente se implementan por las aplicaciones de cliente para recibir la libreta de direcciones y las notificaciones del almacén de mensajes y compatibilidad con el [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interfaz. **IMAPIAdviseSink** contiene un método único, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Formularios y vistas de aviso receptores son menos comunes; se implementan para recibir notificaciones sobre cambios en los formularios personalizados. Formulario de aviso compatibilidad con receptores de la [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) interfaz y vista de aviso compatibilidad con receptores de la [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interfaz. Debido a que los objetos del receptor de aviso estándar de implementar la mayoría de los clientes, se supone que las discusiones de notificaciones se relacionan con la libreta de direcciones y las notificaciones del almacén de mensajes en lugar de las notificaciones de formularios. Para obtener más información acerca de las notificaciones de formularios, vea [Las notificaciones de formularios de MAPI](mapi-forms-notifications.md) y la [Escritura de código de servidor de formulario](writing-form-server-code.md).
  
Origen de objetos se implementan por proveedores de servicio y por MAPI de aviso. No todos los proveedores de servicio admiten la notificación de evento; es opcional, pero se recomienda encarecidamente. Dirección y el almacén de mensajes del libro a proveedores normalmente las notificaciones del objeto de soporte técnico en varios de sus objetos y las notificaciones de tabla en su contenido y las tablas de jerarquía. Los proveedores de transporte no admiten notificaciones directamente; se basan en los métodos alternativos de comunicación con los clientes.
  
A diferencia de los receptores de advise, aviso de objetos de origen no son un único tipo de objeto MAPI. Muchos de los objetos MAPI, como almacenes de mensajes y tablas, pueden realizar en la función de origen advise. Un origen de advise es cualquier objeto MAPI que hace lo siguiente:
  
- Implementa un método **Advise** para recibir los registros de notificación. 
    
- Implementa un método **Unadvise** para recibir cancelaciones de notificación. 
    
- Genera las notificaciones del tipo adecuado a los objetos del receptor advise adecuados que se hayan registrado mediante una llamada a sus métodos **IMAPIAdviseSink::OnNotify** . 
    
Los clientes que implementan de aviso receptor objetos llamen **Advise** cuando desea registrarse para una notificación, en la mayoría de los casos pasando el identificador de entrada del objeto con el que debe producirse el registro y **Unadvise** cuando desean cancelar la en el registro. Los clientes pasan un parámetro a **Advise** que indica cuál de los varios tipos de eventos que desean supervisar. **Advise** devuelve un número distinto de cero que representa una conexión entre el receptor de notificaciones y el origen de advise correctamente. 
  
Antes de llamar a **Advise**, los clientes pueden determinar si un proveedor de almacén de mensajes es compatible con la notificación mediante la comprobación de que el indicador STORE_NOTIFY_OK se establece en **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén de mensajes propiedad. Hay ninguna forma para que los clientes determinar de antemano o no un proveedor de la libreta de direcciones es compatible con las notificaciones. Los clientes deben intentar registrar y si se produce un error en el intento, puede asumir las notificaciones no son compatibles.
  
Cuando se produce un evento para el que se ha registrado un cliente, el origen de advise notifica el receptor de notificaciones mediante una llamada a su método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) con una estructura de datos de notificación que contiene información sobre el evento. Implementación de un receptor de notificaciones de **OnNotify** puede realizar tareas en respuesta a la notificación, como actualizar datos en la memoria o actualizar una presentación de la pantalla. 
  
Proveedores de servicios pueden implementar la compatibilidad con las notificaciones de forma manual o aprovechar las ventajas de la ayuda proporcionada en tres métodos **IMAPISupport** : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport::Notify ](imapisupport-notify.md). Los métodos ** **Subscribe** y** controlen el registro de notificación y anulación de registro para los proveedores; el método **Notify** controla las notificaciones de envía cuando sea apropiado. 
  
Para usar los métodos del objeto compatibilidad con registro de notificaciones, proveedores de servicios de llamada [IMAPISupport::Subscribe](imapisupport-subscribe.md) en sus métodos **Advise** y pasan a **suscribir** el puntero de receptor de advise que los clientes pasan a **Advise**. Si un identificador de entrada se pasa como un parámetro de entrada para especificar un origen de advise, proveedores de servicios de conversión a una clave de binaria. **SUBSCRIBE** crea un número único de conexión y es este número que devuelven los proveedores de servicios a los clientes. Proveedores de servicios pueden liberar el cliente puntero de objeto de receptor de aviso en cualquier momento después de que haya finalizado la llamada **Advise** . 
  
Cuando los clientes llaman **Unadvise** para cancelar un registro, los proveedores de servicios puede ser disminuir el recuento de referencia en el cliente puntero receptor de aviso o llame al **Cancelar suscripción** para hacer lo mismo. 
  
Si es el momento de generar una notificación, proveedores de servicios de llevar a cabo cualquier procesamiento interno que se relaciona con la notificación e inicializa una estructura de [notificación](notification.md) mediante la configuración de todos sus miembros no usados en cero. Esta técnica para inicializar la estructura de **notificación** puede ayudar a los clientes a crear más pequeños, con mayor rapidez y menos propensas a errores implementaciones de **OnNotify** . 
  
En la siguiente ilustración se muestra la comunicación entre objetos del receptor de aviso, objetos de origen y MAPI de aviso. MAPI está implicada sólo cuando el origen de advise llama a los métodos **IMAPISupport** para soporte técnico de notificación. 
  
**Llamadas de notificación de eventos**
  
![Llamadas de notificación de eventos] (media/amapi_51.gif "Llamadas de notificación de eventos")
  
La clase MFCMAPI **CAdviseSink** (con los archivos AdviseSink.h y AdviseSink.cpp) implementa el objeto de receptor advise para todas las llamadas a **Advise**. Para obtener más información sobre MFCMAPI, consulte [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md) y [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

