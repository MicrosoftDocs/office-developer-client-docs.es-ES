---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Inicia sesión en el sitio de red social mediante la autenticación basada en formularios.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335367"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Inicia sesión en el sitio de red social mediante la autenticación basada en formularios.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameters

_connecten_
  
> a Una cadena que es **null**, una dirección URL a un formulario de inicio de sesión en la web o una cadena que contiene las credenciales de inicio de sesión, en función del contexto del proceso de inicio de sesión cuando se llama a este método.
    
_connectOut_
  
> contempla Una cadena que contiene las credenciales de inicio de sesión.
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC) llama al método **LogonWeb** solo si el proveedor indica que admite la autenticación basada en formularios. El proveedor indica que requiere autenticación basada en formularios estableciendo **useLogonWebAuth** como **true** en el XML para **capacidades**. Si el proveedor establece **useLogonWebAuth** como **false**, OSC utiliza la autenticación básica y llama al método [ISocialSession:: Logon](isocialsession-logon.md) . 
  
El inicio de sesión en un sitio de red social mediante la autenticación basada en formularios implica llamar a los métodos **LogonWeb** y [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) en un orden específico: 
  
1. El OSC llama a **LogonWeb** por primera vez, pasando **null** al parámetro _connecten_ . 
    
2. El proveedor genera el error OSC_E_AUTH_ERROR en el OSC.
    
3. El OSC siguiente llama a **GetLogonUrl**.
    
4. El proveedor devuelve la dirección URL correspondiente a una página de inicio de sesión en el método **GetLogonUrl** . 
    
5. El OSC usa la dirección URL devuelta por **GetLogonUrl** para mostrar la página de inicio de sesión basada en formularios. 
    
6. A continuación, el OSC llama a **LogonWeb** por segunda vez, pasando la dirección URL al formulario de inicio de sesión en el parámetro _connecten_ . 
    
7. Si la autenticación se realiza correctamente, el proveedor devuelve las credenciales de inicio de sesión en el parámetro _connectOut_ al OSC. Si se produce un error en la autenticación, el proveedor genera el error OSC_E_AUTH_ERROR en el OSC. 
    
Si el proveedor de OSC admite el inicio de sesión con credenciales almacenadas en caché, especifica **useLogonCached** como **true** en el XML de **funciones** . El proveedor debe ubicar las credenciales de inicio de sesión en la cadena _connectOut_ que el proveedor desea que el OSC almacene entre las conexiones. El OSC no interpreta la cadena _connectOut_ . Una vez que el OSC comprueba que **useLogonCached** es **true**, el OSC cifra la cadena por seguridad antes de almacenarla en el registro de Windows. El OSC pasa esta cadena al parámetro _connecten_ en los intentos subsiguientes de iniciar sesión en la red social llamando a [ISocialSession2:: LogonCached](isocialsession2-logoncached.md). 
  
Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticación basada en formularios](forms-based-authentication.md)

