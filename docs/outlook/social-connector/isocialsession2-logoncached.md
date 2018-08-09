---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Inicie sesión en el sitio de red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821133"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Inicie sesión en el sitio de red social mediante el uso de credenciales almacenadas en caché.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parámetros

_Configuración_
  
> [entrada] Una cadena que puede estar vacía o contiene las credenciales de inicio de sesión, según el contexto en el que el OSC está llamando a **LogonCached**.
    
_userName_
  
> [entrada] Una cadena que contiene el nombre de usuario.
    
_contraseña_
  
> [entrada] Una cadena que contiene la contraseña del usuario.
    
_connectOut_
  
> [out] Una cadena opaca que contiene las credenciales.
    
## <a name="remarks"></a>Comentarios

Se llama a este método de autenticación sólo si **useLogonCached** se establece como **true** en el XML de las **capacidades de** devuelto por [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) llama a **LogonCached**y le pasa una cadena vacía para la _configuración_ y cadenas de _nombre de usuario_ y _contraseña_ no vacías. El proveedor usa el _nombre de usuario_ y _contraseña_ para iniciar sesión en la red social y devuelve un parámetro opaco _connectOut_ para el OSC si la autenticación se realiza correctamente. Si se produce un error en la autenticación, el proveedor devuelve el error OSC_E_LOGON_FAILURE para el OSC. 
  
El parámetro _connectOut_ es una cadena opaca para el OSC y se pasa para el parámetro de _configuración_ en los intentos posteriores por el OSC para iniciar sesión en la red social. El proveedor debe colocar todas las credenciales en la cadena de _connectOut_ que el proveedor desea el OSC para almacenar a través de conexiones. El OSC no interpreta la cadena en _connectOut_y cifra la cadena por razones de seguridad antes de almacenarlos en el registro de Windows.
  
## <a name="see-also"></a>Vea también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

