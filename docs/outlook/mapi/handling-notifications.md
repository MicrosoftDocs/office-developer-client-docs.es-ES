---
title: Administrar las notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429162"
---
# <a name="handling-notifications"></a>Administrar las notificaciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones permiten a un objeto informar a otro de que se ha sometido a un cambio. El tipo de cambio se denomina evento. MAPI define varios eventos para los que se generan notificaciones. 
  
Normalmente, los clientes se registran para uno o más eventos con uno o más objetos. Estos objetos se denominan fuentes de aviso. Los objetos que pueden actuar como orígenes de aviso incluyen el objeto de sesión, bajo el control de MAPI, o un objeto creado por un proveedor de servicios, como un mensaje. El objeto informado, denominado receptor de avisos, contiene una implementación de la interfaz [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) o [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) y se encuentra dentro de una aplicación cliente. 
  
Los objetos de origen de aviso implementan un **método Advise,** al que los clientes llaman para registrarse para recibir notificaciones, y un método **Unadvise,** al que se llama para cancelar un registro. Uno de los parámetros que **se** deben aconsejar es un puntero a una implementación de **IMAPIAdviseSink** o ** IMAPIViewAdviseSink **. El origen de aviso almacena en caché este puntero para que pueda llamar a [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) o a uno de los métodos de **IMAPIViewAdviseSink** cuando se produce un cambio. 
  
Dado que la recepción de notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes se registren y controlan las notificaciones. Sin embargo, es opcional.
  
## <a name="in-this-section"></a>En esta sección

- [Registro de una notificación:](registering-for-a-notification.md)describe cómo registrar un cliente para notificaciones como parte de su proceso de inicialización.
    
- [Cancelar una notificación:](canceling-a-notification.md)describe cómo cancelar una suscripción a una notificación.
    
- [Control de la notificación del almacén de](handling-message-store-notification.md)mensajes: describe cómo registrarse para las notificaciones del almacén de mensajes.
    
- [Notificación de libreta de direcciones](handing-address-book-notification.md)de entrega: describe cómo registrarse y administrar las notificaciones de la libreta de direcciones.
    
- [Controlar la notificación de tabla:](handling-table-notification.md)describe cómo registrar las notificaciones de la tabla de jerarquía.
    
- [Implementación de un objeto receptor de aviso:](implementing-an-advise-sink-object.md)describe cómo implementar un objeto receptor de aviso.
    
- [Temporización de una](timing-a-notification.md)notificación: describe el momento en que los proveedores de servicios han recibido una notificación de cliente.
    
- [Garantizar una notificación Thread-Safe:](ensuring-a-thread-safe-notification.md)describe cómo garantizar una notificación segura para subprocesos con MAPI.
    
- [Forzar una notificación:](forcing-a-notification.md)describe cómo forzar una notificación en MAPI.
    

