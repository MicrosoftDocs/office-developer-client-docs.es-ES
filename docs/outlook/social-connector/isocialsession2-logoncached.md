---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Inicia sesión en el sitio de red social mediante credenciales almacenadas en caché.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436625"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Inicia sesión en el sitio de red social mediante credenciales almacenadas en caché.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in] Una cadena que puede estar vacía o contiene las credenciales de inicio de sesión, según el contexto en el que el OSC llama a **LogonCached**.
    
_userName_
  
> [in] Cadena que contiene el nombre de usuario.
    
_password_
  
> [in] Cadena que contiene la contraseña del usuario.
    
_connectOut_
  
> [salida] Una cadena opaca que contiene credenciales.
    
## <a name="remarks"></a>Comentarios

Este método se llama para la autenticación solo si **useLogonCached** se establece como **true** en las capacidades **XML** devueltas por [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
El Outlook Social Connector (OSC) llama a **LogonCached** y pasa una cadena vacía para las cadenas _connectIn_ y _no vacías userName_ y _password._ El proveedor usa  _userName_ y  _contraseña_ para iniciar sesión en la red social y devuelve un parámetro  _connectOut_ opaco al OSC si la autenticación se realiza correctamente. Si se produce un error en la autenticación, el proveedor devuelve OSC_E_LOGON_FAILURE error al OSC. 
  
El  _parámetro connectOut_ es una cadena opaca al OSC y se pasa al parámetro  _connectIn_ en los intentos posteriores del OSC de iniciar sesión en la red social. El proveedor debe colocar las credenciales en la  _cadena connectOut_ que el proveedor desea que el OSC almacene entre conexiones. El OSC no interpreta la cadena en _connectOut_ y cifra la cadena por motivos de seguridad antes de almacenarla en el Windows registro.
  
## <a name="see-also"></a>Vea también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

