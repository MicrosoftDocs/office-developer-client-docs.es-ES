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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310090"
---
# <a name="implementing-service-provider-logon"></a>Implementar el inicio de sesión del proveedor de servicios

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI llama a un método en el objeto de proveedor para comenzar el proceso de inicio de sesión mediante el puntero que se devuelve de la función de punto de entrada. El método varía como se indica a continuación, según el tipo de proveedor de servicios:
  
- [IABProvider:: Inicio de sesión](iabprovider-logon.md) para los proveedores de libreta de direcciones 
    
- [IMSProvider:: Inicio de sesión](imsprovider-logon.md) para proveedores de almacenamiento de mensajes 
    
- [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para proveedores de transporte 
    
Realice las siguientes tareas en cualquier método de inicio de sesión que implemente:
  
1. Para incrementar el recuento de referencia en el objeto de soporte que se pasa como parámetro de entrada, llame a su método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Llame al método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) del objeto support para obtener acceso a su sección de perfil. 
    
3. Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la sección de perfil para establecer las siguientes propiedades: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > No intente establecer las propiedades **PR_RESOURCE_FLAGS** o **PR_PROVIDER_DLL_NAME** de la sección de perfil. En el momento del inicio de sesión, estas propiedades son de solo lectura. 
  
4. Compruebe que las propiedades que necesita para la configuración se almacenan en el perfil o están disponibles para el usuario. Para obtener más información acerca de la comprobación de la configuración, vea [verifyIng Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Llame al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) del objeto support para registrar un identificador único, o [MAPIUID](mapiuid.md), si el proveedor es una libreta de direcciones o un proveedor de almacenamiento de mensajes. Los proveedores de transporte registran estructuras **MAPIUID** cuando MAPI llama a su método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . Para obtener más información acerca de cómo registrar una **MAPIUID**, consulte [registraNdo identificadores únicos del proveedor de servicios](registering-service-provider-unique-identifiers.md).
    
6. Cree una instancia de un objeto de inicio de sesión y vuelva con uno de los siguientes valores:
    
  - S_OK para indicar que el inicio de sesión se ha realizado correctamente.
    
  - MAPI_E_UNCONFIGURED para indicar que una o varias de las propiedades de configuración no estaban disponibles.
    
  - MAPI_E_USER_CANCEL para indicar que el usuario canceló el cuadro de diálogo de configuración, lo que hace que las propiedades de configuración no estén disponibles.
    
  - MAPI_E_FAILONEPROVIDER para indicar que no se ha podido configurar el proveedor, pero MAPI debe permitir su uso independientemente. Los métodos de inicio de sesión deben devolver este valor para informar de un error no grave, como cuando el proveedor requiere una contraseña y no puede solicitarlo al usuario porque la interfaz de usuario está deshabilitada. 
    
La lista anterior de tareas describe una implementación mínima de un método de inicio de sesión de un proveedor de servicios. Puede incluir una funcionalidad adicional, si es necesario. Por ejemplo, algunos proveedores llaman a [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para actualizar la tabla de estado en su método de inicio de sesión. 
  
> [!NOTE]
> Para obtener el mejor rendimiento en el momento del inicio de sesión, evite llamar a [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) o [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md). Para que estas llamadas puedan completarse y devuelvan el control al método de inicio de sesión, es necesario iniciar la cola MAPI. 
  
## <a name="see-also"></a>Vea también

- [Inicio de un proveedor de servicios](starting-a-service-provider.md)

