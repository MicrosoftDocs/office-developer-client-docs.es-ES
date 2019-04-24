---
title: Notificación de eventos de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321402"
---
# <a name="event-notification-in-mapi"></a>Notificación de eventos de MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La notificación de eventos es la comunicación de información entre dos objetos MAPI. A través de uno de los objetos, un cliente o proveedor de servicios registra la notificación de un cambio o error, denominado evento, que puede tener vez en el otro objeto. Una vez que se produce el evento, se notifica el cambio o error al primer objeto. El objeto que recibe la notificación se denomina receptor de notificaciones; el objeto responsable de la notificación se denomina origen de notificaciones.
  
Hay tres tipos de objetos de notificación de notificaciones (todos los tipos son objetos MAPI estándar):
  
- Notificar a los objetos del receptor.   
- Los objetos de receptor de notificaciones de formulario.  
- Ver los objetos del receptor de notificaciones.
    
Los objetos Sink de aviso son el tipo más común. Los receptores de notificaciones suelen ser implementados por las aplicaciones cliente para recibir notificaciones de la libreta de direcciones y del almacén de mensajes, y admiten la interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) . **IMAPIAdviseSink** contiene un método único, [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md). Los receptores de notificaciones de formulario y vista son menos comunes; se implementan para recibir notificaciones sobre cambios en los formularios personalizados. Los receptores de notificaciones de formulario admiten la [IMAPIFormAdviseSink:](imapiformadvisesinkiunknown.md) la interfaz IUnknown y los receptores de notificaciones admiten la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . Como la mayoría de los clientes implementan objetos de notificación de avisos estándar, supongamos que las discusiones de notificaciones se relacionan con la libreta de direcciones y notificaciones de almacén de mensajes en lugar de notificaciones de formulario. Para obtener más información acerca de las notificaciones de formulario, consulte notificaciones de [formularios MAPI](mapi-forms-notifications.md) y [código de servidor de escritura](writing-form-server-code.md).
  
Aconsejar que los proveedores de servicios y MAPI implementen los objetos de origen. No todos los proveedores de servicios admiten la notificación de eventos; es opcional, pero se recomienda encarecidamente. El almacén de mensajes y los proveedores de libretas de direcciones normalmente admiten notificaciones de objeto en varios de sus objetos y notificaciones de tabla en sus tablas de contenido y jerarquía. Los proveedores de transporte no admiten notificaciones directamente; se basan en métodos alternativos de comunicación con los clientes.
  
A diferencia de los receptores de notificaciones, los objetos de origen de aviso no son un tipo único de objeto MAPI. Muchos objetos MAPI, como las tablas y los almacenes de mensajes, pueden tomar el papel de origen de la notificación. Un origen de aviso es cualquier objeto MAPI que hace lo siguiente:
  
- Implementa un método **Advise** para recibir registros de notificaciones. 
    
- Implementa un método **Unadvise** para recibir cancelaciones de notificaciones. 
    
- Genera notificaciones del tipo apropiado a los objetos de receptor de notificaciones adecuados que se registraron mediante una llamada a sus métodos **IMAPIAdviseSink:: método Notify** . 
    
Los clientes que implementan los objetos **** de notificaciones de aviso llaman a Advise cuando desean registrarse para obtener una notificación, en la mayoría de los casos pasando el identificador de entrada del objeto con el que debe producirse el registro, y sin **avisar** cuando quieran cancelar el registro. Los clientes pasan un parámetro **** a Advise que indica cuál de los distintos tipos de eventos desea supervisar. **Advise** devuelve un número distinto de cero que representa una conexión correcta entre el receptor de notificaciones y el origen de la notificación. 
  
Antes de **** llamar a Advise, los clientes pueden determinar si un proveedor de almacenamiento de mensajes admite notificaciones comprobando que la marca STORE_NOTIFY_OK está establecida en el **PR_STORE_SUPPORT_MASK** del almacén de mensajes ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Inspector. No hay ninguna manera de que los clientes determinen con antelación si un proveedor de libreta de direcciones admite o no las notificaciones. Los clientes deben intentar registrarse y, si se produce un error en el intento, pueden suponer que no se admiten notificaciones.
  
Cuando se produce un evento para el que un cliente se registró, el origen Advise notifica al receptor de notificaciones llamando a su método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) con una estructura de datos de notificación que contiene información sobre el evento. La implementación de notificar a un receptor de **BENOTIFY** puede realizar tareas en respuesta a la notificación, como la actualización de datos en la memoria o la actualización de la presentación en pantalla. 
  
Los proveedores de servicios pueden implementar la compatibilidad de las notificaciones manualmente o aprovechar la ayuda proporcionada en tres métodos **IMAPISupport** : [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport:: Notify ](imapisupport-notify.md). Los métodos **subscribe** y unsubscribe controlan el registro y la anulación de registros de la notificación para los proveedores; **** el método **Notify** controla el envío de notificaciones cuando corresponda. 
  
Para usar los métodos de objeto de soporte para el registro de notificaciones, los proveedores de servicios llaman a [IMAPISupport:: subscribe](imapisupport-subscribe.md) en sus métodos de **aviso** y pasan a **suscribir** el puntero de aviso que los clientes pasan a Advise. **** Si se pasa un identificador de entrada como parámetro de entrada para especificar un origen de notificaciones, los proveedores de servicios lo convierten en una clave binaria. **Subscribe** crea un número de conexión único y es este número que los proveedores de servicios devuelven a los clientes. Los proveedores de servicios pueden liberar el puntero de notificaciones del objeto receptor del cliente **** en cualquier momento después de que se haya completado la llamada a Advise. 
  
Cuando los clientes llaman a **Unadvise** para cancelar un registro, los proveedores de servicios reducen el recuento de referencia en el puntero de notificaciones de receptor del cliente o llaman a unsubscribe para hacer lo mismo. **** 
  
Cuando es el momento de generar una notificación, los proveedores de servicios realizan cualquier procesamiento interno que se relacione con la notificación e inicializa una estructura de [notificación](notification.md) estableciendo todos los miembros que no se usan en cero. Esta técnica para inicializar la estructura de **notificación** puede ayudar a los clientes a crear implementaciones de **Notify** más pequeñas, más rápidas y menos propensas a errores. 
  
La ilustración siguiente muestra la comunicación entre los objetos del receptor de notificaciones, los objetos de origen Advise y MAPI. MAPI sólo está implicado cuando el origen Advise llama a los métodos **IMAPISupport** para la compatibilidad con la notificación. 
  
**Llamadas de notificación de eventos**
  
![Llamadas de notificación de eventos] (media/amapi_51.gif "Llamadas de notificación de eventos")
  
La clase **CAdviseSink** de MFCMAPI (mediante los archivos AdviseSink. h y AdviseSink. cpp) implementa el objeto de notificación de notificaciones para **** todas las llamadas a Advise. Para obtener más información acerca de MFCMAPI, vea [MFCMAPI como ejemplo de código](mfcmapi-as-a-code-sample.md) y [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

