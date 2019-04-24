---
title: Objetos de proveedor de servicios MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251608"
---
# <a name="mapi-service-provider-objects"></a>Objetos de proveedor de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios implementan muchos objetos. Algunas son utilizadas principalmente por MAPI y otras las usan las aplicaciones cliente. Algunos objetos se implementan por todos los tipos de proveedores de servicios; el resto son específicos de un tipo de proveedor único. En la tabla siguiente se describen todos los objetos de proveedor de servicios.
  
|**Objeto de proveedor de servicios**|**Descripción**|
|:-----|:-----|
|Contenedor de libreta de direcciones  <br/> |Contiene la información de destinatario de un proveedor de libreta de direcciones en el perfil activo; los proveedores de libretas de direcciones pueden tener uno o varios contenedores de libretas de direcciones.  <br/> |
|Datos adjuntos  <br/> |Contiene datos adicionales, como un archivo o un objeto OLE, que se van a asociar a un mensaje.  <br/> |
|Control  <br/> |Habilita o deshabilita un botón e inicia el procesamiento cuando se hace clic en el botón.  <br/> |
|Lista de distribución  <br/> |Describe una agrupación de destinatarios individuales de un mensaje.  <br/> |
|Folder  <br/> |Contiene mensajes y otros contenedores de mensajes.  <br/> |
|Inicio de sesión  <br/> |Controla las solicitudes de cliente y las notificaciones de eventos del proveedor de servicios.  <br/> |
|Usuario de mensajería  <br/> |Describe un destinatario individual de un mensaje.  <br/> |
|Mensaje  <br/> |Contiene información que se puede enviar a uno o más destinatarios.  <br/> |
|Almacén de mensajes  <br/> |Actúa como una base de datos de mensajes organizada jerárquicamente.  <br/> |
|Proveedor  <br/> |Controla el inicio y el cierre de un proveedor de servicios.  <br/> |
|Enlace de cola de impresión  <br/> |Realiza un procesamiento especial en los mensajes entrantes y salientes.  <br/> |
|Estado  <br/> |Proporciona acceso al estado del proveedor de servicios.  <br/> |
|Table  <br/> |Proporciona acceso a una vista de Resumen de los datos de objeto en formato de fila y columna, al igual que una tabla de base de datos.  <br/> |
   
Todos los proveedores de servicios implementan un objeto de proveedor y un objeto de inicio de sesión. Los objetos de proveedor son estrictamente para la contabilidad; MAPI los usa para controlar los procesos de inicio y cierre. Los objetos de inicio de sesión el servicio de algunas solicitudes de cliente indirectamente. Por ejemplo, el objeto de inicio de sesión del proveedor de almacenamiento de mensajes controla las solicitudes y el registro de las notificaciones para abrir objetos de almacén de mensajes. 
  
Los objetos de proveedor e inicio de sesión implementan una interfaz diferente según el tipo de proveedor de servicios que proporciona la implementación. Un proveedor de almacenamiento de mensajes implementa las interfaces [IMSProvider: IUnknown](imsprovideriunknown.md) y [IMSLogon: IUnknown](imslogoniunknown.md) en sus objetos de inicio de sesión y proveedor, un proveedor de libreta de direcciones implementa la [IABProvider: IUnknown](iabprovideriunknown.md) y [IABLogon: IUnknown](iablogoniunknown.md) interfaces y un proveedor de transporte implementa las interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) y [IXPLogon: IUnknown](ixplogoniunknown.md) . 
  
Los proveedores de enlace de mensajes implementan objetos de enlace de cola o los objetos que filtran los mensajes entrantes y salientes.
  
Por lo general, los proveedores de servicios usan unos pocos objetos. Con más frecuencia, usan un objeto de soporte que MAPI proporciona para ayudar a implementar solicitudes de clientes. El objeto support se personaliza para el tipo de proveedor que lo usa. Para todos los proveedores de servicios, el objeto support incluye métodos para controlar la notificación de eventos, mostrar propiedades de configuración, abrir objetos y controlar errores. El resto de los métodos son específicos de su uso; hay versiones personalizadas para la libreta de direcciones, el almacén de mensajes y los proveedores de transporte, y para la compatibilidad con la configuración. Por ejemplo, el objeto compatibilidad con libreta de direcciones muestra detalles y cuadros de diálogo de destinatarios personalizados. El objeto de soporte del almacén de mensajes admite operaciones de copiar y mover para carpetas y mensajes. El objeto de soporte de proveedor de transporte incluye métodos para facilitar la interacción con la cola MAPI. 
  
Algunos proveedores de servicios usan datos de tabla y objetos de datos de propiedad (objetos de utilidad que implementa MAPI). Los objetos de datos de tabla permiten a los proveedores de servicios administrar los datos subyacentes de una tabla. Los objetos de datos de propiedad habilitan a los proveedores de servicios para establecer el acceso a objetos y propiedades. 
  
Los proveedores de transporte que admiten el formato de encapsulación neutro para el transporte (TNEF) para transferir propiedades usan un objeto TNEF que MAPI implementa para admitir la interfaz [ITnef: IUnknown](itnefiunknown.md) . Para obtener más información, vea [desarrollar un proveedor de transporte habilitaDo para TNEF](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Vea también



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desarrollar un proveedor de transporte habilitado para TNEF](developing-a-tnef-enabled-transport-provider.md)

