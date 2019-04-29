---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Inicia sesión en el sitio de red social mediante las credenciales almacenadas en caché.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436625"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Inicia sesión en el sitio de red social mediante las credenciales almacenadas en caché.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameters

_connecten_
  
> a Una cadena que puede estar vacía o que contiene las credenciales de inicio de sesión, en función del contexto en el que el OSC llama a **LogonCached**.
    
_userName_
  
> a Una cadena que contiene el nombre de usuario.
    
_password_
  
> a Una cadena que contiene la contraseña del usuario.
    
_connectOut_
  
> contempla Una cadena opaca que contiene las credenciales.
    
## <a name="remarks"></a>Comentarios

Se llama a este método para la autenticación solo si **useLogonCached** se establece como **true** en el XML de **capacidades** devuelto por [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) llama a **LogonCached**y pasa una cadena vacía para las cadenas de _nombre de usuario_ y _contraseña_ _conectadas_ y no vacías. El proveedor usa el _nombre de usuario_ y la _contraseña_ para iniciar sesión en la red social y devuelve un parámetro _connectOut_ opaco al OSC si la autenticación es correcta. Si se produce un error en la autenticación, el proveedor devuelve el error OSC_E_LOGON_FAILURE al OSC. 
  
El parámetro _connectOut_ es una cadena opaca para OSC y se pasa al parámetro connecten __ en los siguientes intentos del OSC para iniciar sesión en la red social. El proveedor debe situar las credenciales en la cadena _connectOut_ que el proveedor desea que el OSC almacene entre las conexiones. El OSC no interpreta la cadena en _connectOut_y cifra la cadena por motivos de seguridad antes de almacenarla en el registro de Windows.
  
## <a name="see-also"></a>Ver también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

