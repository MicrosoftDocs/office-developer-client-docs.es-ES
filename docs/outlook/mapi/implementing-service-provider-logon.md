---
title: Implementación del inicio de sesión del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310090"
---
# <a name="implementing-service-provider-logon"></a>Implementación del inicio de sesión del proveedor de servicios

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI llama a un método en el objeto de proveedor para iniciar el proceso de inicio de sesión mediante el puntero que se devuelve de la función de punto de entrada. El método varía de la siguiente manera, según el tipo de proveedor de servicios:
  
- [IABProvider::Logon](iabprovider-logon.md) para proveedores de libreta de direcciones 
    
- [IMSProvider::Logon](imsprovider-logon.md) para proveedores de almacén de mensajes 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para proveedores de transporte 
    
Realice las siguientes tareas en cualquier método de inicio de sesión que implemente:
  
1. Incremente el número de referencias en el objeto de soporte técnico que se pasa como parámetro de entrada llamando a su [método IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) 
    
2. Llame al método [IMAPISupport::OpenProfileSection del](imapisupport-openprofilesection.md) objeto de soporte técnico para obtener acceso a la sección de perfil. 
    
3. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para establecer las siguientes propiedades: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > No intente establecer las propiedades de PR_RESOURCE_FLAGS **o** **PR_PROVIDER_DLL_NAME** perfil. En el momento del inicio de sesión, estas propiedades son de solo lectura. 
  
4. Compruebe que las propiedades que necesita para la configuración se almacenan en el perfil o están disponibles para el usuario. Para obtener más información acerca de cómo comprobar la configuración, vea [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) del objeto de soporte técnico para registrar un identificador único, o [MAPIUID](mapiuid.md), si su proveedor es un proveedor de libreta de direcciones o almacén de mensajes. Los proveedores de transporte registran **estructuras MAPIUID** cuando MAPI llama a su [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Para obtener más información acerca del registro **de un MAPIUID,** vea [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
    
6. Cree una instancia de un objeto de inicio de sesión y vuelva con uno de los siguientes valores:
    
  - S_OK para indicar un inicio de sesión correcto.
    
  - MAPI_E_UNCONFIGURED para indicar que una o varias de las propiedades de configuración no estaban disponibles.
    
  - MAPI_E_USER_CANCEL para indicar que el usuario canceló el cuadro de diálogo de configuración, lo que hace que las propiedades de configuración no estén disponibles.
    
  - MAPI_E_FAILONEPROVIDER para indicar que el proveedor no se pudo configurar, pero que MAPI debería permitir su uso independientemente. Los métodos de inicio de sesión deben devolver este valor para notificar un error no grave, como cuando el proveedor requiere una contraseña y no se puede solicitar al usuario porque la interfaz de usuario está deshabilitada. 
    
La lista anterior de tareas describe una implementación mínima para un método de inicio de sesión del proveedor de servicios. Puede incluir funciones adicionales, si es necesario. Por ejemplo, algunos proveedores llaman [a IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para actualizar la tabla de estado en su método de inicio de sesión. 
  
> [!NOTE]
> Para lograr el mejor rendimiento en el momento del inicio de sesión, evite llamar a [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) o [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Para que estas llamadas puedan completarse y devolver el control al método de inicio de sesión, se debe iniciar la cola MAPI. 
  
## <a name="see-also"></a>Vea también

- [Inicio de un proveedor de servicios](starting-a-service-provider.md)

