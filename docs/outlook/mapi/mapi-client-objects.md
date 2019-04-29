---
title: Objetos de cliente MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412411"
---
# <a name="mapi-client-objects"></a>Objetos de cliente MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente de mensajería estándar implementan solo un objeto: un receptor de notificaciones. Los receptores de notificaciones heredan de la interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) y se usan en MAPI y los proveedores de servicios para la notificación de eventos. Algunos clientes también implementan objetos Progress para admitir la presentación de cuadros de diálogo de progreso. 
  
Los clientes más complejos que admiten formularios personalizados implementan otro objeto de notificación de notificaciones y otros objetos, como el objeto de sitio de mensaje que hereda de la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) y el objeto de contexto de vista que hereda de la [IMAPIViewContext: interfaz IUnknown](imapiviewcontextiunknown.md) . El objeto del receptor de notificaciones adicionales hereda de la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . 
  
En la tabla siguiente se resumen los objetos MAPI que implementan los clientes de mensajería estándar y los clientes que admiten la visualización de formularios personalizados.
  
|**Objeto de cliente**|**Descripción**|
|:-----|:-----|
|Notificar al receptor  <br/> |Proporciona una función de devolución de llamada para los eventos que se producen en el almacén de mensajes, la libreta de direcciones o la sesión.  <br/> |
|Sitio de mensajes  <br/> |Controla la manipulación de objetos de formulario.  <br/> |
|Progress  <br/> |Muestra un cuadro de diálogo para mostrar el progreso de una operación.  <br/> |
|Ver el receptor de notificaciones  <br/> |Proporciona funciones de devolución de llamada para los eventos que se producen en un formulario.  <br/> |
|Contexto de la vista  <br/> |Admite comandos para imprimir y guardar formularios, y para navegar entre formularios.  <br/> |
   
En la siguiente ilustración se muestra la relación entre estos objetos de cliente diferentes, las interfaces desde las que heredan y los componentes MAPI que los usan. 
  
![Objetos de cliente y sus interfaces correspondientes] (media/amapi_65.gif "Objetos de cliente y sus interfaces correspondientes")
  
Los clientes usan muchos más objetos de los que implementan. Todos los clientes usan un objeto Session para obtener acceso a una amplia variedad de objetos de proveedor de servicios y objetos que implementa MAPI. Los clientes interactúan con los proveedores de servicios de forma indirecta, a través de la sesión, la libreta de direcciones o los objetos de estado que proporciona MAPI, o directamente a través de una variedad de objetos que implementan determinados proveedores de servicios. Para establecer un contacto directo con los proveedores de la libreta de direcciones, los clientes usan contenedores de libretas de direcciones, usuarios de mensajería y listas de distribución. Para obtener acceso directamente a un proveedor de almacenamiento de mensajes, los clientes usan el objeto, las carpetas, los mensajes y los datos adjuntos del almacén de mensajes. Cuando los proveedores de servicios admiten un objeto de estado, los clientes pueden usar el objeto de estado para supervisar el estado del proveedor de servicios.
  
Los clientes que admiten el proveedor de servicios y la configuración del servicio de mensajes usan tres objetos que implementa MAPI: el objeto de administración del servicio de mensajes, el objeto de administración de perfiles y el objeto de administración del proveedor. Los clientes que muestran formularios personalizados usan varios objetos de formulario que implementa un proveedor de bibliotecas de formularios o un servidor de formularios.
  
## <a name="see-also"></a>Ver también

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

