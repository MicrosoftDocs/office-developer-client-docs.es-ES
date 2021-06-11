---
title: Objetos del proveedor de servicios MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432271"
---
# <a name="mapi-service-provider-objects"></a>Objetos del proveedor de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios implementan muchos objetos. Algunas se usan principalmente por MAPI y otras las usan las aplicaciones cliente. Todos los tipos de proveedores de servicios implementan algunos objetos; el resto son específicos de un único tipo de proveedor. En la tabla siguiente se describen todos los objetos del proveedor de servicios.
  
|**Objeto de proveedor de servicios**|**Descripción**|
|:-----|:-----|
|Contenedor de libreta de direcciones  <br/> |Contiene información de destinatarios para un proveedor de libreta de direcciones en el perfil activo; los proveedores de libreta de direcciones pueden tener uno o más contenedores de libreta de direcciones.  <br/> |
|Datos adjuntos  <br/> |Contiene datos adicionales, como un archivo u objeto OLE, que se asociarán a un mensaje.  <br/> |
|Control  <br/> |Habilita o deshabilita un botón e inicia el procesamiento cuando se hace clic en el botón.  <br/> |
|Lista de distribución  <br/> |Describe una agrupación de destinatarios de mensajes individuales.  <br/> |
|Carpeta  <br/> |Contiene mensajes y otros contenedores de mensajes.  <br/> |
|Inicio de sesión  <br/> |Controla la notificación de eventos del proveedor de servicios y las solicitudes de cliente.  <br/> |
|Usuario de mensajería  <br/> |Describe un destinatario individual de un mensaje.  <br/> |
|Mensaje  <br/> |Contiene información que se puede enviar a uno o varios destinatarios.  <br/> |
|Almacén de mensajes  <br/> |Actúa como una base de datos jerárquicamente organizada de mensajes.  <br/> |
|Proveedor  <br/> |Controla el inicio y apagado del proveedor de servicios.  <br/> |
|Gancho de cola  <br/> |Realiza un procesamiento especial en los mensajes entrantes y salientes.  <br/> |
|Estado  <br/> |Proporciona acceso al estado del proveedor de servicios.  <br/> |
|Tabla  <br/> |Proporciona acceso a una vista de resumen de los datos del objeto en formato de fila y columna, similar a una tabla de base de datos.  <br/> |
   
Todos los proveedores de servicios implementan un objeto de proveedor y un objeto de inicio de sesión. Los objetos de proveedor son estrictamente para la contabilidad; MAPI las usa para controlar los procesos de inicio y apagado. Los objetos de inicio de sesión se abaten indirectamente en algunas solicitudes de cliente. Por ejemplo, el objeto de inicio de sesión del proveedor del almacén de mensajes controla el registro de notificaciones y las solicitudes para abrir objetos de almacén de mensajes. 
  
Los objetos de proveedor y de inicio de sesión implementan una interfaz diferente en función del tipo de proveedor de servicios que proporciona la implementación. Un proveedor de almacén de mensajes implementa las interfaces [IMSProvider : IUnknown](imsprovideriunknown.md) e [IMSLogon : IUnknown](imslogoniunknown.md) en sus objetos de proveedor y de inicio de sesión, un proveedor de libreta de direcciones implementa las interfaces [IABProvider : IUnknown](iabprovideriunknown.md) e [IABLogon : IUnknown : IUnknown](iablogoniunknown.md) y un proveedor de transporte implementa las interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) e [IXPLogon : IUnknown.](ixplogoniunknown.md) 
  
Los proveedores de enlaces de mensajes implementan objetos de enlace de cola de cola u objetos que filtran los mensajes entrantes y salientes.
  
Los proveedores de servicios suelen usar solo unos pocos objetos. Con más frecuencia, usan un objeto de soporte técnico que MAPI proporciona para ayudar a implementar solicitudes de cliente. El objeto de soporte técnico se personaliza para el tipo de proveedor que lo usa. Para todos los proveedores de servicios, el objeto de soporte incluye métodos para controlar la notificación de eventos, mostrar propiedades de configuración, abrir objetos y controlar errores. El resto de los métodos son específicos de su uso; hay versiones personalizadas para la libreta de direcciones, el almacén de mensajes y los proveedores de transporte, y para la compatibilidad con la configuración. Por ejemplo, el objeto de soporte de la libreta de direcciones muestra detalles y cuadros de diálogo de destinatarios personalizados. El objeto de soporte del almacén de mensajes admite operaciones de copia y movimiento para carpetas y mensajes. El objeto de soporte del proveedor de transporte incluye métodos para facilitar la interacción con la cola MAPI. 
  
Algunos proveedores de servicios usan objetos de datos de tabla y de propiedad, objetos de utilidad que implementa MAPI. Los objetos de datos de tabla permiten a los proveedores de servicios administrar los datos subyacentes de una tabla. Los objetos de datos de propiedad permiten a los proveedores de servicios establecer el acceso a objetos y propiedades. 
  
Los proveedores de transporte que admiten el formato de encapsulación neutro de transporte (TNEF) para transferir propiedades usan un objeto TNEF que MAPI implementa para admitir la [interfaz ITnef : IUnknown.](itnefiunknown.md) Para obtener más información, vea [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Vea también



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desarrollo de un proveedor TNEF-Enabled transporte](developing-a-tnef-enabled-transport-provider.md)

