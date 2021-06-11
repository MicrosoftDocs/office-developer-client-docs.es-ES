---
title: Introducción a los objetos de soporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433615"
---
# <a name="support-object-overview"></a>Introducción a los objetos de soporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona un objeto de soporte técnico, un objeto que implementa la interfaz [IMAPISupport : IUnknown,](imapisupportiunknown.md) para todos los proveedores de servicios durante el inicio de sesión y para todos los servicios de mensajes durante la configuración. 
  
Los clientes no pueden acceder a los objetos de soporte técnico; se implementan mediante MAPI y solo los llaman los proveedores de servicios. La **interfaz IMAPISupport** se especifica en el archivo de encabezado Mapispi.h. Su identificador es IID_IMAPISup y su tipo de puntero es LPMAPISUP. Los objetos de soporte no exponen ninguna propiedad MAPI. 
  
A un proveedor se le puede dar uno o varios objetos de soporte técnico, según el número de veces que MAPI registra el proveedor o el número de veces que se llama a la función de entrada de servicio de mensajes del proveedor. Normalmente, un proveedor inicia sesión al menos una vez por sesión. Los proveedores de transporte y libreta de direcciones inician sesión cada vez que un cliente inicia una sesión con una entrada de perfil que los solicita. Los proveedores de almacén de mensajes inician sesión cada vez que un cliente llama al método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
En el caso de varios inicios de sesión en una sesión, puede elegir conservar y usar cada objeto de soporte por separado o conservar y usar solo el primero, descartando cada objeto de soporte técnico posterior. Para conservar un objeto de soporte técnico, llame a su **método IUnknown::AddRef.** Llamar **a AddRef** en un objeto de soporte técnico que desea conservar a lo largo de una sesión es extremadamente importante; si no se realiza la llamada, MAPI libera el objeto de soporte técnico y libera su memoria. 
  
El objetivo del objeto de soporte técnico es proporcionar implementaciones para un número bastante grande de métodos usados habitualmente por los proveedores. Cada objeto de soporte también contiene datos contextuales específicos de su propia instancia, como la sesión en la que se está ejecutando el proveedor, la sección de perfil que usa el proveedor y la información de error de la sesión. 
  
Hay cuatro tipos diferentes de objetos de soporte: uno para cada tipo de proveedor principal (libreta de direcciones, almacén de mensajes y transporte) y otro para la compatibilidad con la configuración. 
  
MAPI personaliza cada objeto de soporte técnico al incluir implementaciones de métodos que son relevantes para su uso. Las implementaciones de algunos métodos, [como IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), se incluyen en todos los objetos de compatibilidad. Las implementaciones de otros métodos, [como IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), solo se aplican a objetos de soporte técnico concretos. Solo los proveedores de transporte y almacén de mensajes pueden usar este método; cuando un proveedor de libreta de direcciones o un servicio de mensajes intentan llamarlo, MAPI devuelve MAPI_E_NO_SUPPORT.
  
Los objetos de soporte se pueden usar para realizar muchas tareas, como las siguientes:
  
- Acceso a una sección de perfil.
    
- Copiar carpetas o mensajes. Para obtener más información, [vea Copiar o mover un mensaje o una carpeta](copying-or-moving-a-message-or-a-folder.md).
    
- Acceso a objetos que pertenecen a otros proveedores. Para obtener más información, vea [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md). 
    
- Controlar la notificación de eventos. Para obtener más información, vea [Supporting Event Notification](supporting-event-notification.md).
    
- Asignar y liberar memoria.
    
- Obtener un identificador único.
    
- Invalidar objetos.
    
- Controlar errores.
    
- Registro de preprocesadores de mensajes. 
    
- Preparar informes de entrega de mensajes. 
    
En el momento del inicio de sesión, MAPI llama al método de inicio de sesión del objeto de proveedor de cada proveedor de servicios. Para los proveedores de libreta de direcciones, MAPI llama [a IABProvider::Logon](iabprovider-logon.md). Para los proveedores de almacén de mensajes, MAPI llama a [IMSProvider::Logon](imsprovider-logon.md). Para los proveedores de transporte, MAPI llama [a IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI pasa un puntero al objeto de soporte adecuado en uno de los parámetros a este método. A su vez, el método de inicio de sesión crea una instancia de un objeto de inicio de sesión y le pasa el puntero del objeto de soporte. El objeto de inicio de sesión llama al método **IUnknown::AddRef** del objeto de soporte técnico para retenerlo, si es necesario. Para obtener más información acerca del proceso de inicio de sesión de los proveedores de [servicios,](starting-a-service-provider.md)vea Starting a Service Provider .
  
Cuando un cliente cierra la sesión, MAPI llama al método de cierre de sesión del objeto de inicio de sesión. El método de cierre de sesión llama al método **IUnknown::Release** del objeto de soporte técnico para indicar que el proveedor ya no tiene intención de llamar a ninguno de los métodos de soporte técnico. Al igual que con el inicio de sesión, los métodos de cierre de sesión tienen nombres ligeramente diferentes. Las [interfaces IABLogon](iablogoniunknown.md) [e IMSLogon](imslogoniunknown.md) tienen **métodos Logoff;** la [interfaz IXPLogon](ixplogoniunknown.md) tiene un [método TransportLogoff.](ixplogon-transportlogoff.md) 
  
Se llama a las funciones de punto de entrada del servicio de mensajes cuando se produce un error al intentar iniciar sesión con el error MAPI_E_UNCONFIGURED o cuando un cliente inicia una solicitud de configuración. MAPI crea una instancia de un objeto de compatibilidad con la configuración y llama a la función de punto de entrada del servicio de mensajes para el proveedor no configurado o el proveedor cuya configuración está a punto de cambiar. A diferencia de los demás objetos de soporte técnico, los objetos de soporte técnico de configuración solo son válidos hasta que la función de punto de entrada devuelve; los servicios de mensajes no llaman a los **métodos AddRef de estos** objetos para conservarlos. 
  
Normalmente, MAPI realiza llamadas a la función de punto de entrada de servicio de mensajes de un proveedor, pero a veces se pide a un proveedor que realice la llamada. Esto puede ocurrir cuando un cliente llama al método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de un proveedor para solicitar al proveedor que muestre su hoja de propiedades de configuración. **SettingsDialog** debe llamar a [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obtener un objeto de soporte de configuración que pueda pasar a la función de punto de entrada del servicio de mensajes. 
  
El [método IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponible para determinar las direcciones de las funciones de asignación y asignación de memoria sin tener que vincular con MAPI. El **uso de GetMemAllocRoutines** también facilita el seguimiento de pérdidas de memoria al rodear las llamadas de función de asignación con código de depuración. Si llama a **GetMemAllocRoutines**, como se recomienda, haga esto antes de llamar a la [función CreateIProp,](createiprop.md) que requiere las direcciones de función de asignación como parámetros. 
  
Cuando necesite crear un nuevo objeto de libreta de direcciones o almacén de mensajes, cree y establezca una clave de búsqueda para el objeto en su propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Llama [a IMAPISupport::NewUID](imapisupport-newuid.md) para obtener un identificador único que se usará en la creación de una clave de búsqueda. No use su propio [MAPIUID](mapiuid.md)codificado de forma hard. **MAPIUID** de un proveedor debe usarse solo para identificadores de entrada. Para obtener más información acerca de la construcción de claves de búsqueda, vea [Mapi Record and Search Keys](mapi-record-and-search-keys.md).
  
A veces, una aplicación cliente puede liberar un objeto sin liberar uno o varios de sus objetos asociados. En tal caso, es posible que un proveedor tenga que hacer que un objeto inédito no se pueda usar. Para ello, el proveedor libera todos los recursos conectados al objeto y, a continuación, llama a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) para invalidar la tabla virtual del objeto. **MakeInvalid reemplaza** los métodos **IUnknown** de la vtable (**QueryInterface**, **AddRef** y **Release**) por implementaciones estándar de MAPI y hace que todos los demás métodos devuelvan MAPI_E_INVALID_OBJECT. **MakeInvalid** también libera toda la memoria del objeto que no sea la tabla virtual. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

