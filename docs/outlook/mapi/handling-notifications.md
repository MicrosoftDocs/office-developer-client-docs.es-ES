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
  
Las notificaciones permiten que un objeto informe a otro objeto que ha sufrido un cambio. El tipo de cambio se conoce como un evento. MAPI define varios eventos para los que se generan notificaciones. 
  
Los clientes suelen registrarse para uno o más eventos con uno o más objetos. Estos objetos se conocen como orígenes de notificaciones. Los objetos que pueden actuar como orígenes de notificaciones incluyen el objeto de sesión, bajo el control de MAPI, o un objeto creado por un proveedor de servicios, como un mensaje. El objeto informado, al que se conoce como el receptor de notificaciones, contiene una implementación de la interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) o la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y está dentro de una aplicación cliente. 
  
Aconseje a los objetos **** de origen que implementen un método Advise, al que llaman los clientes para registrarse para notificaciones y un método unaconsejable, al que se llama para cancelar un registro. **** Uno de los parámetros de **Advise** es un puntero a una implementación de **IMAPIAdviseSink** o * * IMAPIViewAdviseSink * *. El origen Advise almacena en caché este puntero para que pueda llamar a [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) o a uno de los métodos de **IMAPIViewAdviseSink** cuando se produzca un cambio. 
  
Como la recepción de notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes se registren y controlen las notificaciones. Sin embargo, es opcional.
  
## <a name="in-this-section"></a>En esta sección

- [Registro para una notificación](registering-for-a-notification.md): describe cómo registrar un cliente para las notificaciones como parte de su proceso de inicialización.
    
- [Cancelación de una notificación](canceling-a-notification.md): describe cómo cancelar una suscripción a una notificación.
    
- [Administración](handling-message-store-notification.md)de notificaCiones del almacén de mensajes: describe cómo registrarse para recibir notificaciones del almacén de mensajes.
    
- [Entrega](handing-address-book-notification.md)de notificaciones de la libreta de direcciones: describe cómo registrar y administrar las notificaciones de la libreta de direcciones.
    
- [Notificación](handling-table-notification.md)de la tabla de administración: describe cómo registrar las notificaciones en la tabla de jerarquías.
    
- [Implementar un objeto de receptor](implementing-an-advise-sink-object.md)de notificaciones: describe cómo implementar un objeto de receptor de notificaciones.
    
- [Cronometrar una notificación](timing-a-notification.md): describe el momento de la notificación del cliente por proveedores de servicios.
    
- [Garantizar una notificación de seguridad para](ensuring-a-thread-safe-notification.md)subprocesos: describe cómo garantizar la notificación de seguridad para subprocesos con MAPI.
    
- [Forzar una notificación](forcing-a-notification.md): describe cómo forzar una notificación en MAPI.
    

