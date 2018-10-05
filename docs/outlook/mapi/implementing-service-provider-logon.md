---
title: Implementar el inicio de sesión del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401646"
---
# <a name="implementing-service-provider-logon"></a>Implementar el inicio de sesión del proveedor de servicios

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
MAPI llama a un método en el objeto de proveedor para comenzar el proceso de inicio de sesión mediante el puntero que devuelve desde la función de punto de entrada. El método manera, varía según el tipo de proveedor de servicios:
  
- [IABProvider::Logon](iabprovider-logon.md) para los proveedores de la libreta de direcciones 
    
- [IMSProvider::Logon](imsprovider-logon.md) para los proveedores de almacén de mensajes 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para los proveedores de transporte 
    
Realizar las siguientes tareas en el método de inicio de sesión que implementa:
  
1. Incrementar el recuento de referencia en el objeto de soporte técnico que se pasa como un parámetro de entrada mediante una llamada a su método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte para obtener acceso a la sección de perfil. 
    
3. Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para establecer las propiedades siguientes: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > No intente establecer las propiedades de la sección de perfil **PR_RESOURCE_FLAGS** o **PR_PROVIDER_DLL_NAME** . En tiempo de inicio de sesión, estas propiedades son de sólo lectura. 
  
4. Compruebe que las propiedades que necesita para la configuración se almacenan en el perfil o están disponibles desde el usuario. Para obtener más información acerca de cómo comprobar la configuración, vea [Comprobar la configuración del proveedor de servicio](verifying-service-provider-configuration.md).
    
5. Llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) del objeto de soporte técnico para registrar un identificador único o [MAPIUID](mapiuid.md), si su proveedor es un proveedor de almacén de mensaje o de la libreta de direcciones. Los proveedores de transporte registrar **MAPIUID** estructuras cuando MAPI llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Para obtener más información acerca de cómo registrar un **MAPIUID**, vea [Identificadores únicos proveedor de servicio de registro](registering-service-provider-unique-identifiers.md).
    
6. Crear una instancia de un objeto de inicio de sesión y devolver con uno de los siguientes valores:
    
  - S_OK para indicar un inicio de sesión correcto.
    
  - MAPI_E_UNCONFIGURED para indicar que uno o más de las propiedades de configuración no estaban disponibles.
    
  - MAPI_E_USER_CANCEL para indicar que el usuario canceló el cuadro de diálogo Configuración, lo que provoca que las propiedades de configuración que no esté disponible.
    
  - MAPI_E_FAILONEPROVIDER para indicar que no se pudo configurar su proveedor, pero que debe permitir la MAPI para usarse independientemente de la forma. Métodos de inicio de sesión deben devolver este valor para notificar un error no grave, como cuando el proveedor requiere una contraseña y no puede solicitar al usuario para él debido a que la interfaz de usuario está deshabilitada. 
    
La lista anterior de tareas describe una implementación mínima para un método de inicio de sesión del proveedor de servicio. Puede incluir funciones adicionales, si es necesario. Por ejemplo, algunos proveedores de llamar a [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para actualizar la tabla de estado en el método de inicio de sesión. 
  
> [!NOTE]
> Para conseguir el mejor rendimiento en tiempo de inicio de sesión, evite llamar a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) o [SpoolerNotify](imapisupport-spoolernotify.md). Antes de estas llamadas pueden completar y devolver el control al método de inicio de sesión, se debe iniciar la cola MAPI. 
  
## <a name="see-also"></a>Vea también

- [Iniciar un proveedor de servicios](starting-a-service-provider.md)

