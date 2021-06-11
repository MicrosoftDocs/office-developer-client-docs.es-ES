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
  
La notificación de eventos es la comunicación de información entre dos objetos MAPI. A través de uno de los objetos, un cliente o proveedor de servicios se registra para la notificación de un cambio o error, denominado evento, que puede tener lugar en el otro objeto. Después de que se produzca el evento, se notificará al primer objeto del cambio o error. El objeto que recibe la notificación se denomina receptor de notificaciones; el objeto responsable de la notificación se denomina el origen del aviso.
  
Hay tres tipos de objetos receptores de aviso (todos los tipos son objetos MAPI estándar):
  
- Aconsejar objetos de receptor.   
- Formulario aconseja objetos de receptor.  
- Ver objetos de receptor de aviso.
    
Aconsejar que los objetos receptores sean el tipo más común. Las aplicaciones cliente suelen implementar receptores para recibir notificaciones de libreta de direcciones y almacén de mensajes y admitir la interfaz [IMAPIAdviseSink : IUnknown.](imapiadvisesinkiunknown.md) **IMAPIAdviseSink** contiene un único método, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Los receptores de aviso de formulario y vista son menos comunes; se implementan para recibir notificaciones sobre cambios en formularios personalizados. Los receptores de aviso de formulario admiten [la interfaz IMAPIFormAdviseSink: la interfaz IUnknown](imapiformadvisesinkiunknown.md) y los receptores de avisos de vista admiten la interfaz [IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) Dado que la mayoría de los clientes implementan objetos receptores de aviso estándar, supongamos que las discusiones de notificaciones se relacionan con notificaciones de libreta de direcciones y almacén de mensajes en lugar de notificaciones de formularios. Para obtener más información acerca de las notificaciones de formularios, vea [MAPI Forms Notifications](mapi-forms-notifications.md) and [Writing Form Server Code](writing-form-server-code.md).
  
Aconseje que los proveedores de servicios y MAPI implementen los objetos de origen. No todos los proveedores de servicios admiten la notificación de eventos; es opcional, pero se recomienda encarecidamente. Los proveedores de almacén de mensajes y libreta de direcciones suelen admitir notificaciones de objetos en varios de sus objetos y notificaciones de tabla en sus tablas de contenido y jerarquía. Los proveedores de transporte no admiten notificaciones directamente; se basan en métodos alternativos de comunicación con los clientes.
  
A diferencia de los receptores de aviso, los objetos de origen de aviso no son un tipo único de objeto MAPI. Muchos objetos MAPI, como almacenes de mensajes y tablas, pueden asumir el rol de origen de aviso. Un origen de aviso es cualquier objeto MAPI que haga lo siguiente:
  
- Implementa un método **Advise** para recibir registros de notificaciones. 
    
- Implementa un método **Unadvise** para recibir cancelaciones de notificaciones. 
    
- Genera notificaciones del tipo adecuado a los objetos receptores de aviso adecuados que se han registrado llamando a sus **métodos IMAPIAdviseSink::OnNotify.** 
    
Los clientes que implementan objetos receptores de avisos llaman a **Advise** cuando quieren registrarse para una notificación, en la mayoría de los casos pasando el identificador de entrada del objeto con el que debe producirse el registro y **Unadvise** cuando quieren cancelar el registro. Los clientes pasan un parámetro **a Advise** que indica cuál de los varios tipos de eventos que desea supervisar. **Advise** devuelve un número distinto de cero que representa una conexión correcta entre el receptor de avisos y el origen de aviso. 
  
Antes de llamar a **Advise,** los clientes pueden determinar si un proveedor de almacén de mensajes admite notificaciones comprobando que la marca STORE_NOTIFY_OK está establecida en la propiedad PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén de mensajes. No hay manera de que los clientes determinen con antelación si un proveedor de libreta de direcciones admite o no notificaciones. Los clientes deben intentar registrarse y, si se produce un error en el intento, pueden asumir que las notificaciones no son compatibles.
  
Cuando se produce un evento para el que se ha registrado un cliente, el origen del aviso notifica al receptor de notificaciones llamando a su método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) con una estructura de datos de notificación que contiene información sobre el evento. La implementación de **OnNotify** de un receptor de notificaciones puede realizar tareas en respuesta a la notificación, como actualizar datos en la memoria o actualizar una pantalla. 
  
Los proveedores de servicios pueden implementar la compatibilidad con las notificaciones manualmente o aprovechar la ayuda proporcionada en tres métodos **IMAPISupport:** [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)y [IMAPISupport::Notify](imapisupport-notify.md). Los **métodos Subscribe** y **Unsubscribe** controlan el registro y la anulación de registro de notificaciones para los proveedores; el **método Notify** controla el envío de notificaciones cuando corresponda. 
  
Para usar los métodos de objeto de soporte técnico para el registro de notificaciones, los proveedores de servicios llaman a [IMAPISupport::Subscribe](imapisupport-subscribe.md) en sus métodos **Advise** y pasan a **Subscribe** el puntero del receptor de notificaciones que los clientes pasan a **Advise**. Si se pasa un identificador de entrada como parámetro de entrada para especificar un origen de aviso, los proveedores de servicios lo convierten en una clave binaria. **Subscribe** crea un número de conexión único y es este número el que los proveedores de servicios devuelven a los clientes. Los proveedores de servicios pueden liberar el puntero de objeto de receptor de aviso del cliente en cualquier momento después de **que** se haya completado la llamada advise. 
  
Cuando los clientes llaman a **Unadvise** para cancelar un registro, los proveedores de servicios disminuyen el número de referencias en el puntero receptor de aviso del cliente o llaman a **Cancelar** suscripción para hacer lo mismo. 
  
Cuando es el momento de generar una notificación, los proveedores de servicios realizan cualquier procesamiento interno relacionado con la notificación e inicializan una estructura [notification](notification.md) estableciendo todos sus miembros no usados en cero. Esta técnica para inicializar la estructura **notification** puede ayudar a los clientes a crear implementaciones **onNotify** más pequeñas, rápidas y menos propensas a errores. 
  
En la siguiente ilustración se muestra la comunicación entre los objetos de receptor advise, advise source objects y MAPI. MAPI solo interviene cuando el origen del aviso llama a los **métodos IMAPISupport** para la compatibilidad con notificaciones. 
  
**Llamadas de notificación de eventos**
  
![Llamadas de notificación de eventos Llamadas]de notificación de(media/amapi_51.gif "eventos")
  
La clase **CAdviseSink** de MFCMAPI (mediante los archivos AdviseSink.h y AdviseSink.cpp) implementa el objeto de receptor advise para todas las llamadas a **Advise**. Para obtener más información acerca de MFCMAPI, vea [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md) y [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

