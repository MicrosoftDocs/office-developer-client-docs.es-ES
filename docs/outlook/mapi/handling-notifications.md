---
title: Administrar notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567583"
---
# <a name="handling-notifications"></a>Administrar notificaciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones de habilitar un objeto informar a otro objeto que ha experimentado un cambio. El tipo de cambio se conoce como un evento. MAPI define varios eventos para el que se generan notificaciones. 
  
Normalmente, los clientes de registrar los eventos de uno o más con uno o más objetos. Estos objetos se conocen como orígenes de aviso. Los objetos que pueden actuar como orígenes de aviso incluyen el objeto de sesión, bajo control de MAPI o un objeto creado por un proveedor de servicios, como un mensaje. El objeto informado, que se conoce como el receptor de notificaciones, contiene puede ser una implementación de la [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interfaz o el [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) de la interfaz y está dentro de una aplicación cliente. 
  
Objetos de origen de Advise implementan un método **Advise** , que se llama a los clientes para registrar las notificaciones y un método **Unadvise** , que se llama para cancelar un registro. Uno de los parámetros a **Advise** es un puntero a una implementación de **IMAPIAdviseSink** o ** IMAPIViewAdviseSink **. El origen de advise se almacena en caché en este puntero para que pueda llamar [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) o uno de los métodos en **IMAPIViewAdviseSink** cuando se produce un cambio. 
  
Debido a que recibir notificaciones permite a los usuarios ver la información más actualizada, se recomienda que todos los clientes de registrarse para obtener y controlan las notificaciones. Sin embargo, es opcional.
  
## <a name="in-this-section"></a>En esta sección

- [Registrar para una notificación](registering-for-a-notification.md): se describe cómo registrar un cliente para las notificaciones como parte de su proceso de inicialización.
    
- [Cancelación de una notificación](canceling-a-notification.md): se describe cómo cancelar una suscripción a una notificación.
    
- [Controlar la notificación del almacén de mensaje](handling-message-store-notification.md): se describe cómo registrarse para las notificaciones del almacén de mensajes.
    
- [Tener que proporcionar la notificación de la libreta de direcciones](handing-address-book-notification.md): describe cómo registrarse para obtener y controlar las notificaciones de la libreta de direcciones.
    
- [Controlar la notificación de tabla](handling-table-notification.md): describe cómo registrarse para recibir notificaciones de la tabla de jerarquía.
    
- [Implementación de un objeto de receptor de aviso](implementing-an-advise-sink-object.md): describe cómo implementar un objeto de receptor advise.
    
- [Una notificación de intervalos de tiempo](timing-a-notification.md): describe los intervalos de notificación de cliente por los proveedores de servicio.
    
- [Garantizar una notificación de subprocesos](ensuring-a-thread-safe-notification.md): describe cómo asegurar la notificación de seguros para subprocesos con MAPI.
    
- [Forzar una notificación](forcing-a-notification.md): se describen los procedimientos para forzar una notificación en MAPI.
    

