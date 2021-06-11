---
title: Implementación del inicio de sesión y cierre de sesión del proveedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438739"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementación del inicio de sesión y cierre de sesión del proveedor de libreta de direcciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libreta de direcciones admiten el inicio de sesión y el cierre de sesión mediante la implementación de los métodos de la [interfaz IABProvider : IUnknown.](iabprovideriunknown.md) La interfaz ** IABProvider ** hereda directamente de **IUnknown** y agrega solo otros dos métodos: **Logon** y **Shutdown**. 
  
## <a name="logoff"></a>Cierre de sesión

MAPI llamará al método [IABProvider::Logon](iabprovider-logon.md) del proveedor al principio de cada sesión y siempre que el proveedor se agrega al perfil actual y el cliente admite la reconfiguración dinámica. Cuando MAPI llama al **método IABProvider::Logon,** el proveedor de la libreta de direcciones inicia el proceso de inicio de sesión. 
  
**Para implementar IABProvider::Log**
  
1. Inicializa todos los punteros de parámetro de salida pasados por MAPI. 
    
2. Llame al método **IUnknown::AddRef** del objeto de soporte técnico para incrementar su recuento de referencias. 
    
3. Llame al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte técnico para abrir la sección del perfil que contiene información de configuración sobre el proveedor. Pase NULL para el  _parámetro lpUID_ y la marca MAPI_MODIFY si desea realizar cambios. 
    
4. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la sección de perfil para recuperar las propiedades que el proveedor necesita para el inicio de sesión, como el nombre del archivo de datos o la tabla de base de datos. 
    
5. Compruebe que todas las propiedades están disponibles y son válidas. Si es necesario y está permitido, muestre un cuadro de diálogo para solicitar al usuario que realice correcciones o adiciones a información no válida o que falte y llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para guardar los cambios. Algunas de las propiedades comunes que deben estar disponibles incluyen: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > No establezca **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) **o PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). En el momento del inicio de sesión, estas propiedades son de solo lectura. 
  
6. Si una o varias propiedades de configuración no están disponibles, se producirá un error y se devolverá el MAPI_E_UNCONFIGURED.
    
7. Llame [a IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar [un MAPIUID](mapiuid.md). El proveedor puede crear un **MAPIUID** mediante: 
    
   - Llamar al [método IMAPISupport::NewUID.](imapisupport-newuid.md) 
    
   - Llamar a la UUIDGEN.EXE para definir un GUID que el proveedor usa para incluir en uno de sus archivos de encabezado.
    
8. Si lo desea, guarde un **MAPIUID** recién creado en el perfil actual llamando al método ** IMAPIProp::SetProps ** de la sección de perfil. 
    
9. Libere la sección de perfil llamando a su **método IUnknown::Release.** 
    
10. Cree una instancia de un nuevo objeto de inicio de sesión y establezca el contenido del parámetro  _lppABLogon_ en la dirección de este nuevo objeto. 
    
Dado que es posible que MAPI llame al método ** Logon ** varias veces durante una sesión, es aconsejable admitir esta posibilidad en la implementación al poder crear varios objetos de inicio de sesión y realizar un seguimiento de cada objeto que se crea. Admitir varias llamadas **de inicio** de sesión permite al usuario de una aplicación cliente, por ejemplo, iniciar sesión en una sesión con identidades diferentes o usar destinos de entrega diferentes. 
  
**Se** llama al apagado cuando finaliza la sesión. MAPI llama al [método IABProvider::Shutdown](iabprovider-shutdown.md) como una de las últimas tareas relacionadas con el cierre de una sesión. MAPI ha liberado todos los objetos de inicio de sesión del proveedor y, cuando el proveedor recibe esta llamada, puede suponer que esta es la última llamada que recibirá. En la implementación de **IABProvider::Shutdown**, realice cualquier limpieza final que crea necesaria. Por ejemplo, el proveedor puede llamar a **MAPIDeinitIdle** si ha llamado a **MAPIInitIdle** para usar el motor inactivo durante la sesión o el método **IUnknown::Release** de los objetos que aún no se han liberado. 
  
Si el proveedor no tiene ninguna limpieza final, su implementación puede estar hecha de una sola línea de código: 
  
```cpp
return S_OK;

```


