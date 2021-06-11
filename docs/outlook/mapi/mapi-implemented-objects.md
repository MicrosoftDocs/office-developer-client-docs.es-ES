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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430633"
---
# <a name="mapi-implemented-objects"></a>Objetos implementados por MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI implementa varios objetos para su uso por parte de las aplicaciones cliente y los proveedores de servicios. El objeto de sesión permite a los clientes usar servicios de sesión, acceder a tablas y comunicarse con proveedores de servicios. El objeto de libreta de direcciones proporciona a los clientes acceso integrado a todos los diferentes proveedores de libreta de direcciones. 
  
MAPI proporciona varios objetos de tabla y estado para que los clientes los usen para ver y supervisar la información del proveedor de servicios y sesiones. Por ejemplo, MAPI proporciona una tabla de perfiles con información sobre todos los perfiles instalados en el equipo y una tabla de servicio de mensajes con información sobre todos los servicios de mensajes del perfil actual. MAPI proporciona tres objetos de estado diferentes: uno que representa el subsistema general, uno para la cola MAPI y otro para la libreta de direcciones integrada. 
  
MAPI implementa cuatro objetos diferentes para administrar la configuración de servicios de mensajes, proveedores de servicios y perfiles. Tanto los clientes como los proveedores de servicios usan objetos de sección de perfiles y administración del proveedor; estos objetos les permiten configurar proveedores de servicios y obtener acceso a las propiedades de perfil. Los clientes solo usan objetos de administración de perfiles y servicio de mensajes, los objetos que admiten la administración de perfiles y servicios de mensajes. 
  
MAPI proporciona dos objetos para proveedores de servicios: un objeto de soporte técnico y un objeto TNEF. Todos los proveedores de servicios usan uno o varios objetos de soporte técnico; hay cuatro implementaciones de objetos de soporte técnico diferentes. MAPI proporciona una implementación para admitir la configuración, así como implementaciones específicas para admitir la libreta de direcciones, el almacén de mensajes y los proveedores de transporte. Los proveedores de transporte que admiten el formato de encapsulación neutral de transporte (TNEF) usan el objeto TNEF.
  
Los proveedores de servicios suelen usar dos objetos de utilidad, datos de tabla y datos de propiedades. Objetos de datos de tabla ayuda en la implementación de objetos de tabla; objetos de datos de propiedad ayudan a establecer y ver el acceso a propiedades y ayuda en la implementación de [IMAPIProp : IUnknown](imapipropiunknown.md), la interfaz de la propiedad base. 
  
En la tabla siguiente se resume el propósito de cada objeto que implementa MAPI.
  
|**Objeto MAPI**|**Descripción**|
|:-----|:-----|
|Libreta de direcciones  <br/> |Proporciona acceso a la vista integrada de la información de destinatarios que pertenece a todos los proveedores de libreta de direcciones del perfil activo.  <br/> |
|Administración del servicio de mensajes  <br/> |Proporciona acceso a la información del servicio de mensajes para la configuración.  <br/> |
|Administración de perfiles  <br/> |Proporciona acceso a la información de perfil para la configuración.  <br/> |
|Sección Perfil  <br/> |Parte de un perfil usado para describir un servicio de mensajes o un proveedor de servicios en particular.  <br/> |
|Datos de propiedad  <br/> |Mantiene el acceso a las propiedades y ayuda a implementar **IMAPIProp**.  <br/> |
|Administración del proveedor  <br/> |Proporciona acceso a la información del proveedor de servicios para la configuración.  <br/> |
|Sesión  <br/> |Representa una conexión a sistemas de mensajería subyacentes y proporciona a los clientes acceso a recursos MAPI.  <br/> |
|Estado  <br/> |Proporciona acceso al estado del subsistema MAPI, la libreta de direcciones o la cola MAPI.  <br/> |
|Soporte técnico  <br/> |Ayuda a los proveedores de servicios a administrar las solicitudes de cliente.  <br/> |
|Tabla  <br/> |Proporciona acceso a una vista de resumen de los datos del objeto en formato de fila y columna, similar a una tabla de base de datos.  <br/> |
|Datos de tabla  <br/> |Mantiene el acceso a los datos de tabla subyacentes e implementa objetos de tabla.  <br/> |
|TNEF  <br/> |Admite el uso del formato de encapsulación neutro de transporte (TNEF).  <br/> |
   
En la siguiente ilustración se muestra la relación entre los objetos que implementa MAPI, las interfaces de las que heredan y los componentes que los usan. 
  
**Objetos que MAPI implementa**
  
![Objetos que MAPI implementa objetos]que implementa(media/amapi_68.gif "MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

