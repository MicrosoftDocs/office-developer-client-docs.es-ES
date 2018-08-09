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
ms.openlocfilehash: fb37c15e6544798a956e865e6c8c6d62bee44d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818096"
---
# <a name="mapi-client-objects"></a>Objetos de cliente MAPI
  
**Hace referencia a**: Outlook 
  
Aplicaciones de cliente de mensajería estándar implementan un solo objeto, un receptor de notificaciones. Aviso receptores de heredan de la [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) de la interfaz y se usan por MAPI y los proveedores de notificación de eventos de servicios. Algunos clientes también implementan objetos de progreso para admitir la presentación de cuadros de diálogo de progreso. 
  
Los clientes más complejos que los formularios personalizados de soporte técnico implementan advise otro receptor de objeto y algunos otros objetos, como el objeto de sitio de mensaje que hereda de la [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interfaz y el objeto de contexto de vista que herede de la [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interfaz. El objeto de receptor advise adicionales hereda el [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interfaz. 
  
En la siguiente tabla se resume los objetos MAPI se implementa por los clientes de mensajería estándares y los clientes que admiten la visualización de los formularios personalizados.
  
|**Objeto de cliente**|**Descripción**|
|:-----|:-----|
|Receptor de aviso  <br/> |Proporciona una función de devolución de llamada para los eventos que se producen en el almacén de mensajes, la libreta de direcciones o la sesión.  <br/> |
|Sitio de mensaje  <br/> |Administra la manipulación de objetos de formulario.  <br/> |
|Progress  <br/> |Muestra un cuadro de diálogo para mostrar el progreso de una operación.  <br/> |
|Vista de aviso receptor  <br/> |Proporciona funciones de devolución de llamada para los eventos que se producen en un formulario.  <br/> |
|Contexto de vista  <br/> |Admite comandos para imprimir y guardar formularios y para navegar entre formularios.  <br/> |
   
En la siguiente ilustración se muestra la relación entre estos objetos de cliente distinto, las interfaces de la que heredan y los componentes MAPI que usan. 
  
![Objetos de cliente y las interfaces correspondientes] (media/amapi_65.gif "Objetos de cliente y las interfaces correspondientes")
  
Los clientes usan muchos más objetos que implementan. Todos los clientes de usar un objeto de sesión para obtener acceso a una amplia variedad de objetos que implementa MAPI y objetos de proveedor de servicio. Los clientes interactúan con los proveedores de servicios indirectamente, a través de la sesión, la libreta de direcciones o los objetos de estado que suministran los MAPI, o directamente a través de una variedad de objetos que implementan los proveedores de servicio en particular. Para hacer que un contacto directo con los proveedores de la libreta de direcciones, los clientes usan contenedores de libretas de direcciones, los usuarios y las listas de distribución de mensajería. Para obtener acceso a un proveedor de almacén de mensajes, los clientes utilizan directamente el objeto de almacén de mensajes, carpetas, mensajes y datos adjuntos. Cuando los proveedores de servicios son compatibles con un objeto de estado, los clientes pueden utilizar el objeto de estado para supervisar el estado de un proveedor de servicios.
  
Los clientes que admiten el proveedor de servicios y la configuración del servicio de mensaje usan tres objetos que implementa MAPI: el objeto de administración del servicio de message, el objeto de perfil de administración y el objeto de proveedor de administración. Los clientes que mostrar formularios personalizados usan varios objetos de formulario que implementa un proveedor de la biblioteca de formulario o un servidor de formulario.
  
## <a name="see-also"></a>Vea también

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

