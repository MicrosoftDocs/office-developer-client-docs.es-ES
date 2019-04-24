---
title: Información general sobre el objeto support
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327170"
---
# <a name="support-object-overview"></a>Información general sobre el objeto support

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI suministra un objeto de soporte, un objeto que implementa la interfaz [IMAPISupport: IUnknown](imapisupportiunknown.md) , para todos los proveedores de servicios durante el inicio de sesión y para todos los servicios de mensajes durante la configuración. 
  
Los clientes no pueden tener acceso a los objetos de soporte; se implementan mediante MAPI y solo los proveedores de servicios los llaman. La interfaz **IMAPISupport** se especifica en el archivo de encabezado Mapispi. h. Su identificador es IID_IMAPISup y su tipo de puntero es LPMAPISUP. Los objetos de compatibilidad no exponen ninguna propiedad MAPI. 
  
Un proveedor puede tener uno o varios objetos de soporte, en función del número de veces que MAPI registra el proveedor o el número de veces que se llama a la función de entrada del servicio de mensajes del proveedor. Normalmente, un proveedor iniciará sesión al menos una vez por sesión. La libreta de direcciones y los proveedores de transporte se registran cada vez que un cliente inicia una sesión con una entrada de perfil que las solicita. Los proveedores de almacenamiento de mensajes se registran cada vez que un cliente llama al método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . 
  
En el caso de varios inicios de sesión en una sesión, puede elegir entre retener y usar cada objeto de compatibilidad por separado, o conservar y usar solamente el primero, descartando cada objeto de soporte posterior. Para conservar un objeto de soporte, llame a su método **IUnknown:: AddRef** . Llamar a **AddRef** en un objeto de soporte que desea conservar durante una sesión es sumamente importante; Si no se realiza la llamada, MAPI libera el objeto de soporte y libera su memoria. 
  
El objetivo del objeto de soporte es proporcionar implementaciones para un número relativamente grande de métodos usados normalmente por los proveedores. Cada objeto support también contiene datos contextuales específicos de su propia instancia, como la sesión en la que se está ejecutando el proveedor, la sección Profile que usa el proveedor y la información de error de la sesión. 
  
Hay cuatro tipos diferentes de objetos de soporte: uno para cada tipo de proveedor principal (libreta de direcciones, almacén de mensajes y transporte) y otro para la configuración compatible. 
  
MAPI Personaliza cada objeto de soporte mediante la inclusión de implementaciones de métodos relevantes para su uso. Las implementaciones de algunos métodos, como [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), se incluyen en todos los objetos de compatibilidad. Las implementaciones de otros métodos, como [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md), solo se aplican a objetos de compatibilidad determinados. Solo los proveedores de almacenamiento y transporte de mensajes pueden usar este método; Cuando un proveedor de libretas de direcciones o un servicio de mensajes intentan llamarlo, MAPI devuelve MAPI_E_NO_SUPPORT.
  
Los objetos de soporte pueden usarse para realizar muchas tareas, como las siguientes:
  
- Acceso a una sección de perfil.
    
- Copiar carpetas o mensajes. Para obtener más información, vea [copiar o mover un mensaje o una carpeta](copying-or-moving-a-message-or-a-folder.md).
    
- Obtener acceso a objetos que pertenecen a otros proveedores. Para obtener más información, consulte compatibilidad con el [acceso a objetos y la comparación](supporting-object-access-and-comparison.md). 
    
- Controlar la notificación de eventos. Para obtener más información, consulte [admitir la notificación de eventos](supporting-event-notification.md).
    
- Asignar y liberar memoria.
    
- Obtener un identificador único.
    
- Invalidando objetos.
    
- Control de errores.
    
- Registro de preprocesadores de mensajes. 
    
- Preparar los informes de entrega de mensajes. 
    
Durante el inicio de sesión, MAPI llama al método Logon del objeto de proveedor de cada proveedor de servicios. Para los proveedores de la libreta de direcciones, las llamadas MAPI [IABProvider:: Logon](iabprovider-logon.md). Para los proveedores de almacenamiento de mensajes, las llamadas MAPI [IMSProvider:: Logon](imsprovider-logon.md). Para los proveedores de transporte, las llamadas MAPI [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). MAPI pasa un puntero al objeto de soporte adecuado en uno de los parámetros de este método. A su vez, el método Logon crea una instancia de un objeto de inicio de sesión, pasándole el puntero de objeto de compatibilidad. El objeto de inicio de sesión llama al método **IUnknown:: AddRef** del objeto support para mantenerlo, si es necesario. Para obtener más información acerca del proceso de inicio de sesión para los proveedores de servicios, consulte [iniciar un proveedor de servicios](starting-a-service-provider.md).
  
Cuando un cliente cierra la sesión, MAPI llama al método Logoff del objeto de inicio de sesión. El método Logoff llama al método **IUnknown:: Release** del objeto support para indicar que el proveedor ya no va a llamar a ninguno de los métodos de soporte técnico. Al igual que con el inicio de sesión, los métodos de cierre de sesión tienen nombres ligeramente diferentes. Las interfaces [IABLogon](iablogoniunknown.md) y [IMSLogon](imslogoniunknown.md) tienen métodos de **cierre de sesión** ; la interfaz [IXPLogon](ixplogoniunknown.md) tiene un método [TransportLogoff](ixplogon-transportlogoff.md) . 
  
Se llama a las funciones de punto de entrada del servicio de mensajes cuando se produce un error de intento de inicio de sesión con el error MAPI_E_UNCONFIGURED o cuando un cliente inicia una solicitud de configuración. MAPI crea una instancia de un objeto de soporte de configuración y llama a la función de punto de entrada del servicio de mensaje para el proveedor no configurado o el proveedor cuya configuración va a cambiar. A diferencia de los otros objetos de compatibilidad, los objetos de compatibilidad de configuración son válidos hasta que se devuelve la función de punto de entrada; los servicios de mensajes no llaman a estos objetos a los métodos **AddRef** para conservarlos. 
  
Normalmente, MAPI realiza llamadas a la función de punto de entrada del servicio de mensajes de un proveedor, pero a veces se pide a un proveedor que realice la llamada. Esto puede ocurrir cuando un cliente llama al método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) de un proveedor para solicitar al proveedor que muestre su hoja de propiedades de configuración. **SettingsDialog** debe llamar a [IMAPISupport:: GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obtener un objeto de compatibilidad de configuración que pueda pasar a la función de punto de entrada del servicio de mensajes. 
  
El método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponible para determinar las direcciones de las funciones de asignación de memoria y desasignación sin tener que vincular con MAPI. El uso de **GetMemAllocRoutines** también hace que sea más fácil realizar el seguimiento de pérdidas de memoria al rodear las llamadas de función de asignación con código de depuración. Si llama a **GetMemAllocRoutines**, tal y como se recomienda, hágalo antes de llamar a la función [CreateIProp](createiprop.md) , que requiere que la función de asignación se redirige como parámetros. 
  
Cuando necesite crear una nueva libreta de direcciones o un objeto de almacén de mensajes, cree y establezca una clave de búsqueda para el objeto en su propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Llamar a [IMAPISupport:: NewUID](imapisupport-newuid.md) para obtener un identificador único para usarlo en la creación de una clave de búsqueda. No use sus propios [MAPIUID](mapiuid.md)codificados de forma rígida. El **MAPIUID** de un proveedor debe usarse solo para los identificadores de entrada. Para obtener más información acerca de la creación de claves de búsqueda, consulte [MAPI record and search Keys](mapi-record-and-search-keys.md).
  
Una aplicación cliente puede, a veces, liberar un objeto sin liberar uno o más de sus objetos asociados. En este caso, es posible que un proveedor necesite representarlo a un objeto que no está en versión inutilizable. Para ello, el proveedor libera todos los recursos conectados con el objeto y, a continuación, llama a [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) para invalidar la vtable del objeto. **MakeInvalid** reemplaza los métodos **IUnknown** de vtable (**QueryInterface**, **ADDREF**y **Release**) con implementaciones MAPI estándar y, de este modo, todos los demás métodos devuelven MAPI_E_INVALID_OBJECT. **MakeInvalid** también libera toda la memoria del objeto que no sea vtable. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

