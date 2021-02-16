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
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348786"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada] Puntero al objeto de compatibilidad del proveedor de libreta de direcciones.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo de inicio de sesión que muestra el método **de** inicio de sesión, si se permite. El _parámetro ulUIParam_ contiene el valor del parámetro del mismo nombre pasado a MAPI en la llamada anterior a la [función MAPILogonEx.](mapilogonex.md) 
    
 _lpszProfileName_
  
> [entrada] Puntero al nombre del perfil de sesión.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza el inicio de sesión. Se pueden establecer las siguientes marcas:
    
AB_NO_DIALOG 
  
> El proveedor no debe mostrar un cuadro de diálogo durante el inicio de sesión. Si no se establece esta marca, el proveedor puede mostrar un cuadro de diálogo para solicitar al usuario la información de configuración que falta.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que el inicio** de sesión vuelva correctamente, posiblemente antes de que finalice el proceso de inicio de sesión. 
    
MAPI_UNICODE 
  
> Todas las cadenas deben estar en formato Unicode. Si no MAPI_UNICODE marca, las cadenas deben estar en formato ANSI.
    
 _lpulcbSecurity_
  
> [entrada, salida] Puntero al tamaño, en bytes, de la estructura de credenciales de seguridad a la que apunta el _parámetro lppbSecurity._ En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero. En ambos casos, los punteros deben ser válidos. 
    
 _lppbSecurity_
  
> [entrada, salida] Puntero a un puntero a credenciales de seguridad. En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero. En ambos casos, el puntero debe ser válido.
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a una [estructura MAPIERROR.](mapierror.md) El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
 _lppABLogon_
  
> [salida] Puntero a un puntero al objeto de inicio de sesión del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente una conexión a una sesión activa.
    
MAPI_E_FAILONEPROVIDER 
  
> El proveedor no puede iniciar sesión, pero MAPI puede continuar iniciando sesión en los demás proveedores en el servicio de mensajes al que pertenece el proveedor. 
    
MAPI_E_UNCONFIGURED 
  
> El proveedor no tiene información suficiente para completar el inicio de sesión. MAPI llama a la función de entrada del servicio de mensajes del proveedor.
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar del cuadro de diálogo de inicio de sesión. 
    
## <a name="remarks"></a>Comentarios

Las conexiones se establecen con cada proveedor de libreta de direcciones en el perfil de sesión cuando un cliente llama al método [IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md) **A continuación, OpenAddressBook** llama al método de inicio de **sesión de cada** proveedor. 
  
El nombre de perfil al que apunta el parámetro _lpszProfileName_ se muestra en el juego de caracteres del cliente del usuario, como se indica mediante la presencia o ausencia de la marca MAPI_UNICODE en el parámetro _ulFlags._ 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

En la implementación del método **Logon,** llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar un identificador único o estructura [MAPIUID.](mapiuid.md) Cada uno de los objetos tendrá un identificador de entrada que incluye este **MAPIUID**. MAPI usa **MAPIUID para** hacer coincidir un objeto con su proveedor. Por ejemplo, cuando un cliente llama al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un usuario de mensajería, **OpenEntry** examina la parte **MAPIUID** del identificador de entrada que se pasó y la encuentra con **un MAPIUID** registrado por un proveedor de libreta de direcciones. 
  
Si un cliente inicia sesión en su proveedor más de una vez, es posible que desee registrar un **MAPIUID diferente** para cada inicio de sesión. El registro de estructuras **MAPIUID** únicas permite a MAPI enrutar correctamente las solicitudes a la instancia de proveedor adecuada. Sin embargo, es posible que desee que cada objeto de inicio de sesión comparta un **MAPIUID**. En este caso, debe poder controlar el enrutamiento usted mismo en lugar de depender de MAPI. Para obtener más información acerca de cómo crear **un MAPIUID,** vea [Registrar identificadores únicos](registering-service-provider-unique-identifiers.md)del proveedor de servicios.
  
El objeto de compatibilidad que MAPI pasa al método **Logon** en el parámetro _lpMAPISup_ proporciona acceso a muchos de los métodos incluidos en la interfaz [IMAPISupport : IUnknown.](imapisupportiunknown.md) MAPI crea un objeto de compatibilidad personalizado para el tipo de proveedor. Por ejemplo, si necesita iniciar sesión en un sistema de mensajería subyacente o un servicio de directorio al establecer la conexión, puede llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar credenciales de seguridad para esta sesión de inicio de sesión en particular. 
  
Si **el** inicio de sesión se realiza correctamente, asegúrese de llamar al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto de compatibilidad para incrementar el recuento de referencias. Esto permite al proveedor mantener el puntero del objeto de compatibilidad durante el resto de la sesión. Si no llama a este **método AddRef,** MAPI descargará el proveedor. 
  
Puede incluir el nombre de perfil pasado en el parámetro  _lpszProfileName_ en cuadros de diálogo de error, pantallas de inicio de sesión u otras interfaces de usuario. Para usar el nombre del perfil, cópielo en el almacenamiento que haya asignado. 
  
Cree un objeto de inicio de sesión y devuelva un puntero a él en el _parámetro lppABLogon._ MAPI usa este objeto de inicio de sesión para realizar llamadas a los métodos de la [implementación de IABLogon.](iablogoniunknown.md) 
  
Si necesita una contraseña durante el inicio de sesión, muestre un cuadro de diálogo de inicio de sesión solo si no AB_NO_DIALOG marca de inicio de sesión. Si el usuario cancela el proceso de  inicio de sesión, normalmente haciendo clic en el botón Cancelar del cuadro de diálogo, devuelva MAPI_E_USER_CANCEL de **inicio de sesión.**
  
Normalmente, cuando un proveedor de libreta de direcciones no puede iniciar sesión, MAPI deshabilita el servicio de mensajes al que pertenece el proveedor con errores, es decir, MAPI no intentará establecer conexiones para ninguno de los otros proveedores que pertenecen al servicio durante el resto de la duración de la sesión. Sin embargo, si el proveedor no puede establecer una conexión y no desea deshabilitar todo el servicio, devuelva MAPI_E_FAILONEPROVIDER o MAPI_E_UNCONFIGURED. MAPI no deshabilitará el servicio de mensajes al que pertenece el proveedor. 
  
Devuelve MAPI_E_FAILONEPROVIDER si se produce un error que no es lo suficientemente grave como para impedir que los demás proveedores del servicio de mensajes establezcan conexiones. Devuelve MAPI_E_UNCONFIGURED si falta la información de configuración necesaria en el perfil y no se puede mostrar un cuadro de diálogo para preguntar al usuario. MAPI responderá llamando a la función de punto de entrada del servicio de mensajes del proveedor con MSG_SERVICE_CONFIGURE establecido como parámetro  _ulContext_ para dar al servicio la oportunidad de configurarse, ya sea mediante programación o mediante una hoja de propiedades. Una vez finalizada la función de punto de entrada del servicio de mensajes, MAPI vuelve a iniciar sesión. 
  
## <a name="see-also"></a>Consulte también



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

