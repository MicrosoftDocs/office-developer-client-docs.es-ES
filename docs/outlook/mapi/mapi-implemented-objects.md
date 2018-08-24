---
title: Objetos implementa MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d212a86aae0503a5e02a5a7ecddb83db10a4d664
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572378"
---
# <a name="mapi-implemented-objects"></a>Objetos implementa MAPI
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
MAPI implementa varios objetos para su uso por las aplicaciones cliente y los proveedores de servicios. El objeto de sesión permite a los clientes usar los servicios de sesión, para tener acceso a las tablas y para comunicarse con los proveedores de servicios. El objeto de la libreta de direcciones proporciona a los clientes con acceso integrado a todos los proveedores de libreta de direcciones diferente. 
  
MAPI proporciona varios objetos de tabla y el estado de los clientes puedan usar para ver y supervisar la información del proveedor de servicio y de la sesión. Por ejemplo, MAPI proporciona una tabla de perfil con información acerca de todos los perfiles que están instalados en el equipo y una tabla de servicios de mensaje con información acerca de todos los servicios de mensaje en el perfil actual. MAPI proporciona tres objetos de estado diferentes: uno que representa el subsistema de general, uno para la cola MAPI y otro para la libreta de direcciones integrada. 
  
MAPI implementa cuatro objetos diferentes para administrar la configuración de servicios de mensajes, los proveedores de servicios y los perfiles. Los clientes y proveedores de servicios de usan administración del proveedor y objetos de sección de perfil; estos objetos que puedan configurar proveedores de servicios y obtener acceso a las propiedades de perfil. Los clientes usan solo el servicio de mensajes y objetos de administración de perfiles, los objetos que admiten la administración de servicios de mensajes y los perfiles. 
  
MAPI proporciona dos objetos para los proveedores de servicio: un objeto de soporte técnico y un objeto TNEF. Todos los proveedores de servicio utilizan uno o más objetos de soporte técnico; Hay cuatro implementaciones de objetos de compatibilidad con diferentes. MAPI proporciona una implementación para admitir la configuración, así como implementaciones específicas para admitir la libreta de direcciones, almacén de mensajes y los proveedores de transporte. El objeto TNEF se usa en los proveedores de transporte que admiten el formato de encapsulación neutro de transporte (TNEF).
  
Dos objetos de utilidad, datos de la tabla y datos de propiedad, se suelen usar proveedores de servicios. Ayudarán de objetos de datos de tabla en la implementación de objetos de la tabla; Ayuda de objetos de datos (propiedad) para el conjunto y vista de acceso a la propiedad y la Ayuda en la implementación de [IMAPIProp: IUnknown](imapipropiunknown.md), la interfaz de la propiedad base. 
  
La tabla siguiente resume el propósito de cada objeto que implementa MAPI.
  
|**Objeto MAPI**|**Descripción**|
|:-----|:-----|
|Libreta de direcciones  <br/> |Proporciona acceso a la vista integrada de información del destinatario que pertenece a todos los proveedores de la libreta de direcciones en el perfil activo.  <br/> |
|Administración del servicio de mensajes  <br/> |Proporciona acceso a la información de servicio de mensaje para la configuración.  <br/> |
|Administración de perfiles  <br/> |Proporciona acceso a la información de perfil para la configuración.  <br/> |
|Sección de perfil  <br/> |Una parte de un perfil utilizado para describir un servicio de mensaje en particular o el proveedor de servicios.  <br/> |
|Datos (propiedad)  <br/> |Mantiene el acceso a las propiedades y ayuda a implementar **IMAPIProp**.  <br/> |
|Administración del proveedor  <br/> |Proporciona acceso a información del proveedor de servicio de configuración.  <br/> |
|Sesión  <br/> |Representa una conexión a sistemas de mensajería subyacentes y proporciona a los clientes con acceso a los recursos MAPI.  <br/> |
|Status  <br/> |Proporciona acceso al estado de la cola MAPI, la libreta de direcciones o el subsistema MAPI.  <br/> |
|Soporte técnico  <br/> |Ayuda a los proveedores de servicios de administrar las solicitudes de cliente.  <br/> |
|Tabla  <br/> |Proporciona acceso a una vista de resumen de datos de objetos en formato de filas y columnas, similar a una tabla de base de datos.  <br/> |
|Datos de la tabla  <br/> |Mantiene el acceso a datos de la tabla subyacente e implementa los objetos de la tabla.  <br/> |
|TNEF  <br/> |Admite el uso del formato de encapsulación neutro de transporte (TNEF).  <br/> |
   
En la siguiente ilustración se muestra la relación entre los objetos que implementa MAPI, las interfaces de la que heredan y los componentes que usan. 
  
**Objetos que MAPI implementa**
  
![Objetos que implementa MAPI] (media/amapi_68.gif "Objetos que implementa MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

