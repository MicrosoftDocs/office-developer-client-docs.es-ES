---
title: Información general del objeto de soporte técnico
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ecc5439b4abbbfd920fba5456db7462f7967388f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820776"
---
# <a name="support-object-overview"></a>Información general del objeto de soporte técnico

  
  
**Hace referencia a**: Outlook 
  
MAPI proporciona un objeto de soporte técnico, un objeto que implementa el [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz, para todos los proveedores de servicio durante el inicio de sesión y para todos los servicios de mensaje durante la configuración. 
  
Compatibilidad con objetos no son accesibles para los clientes; se implementan mediante MAPI y llamados sólo por los proveedores de servicios. La interfaz **IMAPISupport** se especifica en el archivo de encabezado Mapispi.h. Su identificador es IID_IMAPISup y su tipo de puntero es LPMAPISUP. Se exponen propiedades MAPI por compatibilidad con objetos. 
  
Un proveedor puede tener uno o más objetos de soporte técnico, según el número de veces que el proveedor de los registros de MAPI en o el número de veces que se denomina función de entrada de servicio de mensajes del proveedor. Normalmente, un proveedor se registrarán al menos una vez por sesión. Los proveedores de transporte y de la libreta de direcciones se registran cada vez que un cliente inicia una sesión con una entrada de perfil que solicita de ellos. Los proveedores de almacén de mensajes se registran cada vez que un cliente llama al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
En el caso de múltiples inicios de sesión en una sesión, puede elegir a conservar y utilizar cada objeto de soporte técnico por separado o a conservar y utilizar sólo la primera, descartar cada objeto de soporte técnico posteriores. Para conservar un objeto de soporte técnico, llame al método **IUnknown:: AddRef** . Una llamada a **AddRef** en un objeto de soporte técnico que desea conservar a lo largo de una sesión es extremadamente importante; Si no se realiza la llamada, MAPI libera el objeto de soporte técnico y libera su memoria. 
  
El propósito del objeto de soporte consiste en proporcionar implementaciones para un número bastante grande de métodos utilizadas frecuentemente por los proveedores. Cada objeto de soporte técnico también contiene datos contextuales específicos de su propia instancia, como la sesión que se está ejecutando el proveedor en la sección de perfil que se está usando el proveedor y la información de error de la sesión. 
  
Hay cuatro tipos diferentes de objetos de soporte técnico: uno para cada tipo de proveedor principales (la libreta de direcciones, almacén de mensajes y transporte) y otro para la compatibilidad con la configuración. 
  
MAPI personaliza cada objeto de soporte técnico mediante la inclusión de las implementaciones de métodos que son relevantes para su uso. Las implementaciones de algunos métodos, como [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), se incluyen en todos los objetos de soporte técnico. Las implementaciones de otros métodos, como [SpoolerNotify](imapisupport-spoolernotify.md), se aplican únicamente a objetos de asistencia determinado. Almacén de mensajes sólo y los proveedores de transporte pueden usar este método; Cuando un proveedor de la libreta de direcciones o un servicio de mensajes intenta llamar a él, MAPI devuelve MAPI_E_NO_SUPPORT.
  
Compatibilidad con objetos se pueden usar para realizar muchas tareas, como las siguientes:
  
- Obtener acceso a una sección de perfil.
    
- Copiar carpetas o mensajes. Para obtener más información, vea [Copiar o mover un mensaje o una carpeta](copying-or-moving-a-message-or-a-folder.md).
    
- Obtener acceso a los objetos que pertenecen a otros proveedores. Para obtener más información, vea [compatibilidad con el acceso a objetos y comparación](supporting-object-access-and-comparison.md). 
    
- Controlar la notificación de evento. Para obtener más información, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).
    
- Asignar y liberar memoria.
    
- Obtención de un identificador único.
    
- La invalidación de objetos.
    
- Tratamiento de errores.
    
- Registrar preprocessors de mensaje. 
    
- Preparación de los informes de entrega de mensajes. 
    
En tiempo de inicio de sesión, MAPI llama al método de inicio de sesión del objeto de proveedor de cada proveedor de servicios. Para los proveedores de la libreta de direcciones, MAPI llama a [IABProvider::Logon](iabprovider-logon.md). Para los proveedores de almacén de mensajes, MAPI llama a [IMSProvider::Logon](imsprovider-logon.md). Para los proveedores de transporte, MAPI llama a [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI pasa un puntero al objeto de soporte adecuado en uno de los parámetros a este método. El método de inicio de sesión a su vez crea una instancia de un objeto de inicio de sesión, pasando el puntero del objeto de soporte técnico. El objeto de inicio de sesión llama al método **IUnknown:: AddRef** del objeto de soporte técnico para conservar, si es necesario. Para obtener más información acerca del proceso de inicio de sesión para proveedores de servicios, vea [iniciar un proveedor de servicios](starting-a-service-provider.md).
  
Cuando un cliente cierra la sesión, llamadas a método de cierre de sesión del objeto de inicio de sesión MAPI. El método de cierre de sesión llama a **IUnknown:: Release** (método) del objeto de soporte técnico para indicar que el proveedor ya no tiene intención de llamar a cualquiera de los métodos de soporte técnico. Al igual que con inicio de sesión, los métodos de cierre de sesión tienen nombres ligeramente diferentes. Las interfaces [IABLogon](iablogoniunknown.md) y [IMSLogon](imslogoniunknown.md) tienen métodos de **cierre de sesión** ; la interfaz [IXPLogon](ixplogoniunknown.md) tiene un método [TransportLogoff](ixplogon-transportlogoff.md) . 
  
Funciones de punto de entrada de servicio de mensajes se llama cuando se produce un error en un intento de inicio de sesión con el error MAPI_E_UNCONFIGURED o cuando un cliente inicia una solicitud de configuración. MAPI crea una instancia de un objeto de configuración de soporte técnico y llama a la función de punto de entrada de servicio de mensaje para el proveedor no configurado o el proveedor de cuya configuración va a cambiar. A diferencia de los objetos de soporte técnico, objetos de configuración de soporte técnico son válidos sólo hasta que el punto de entrada función devuelve; Servicios de mensajes no llamar a métodos de estos objetos **AddRef** para mantenerlas. 
  
Normalmente, MAPI realiza llamadas a la función de punto de entrada de servicio de un proveedor mensaje, pero a veces se solicita un proveedor para realizar la llamada. Esto puede ocurrir cuando un cliente llama el método [SettingsDialog](imapistatus-settingsdialog.md) de un proveedor para solicitar el proveedor para mostrar su hoja de propiedades de configuración. **Diálogo Configuración** debe llamar a [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obtener un objeto de soporte técnico de configuración que pueden pasar a la función de punto de entrada de servicio de mensaje. 
  
El método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponible para determinar las direcciones de las funciones de asignación y cancelación de asignación de memoria sin tener que volver a vincular con MAPI. Uso **GetMemAllocRoutines** también hace que sea más fácil para el seguimiento de pérdidas de memoria rodeando las llamadas de función de asignación con código de depuración. Si se llama **GetMemAllocRoutines**, tal y como se recomienda, debe hacerlo antes de llamar a la función [CreateIProp](createiprop.md) , que requiere que las direcciones de la función de asignación como parámetros. 
  
Cuando se necesita para crear una nueva libreta de direcciones o un mensaje almacena el objeto, crear y establecer una clave de búsqueda para el objeto en su propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Llame a [IMAPISupport::NewUID](imapisupport-newuid.md) para obtener un identificador único para usar en la creación de una clave de búsqueda. No use su propio codificado de forma rígida [MAPIUID](mapiuid.md). Un proveedor **MAPIUID** se debe usar solo para los identificadores de entrada. Para obtener más información acerca de la creación de las claves de búsqueda, vea el [registro de MAPI y las claves de búsqueda](mapi-record-and-search-keys.md).
  
A veces, una aplicación cliente puede liberar un objeto sin liberar uno o varios de sus objetos afiliados. En tal caso, un proveedor puede requerir representar un objeto no publicado no se puede utilizar. Para ello, el proveedor libera todos los recursos relacionados con el objeto y, a continuación, llama a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) para invalidar vtable del objeto. **MakeInvalid** reemplaza los métodos de **IUnknown** del vtable (**QueryInterface**, **AddRef**y **Release**) con implementaciones estándar de MAPI y hace que todos los otros métodos devolver MAPI_E_INVALID_OBJECT. **MakeInvalid** también libera memoria de todos los objetos que no sea la tabla vtable. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

