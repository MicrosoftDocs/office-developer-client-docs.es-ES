---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817114"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Hace referencia a**: Outlook 
  
Establece una conexión a una sesión activa.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>Parámetros

 _lpMAPISup_
  
> [entrada] Un puntero al objeto de soporte técnico del proveedor de libreta de direcciones.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana primaria para el cuadro de diálogo de inicio de sesión que muestra el método de **Inicio de sesión** , si se permite. El parámetro _ulUIParam_ contiene el valor del parámetro el mismo nombre que se pasan a MAPI en la llamada a la función [MAPILogonEx](mapilogonex.md) anterior. 
    
 _lpszProfileName_
  
> [entrada] Un puntero al nombre del perfil de la sesión.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
AB_NO_DIALOG 
  
> El proveedor no debe mostrar un cuadro de diálogo durante el inicio de sesión. Si no se establece este indicador, el proveedor puede mostrar un cuadro de diálogo para preguntar al usuario para que falta información de configuración.
    
MAPI_DEFERRED_ERRORS 
  
> Permite el **Inicio de sesión** devolver de correctamente, posiblemente antes de que finalice el proceso de inicio de sesión. 
    
MAPI_UNICODE. 
  
> Todas las cadenas deben estar en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas deben estar en formato ANSI.
    
 _lpulcbSecurity_
  
> [entrada, salida] Un puntero al tamaño, en bytes, de la estructura de las credenciales de seguridad indicada por el parámetro _lppbSecurity_ . En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero. En ambos casos, los punteros deben ser válidos. 
    
 _lppbSecurity_
  
> [entrada, salida] Un puntero a un puntero a las credenciales de seguridad. En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero. En ambos casos, el puntero debe ser válido.
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a una estructura [MAPIERROR](mapierror.md) . El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
 _lppABLogon_
  
> [out] Un puntero a un puntero al objeto de inicio de sesión del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente una conexión a una sesión activa.
    
MAPI_E_FAILONEPROVIDER 
  
> El proveedor no puede iniciar sesión, pero puede seguir los otros proveedores en el servicio de mensajes a la que pertenece el proveedor de inicio de sesión MAPI. 
    
MAPI_E_UNCONFIGURED 
  
> El proveedor tiene información suficiente para completar el inicio de sesión. MAPI llama a la función de entrada de servicio de mensajes del proveedor.
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo de inicio de sesión. 
    
## <a name="remarks"></a>Comentarios

Las conexiones se establecen con cada proveedor de la libreta de direcciones en el perfil de sesión cuando un cliente llama al método [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) . **OpenAddressBook** , a continuación, llama el método de **Inicio de sesión** de cada proveedor. 
  
El nombre del perfil que apunta el parámetro _lpszProfileName_ se muestra en el juego de caracteres del cliente del usuario como se indica por la presencia o ausencia de la marca MAPI_UNICODE en el parámetro _ulFlags indicado_ . 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

En la implementación del método de **Inicio de sesión** , llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar un identificador único o la estructura [MAPIUID](mapiuid.md) . Cada uno de los objetos tendrá un identificador de entrada que incluye este **MAPIUID**. MAPI utiliza el **MAPIUID** para que coincida con un objeto con su proveedor. Por ejemplo, cuando un cliente llama al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un usuario de mensajería, **OpenEntry** examina la parte **MAPIUID** del identificador de entrada que se pasó y coincide con un **MAPIUID** registrado por un proveedor de libreta de direcciones. 
  
Si un cliente inicia sesión en su proveedor de más de una vez, es posible que desee registrar un **MAPIUID** de diferentes para cada inicio de sesión. Registrar las estructuras **MAPIUID** únicas permite MAPI enrutar correctamente las solicitudes a la instancia de proveedor adecuado. Sin embargo, es posible que desea que tengan cada objeto de inicio de sesión compartir uno **MAPIUID**. En este caso, debe ser capaz de controlar el enrutamiento de sí mismo en lugar de depender de la MAPI. Para obtener más información acerca de cómo crear un **MAPIUID**, vea [Identificadores únicos proveedor de servicio de registro](registering-service-provider-unique-identifiers.md).
  
El objeto de soporte técnico que MAPI se pasa al método de **Inicio de sesión** en el parámetro _lpMAPISup_ proporciona acceso a muchos de los métodos incluidos en la [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz. MAPI crea un objeto de soporte técnico personalizado para el tipo de proveedor. Por ejemplo, si necesita iniciar sesión en un sistema de mensajería subyacente o el servicio de directorio al establecer la conexión, puede llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar las credenciales de seguridad para esta sesión de inicio de sesión determinado. 
  
Si el **Inicio de sesión** es correcta, asegúrese de que llame al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) del objeto de soporte técnico para incrementar su recuento de referencia. Esto permite a su proveedor retener el puntero del objeto de soporte técnico para el resto de la sesión. Si no se llama a este método **AddRef** , MAPI descargará su proveedor. 
  
Puede incluir el nombre de perfil que se pasa en el parámetro _lpszProfileName_ en otras interfaces de usuario, pantallas de inicio de sesión o cuadros de diálogo de error. Para usar el nombre del perfil, cópielo en el almacenamiento que haya asignado. 
  
Crear un objeto de inicio de sesión y devolver un puntero a ella en el parámetro _lppABLogon_ . MAPI utiliza este objeto de inicio de sesión para realizar llamadas a los métodos en su implementación [IABLogon](iablogoniunknown.md) . 
  
Si necesita una contraseña durante el inicio de sesión, mostrar un cuadro de diálogo de inicio de sesión sólo si no se establece la marca AB_NO_DIALOG. Si el usuario cancela el proceso de inicio de sesión, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo devolver MAPI_E_USER_CANCEL de **Inicio de sesión**.
  
Normalmente, cuando un proveedor de la libreta de direcciones no puede iniciar sesión, MAPI deshabilita el servicio de mensajes a la que pertenece el proveedor con errores, es decir, MAPI no intentará establecer conexiones para cualquiera de los otros proveedores que pertenecen al servicio para el resto de la sesión período de duración. Sin embargo, si el proveedor no puede establecer una conexión y no desea deshabilitar todo el servicio, devolver MAPI_E_FAILONEPROVIDER o MAPI_E_UNCONFIGURED. MAPI no deshabilita el servicio de mensajes a la que pertenece el proveedor. 
  
Retorno MAPI_E_FAILONEPROVIDER si produce un error no es lo suficientemente grave como para impedir que los otros proveedores en el servicio de mensajes establecer conexiones. Devolver MAPI_E_UNCONFIGURED si falta la información de configuración necesaria desde el perfil y no se puede mostrar un cuadro de diálogo para preguntar al usuario. MAPI responderá al llamar a la función de punto de entrada de servicio del su proveedor mensaje con MSG_SERVICE_CONFIGURE establecido como el parámetro _ulContext_ para proporcionar el servicio de una oportunidad para configurarse a sí mismo, ya sea mediante programación o mediante una hoja de propiedades. Cuando elija la entrada de mensajes de servicio finalizado (función), el inicio de sesión de reintentos de MAPI. 
  
## <a name="see-also"></a>Vea también



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

