---
title: Implementar el inicio y cierre de sesión de proveedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817683"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementar el inicio y cierre de sesión de proveedor de libreta de direcciones

**Hace referencia a**: Outlook 
  
Los proveedores de la libreta de direcciones compatible con inicio de sesión y cierre de sesión mediante la implementación de los métodos de la [IABProvider: IUnknown](iabprovideriunknown.md) interfaz. El ** IABProvider ** interfaz hereda directamente de **IUnknown** y agrega otros sólo dos métodos: **Inicio de sesión** y **apagado**. 
  
## <a name="logoff"></a>Cierre de sesión

MAPI llamará al método de [IABProvider::Logon](iabprovider-logon.md) de su proveedor al principio de cada sesión y siempre que el proveedor se agrega al perfil actual y el cliente permite la reconfiguración dinámica. Cuando el método **IABProvider::Logon** llama a MAPI, su proveedor de libreta de direcciones comienza su proceso de inicio de sesión. 
  
**Para implementar IABProvider::Log**
  
1. Inicializar todos los punteros de parámetro de salida que se pasó por MAPI. 
    
2. Llamar al método **IUnknown:: AddRef** del objeto de soporte técnico para incrementar su recuento de referencia. 
    
3. Llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte técnico para abrir la sección del perfil que contiene información de configuración acerca de su proveedor. Pase NULL para el parámetro _lpUID_ y el indicador MAPI_MODIFY si va a realizar cambios. 
    
4. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la sección de perfil para recuperar las propiedades que necesita su proveedor de inicio de sesión, como el nombre de la tabla de base de datos o archivo de datos. 
    
5. Compruebe que las propiedades están todas disponibles y válido. Si es necesario y permitidos, se muestra un cuadro de diálogo para pedir al usuario que realice las correcciones o adiciones a la información no es válido o falta y llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para guardar los cambios. Algunas de las propiedades comunes que deberían estar disponibles son: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > No establezca **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) o **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). En tiempo de inicio de sesión, estas propiedades son de sólo lectura. 
  
6. Si una o más propiedades de configuración no están disponibles, se producirá un error y devolver el valor MAPI_E_UNCONFIGURED.
    
7. Llame a [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar un [MAPIUID](mapiuid.md). El proveedor puede crear una **MAPIUID** por: 
    
   - Llamar al método [IMAPISupport::NewUID](imapisupport-newuid.md) . 
    
   - Llamar a la UUIDGEN. Herramienta de EXE para definir un GUID que el proveedor se usa para incluir en uno de sus archivos de encabezado.
    
8. Si lo desea, guarde un recién creado **MAPIUID** en el perfil actual mediante una llamada a la sección de perfil ** IMAPIProp::SetProps ** (método). 
    
9. Versión de la sección de perfil llamando a su método **IUnknown:: Release** . 
    
10. Crear una instancia de un nuevo objeto de inicio de sesión y establecer el contenido del parámetro _lppABLogon_ a la dirección de este nuevo objeto. 
    
Debido a que es posible de MAPI para llamar a su ** inicio de sesión ** método varias veces durante una sesión, es conveniente admitir esta posibilidad en su implementación por la posibilidad de crear varios objetos de inicio de sesión y realizar un seguimiento de cada objeto que se crea. Admitir varias llamadas de **Inicio de sesión** , permite a un usuario de una aplicación cliente, por ejemplo, para iniciar sesión en una sesión con identidades diferentes o destinos de entrega diferentes de uso. 
  
Se llama al método **Shutdown** cuando finaliza la sesión. MAPI llama a su método [IABProvider::Shutdown](iabprovider-shutdown.md) como una de las tareas última necesarios para cerrar una sesión. MAPI ha publicado todos los objetos de su proveedor inicio de sesión y, cuando el proveedor recibe esta llamada, puede suponer que se trata de la última llamada que va a recibir. En la implementación de **IABProvider::Shutdown**, realizar la limpieza final que se siente es necesario. Por ejemplo, el proveedor puede llamar a **MAPIDeinitIdle** si se denomina **MAPIInitIdle** para usar el motor de inactividad durante la sesión o el método **IUnknown:: Release** de todos los objetos que todavía tiene que liberar. 
  
Si su proveedor no tiene ninguna limpieza final, su implementación puede constar de una sola línea de código: 
  
```cpp
return S_OK;

```


