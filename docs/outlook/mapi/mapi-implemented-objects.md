---
title: Objetos implementados por MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 86aa8451b5b127764134f1a3a905366fd014d0c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346861"
---
# <a name="mapi-implemented-objects"></a>Objetos implementados por MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI implementa varios objetos para su uso por parte de las aplicaciones cliente y los proveedores de servicios. El objeto Session permite a los clientes usar los servicios de sesión, tener acceso a tablas y comunicarse con proveedores de servicios. El objeto de la libreta de direcciones proporciona a los clientes acceso integrado a todos los distintos proveedores de la libreta de direcciones. 
  
MAPI proporciona varios objetos de tabla y estado para que los clientes los usen para ver y supervisar la información del proveedor de servicios y sesiones. Por ejemplo, MAPI proporciona una tabla de perfil con información acerca de todos los perfiles instalados en el equipo y una tabla de servicio de mensajes con información sobre todos los servicios de mensajes del perfil actual. MAPI proporciona tres objetos de estado diferentes: uno que representa el subsistema general, uno para la cola MAPI y otro para la libreta de direcciones integrada. 
  
MAPI implementa cuatro objetos diferentes para administrar la configuración de los servicios de mensajes, los proveedores de servicios y los perfiles. Los clientes y los proveedores de servicios usan los objetos de sección de perfil y administración de proveedores; Estos objetos les permiten configurar proveedores de servicios y las propiedades de Perfil de acceso. Los clientes solo usan los objetos de servicio de mensajes y de administración de perfiles, los objetos que admiten la administración de los servicios de mensajes y los perfiles. 
  
MAPI proporciona dos objetos para proveedores de servicios: un objeto de compatibilidad y un objeto TNEF. Todos los proveedores de servicios usan uno o varios objetos de soporte; Hay cuatro implementaciones de objetos de compatibilidad diferentes. MAPI proporciona una implementación para admitir la configuración, así como implementaciones específicas para admitir la libreta de direcciones, el almacén de mensajes y los proveedores de transporte. El objeto TNEF lo utilizan los proveedores de transporte que admiten el formato de encapsulación neutro para el transporte (TNEF).
  
Los proveedores de servicios suelen usar dos objetos de utilidad, datos de tabla y datos de propiedad. Los objetos de datos de tabla ayudan en la implementación de objetos Table; los objetos de datos de propiedad ayudan a establecer y ver el acceso a las propiedades y la ayuda en la implementación de [IMAPIProp: IUnknown](imapipropiunknown.md), la interfaz de propiedades base. 
  
En la tabla siguiente se resume el propósito de cada objeto que implementa MAPI.
  
|**Objeto MAPI**|**Descripción**|
|:-----|:-----|
|Libreta de direcciones  <br/> |Proporciona acceso a la vista integrada de la información de destinatarios que pertenece a todos los proveedores de la libreta de direcciones del perfil activo.  <br/> |
|Administración del servicio de mensajes  <br/> |Proporciona acceso a la información del servicio de mensajes para la configuración.  <br/> |
|Administración de perfiles  <br/> |Proporciona acceso a la información de Perfil de configuración.  <br/> |
|Sección de perfil  <br/> |Parte de un perfil que se usa para describir un servicio de mensajes o un proveedor de servicios en particular.  <br/> |
|Datos de propiedad  <br/> |Mantiene el acceso a las propiedades y ayuda a implementar **IMAPIProp**.  <br/> |
|Administración del proveedor  <br/> |Proporciona acceso a la información del proveedor de servicios para la configuración.  <br/> |
|Session  <br/> |Representa una conexión a los sistemas de mensajería subyacentes y proporciona a los clientes acceso a los recursos de MAPI.  <br/> |
|Estado  <br/> |Proporciona acceso al estado del subsistema MAPI, la libreta de direcciones o la cola de impresión MAPI.  <br/> |
|Soporte técnico  <br/> |Ayuda a los proveedores de servicios a administrar las solicitudes de los clientes.  <br/> |
|Table  <br/> |Proporciona acceso a una vista de Resumen de los datos de objeto en formato de fila y columna, al igual que una tabla de base de datos.  <br/> |
|Datos de la tabla  <br/> |Mantiene el acceso a los datos de la tabla subyacente e implementa objetos Table.  <br/> |
|TNEF  <br/> |Admite el uso del formato de encapsulamiento neutro para el transporte (TNEF).  <br/> |
   
En la siguiente ilustración se muestra la relación entre los objetos que implementa MAPI, las interfaces desde las que heredan y los componentes que los usan. 
  
**Objetos que MAPI implementa**
  
![Objetos que implementa MAPI] (media/amapi_68.gif "Objetos que implementa MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

