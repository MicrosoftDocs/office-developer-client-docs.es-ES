---
title: Objetos de proveedor de servicio MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 505b27b469a4ab197b41058ea5b933608818f0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818198"
---
# <a name="mapi-service-provider-objects"></a>Objetos de proveedor de servicio MAPI

  
  
**Hace referencia a**: Outlook 
  
Proveedores de servicios de implementan muchos objetos. Algunos se usan principalmente por MAPI y algunas se usan por las aplicaciones cliente. Algunos objetos se implementan todos los tipos de proveedores de servicios; el resto son específicos de un tipo de proveedor único. En la siguiente tabla se describe todos los objetos de proveedor de servicio.
  
|**Objeto de proveedor de servicio**|**Descripción**|
|:-----|:-----|
|Contenedor de la libreta de direcciones  <br/> |Contiene información de destinatarios para un proveedor de libreta de direcciones en el perfil activo; los proveedores de la libreta de direcciones pueden tener uno o varios contenedores de la libreta de direcciones.  <br/> |
|Datos adjuntos  <br/> |Contiene datos adicionales, como un archivo o un objeto OLE, que se asociará con un mensaje.  <br/> |
|Control  <br/> |Habilita o deshabilita un botón e inicia el procesamiento cuando se hace clic en el botón.  <br/> |
|Lista de distribución  <br/> |Describe una agrupación de destinatarios del mensaje individuales.  <br/> |
|Folder  <br/> |Contiene los mensajes y otros contenedores de mensaje.  <br/> |
|Inicio de sesión  <br/> |Controladores de solicitudes de notificación y cliente de evento de proveedor de servicio.  <br/> |
|Usuario de mensajería  <br/> |Describe a un destinatario individual de un mensaje.  <br/> |
|Message  <br/> |Contiene información que se puede enviar a uno o más destinatarios.  <br/> |
|Almacén de mensajes  <br/> |Actúa como una base de datos organizado jerárquicamente de mensajes.  <br/> |
|Proveedor  <br/> |Controladores de cierre e inicio del proveedor de servicio.  <br/> |
|Enlace de la cola de impresión  <br/> |Realiza procesamiento especial en los mensajes entrantes y salientes.  <br/> |
|Status  <br/> |Proporciona acceso al estado de un proveedor de servicios.  <br/> |
|Tabla  <br/> |Proporciona acceso a una vista de resumen de datos de objetos en formato de filas y columnas, similar a una tabla de base de datos.  <br/> |
   
Todos los proveedores de servicios de implementan un objeto de proveedor y un objeto de inicio de sesión. Objetos de proveedor de manera estricta son para contabilidad; se utilizan por MAPI para controlar los procesos de inicio y cierre. Objetos de inicio de sesión de servicio indirectamente algunas solicitudes de cliente. Por ejemplo, el mensaje de almacenar el registro de la notificación de identificadores de objeto del proveedor de inicio de sesión y las solicitudes para abrir los objetos de almacén de mensajes. 
  
Objetos de inicio de sesión y proveedor de implementar una interfaz diferente según el tipo de proveedor de servicios que proporciona la implementación. Implementa un proveedor de almacén de mensajes la [IMSProvider: IUnknown](imsprovideriunknown.md) y [IMSLogon: IUnknown](imslogoniunknown.md) interfaces en su proveedor y objetos de inicio de sesión, la dirección del libro proveedor implementa el [IABProvider: IUnknown](iabprovideriunknown.md) y [IABLogon: IUnknown](iablogoniunknown.md) interfaces y un proveedor de transporte implementa el [IXPProvider: IUnknown](ixpprovideriunknown.md) y [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces. 
  
Proveedores de enlace de mensaje implementan objetos de enlace de cola de impresión, u objetos que filtra los mensajes entrantes y salientes.
  
Proveedores de servicio normalmente usan solo unos pocos objetos. Con más frecuencia, utilizan un objeto de soporte técnico que MAPI se proporciona para ayudar a implementar las solicitudes de cliente. El objeto de soporte personalizado para el tipo de proveedor que lo está usando. Para todos los proveedores de servicio, el objeto de soporte incluye métodos para controlar la notificación de eventos, y se muestran las propiedades de configuración, abrir objetos y tratamiento de errores. El resto de los métodos son específicos de su uso; hay versiones personalizadas para libreta de direcciones, almacén de mensajes y los proveedores de transporte y para la compatibilidad con la configuración. Por ejemplo, el objeto de soporte técnico de la libreta de direcciones muestra detalles y cuadros de diálogo de destinatario personalizados. El almacén de mensajes admitir objeto admite copia y mover las operaciones de carpetas y mensajes. El objeto de soporte técnico del proveedor de transporte incluye métodos para facilitar la interacción con la cola de MAPI. 
  
Algunos proveedores de servicios utilizan objetos de datos de datos y la propiedad table: objetos de utilidad que implementa MAPI. Objetos de datos de tabla permiten a los proveedores de servicio administrar los datos subyacentes de una tabla. Objetos de datos de propiedad permiten a los proveedores de servicio configurar el acceso de objeto y propiedad. 
  
Los proveedores de transporte que admiten el formato de encapsulación neutro de transporte (TNEF) para la transferencia de las propiedades de usan un objeto TNEF que MAPI implementa para admitir el [ITnef: IUnknown](itnefiunknown.md) interfaz. Para obtener más información, vea [desarrollar un proveedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Vea también



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desarrollar un proveedor de transporte habilitado para TNEF](developing-a-tnef-enabled-transport-provider.md)

