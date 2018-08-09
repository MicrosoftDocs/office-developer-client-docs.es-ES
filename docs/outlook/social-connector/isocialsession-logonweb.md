---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Inicie sesión en el sitio de red social mediante la autenticación basada en formularios.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821126"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Inicie sesión en el sitio de red social mediante la autenticación basada en formularios.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parámetros

_Configuración_
  
> [entrada] Una cadena que es **null**, una dirección URL a un formulario de inicio de sesión en el web o una cadena que contiene las credenciales de inicio de sesión, según el contexto en el proceso de inicio de sesión cuando se llama a este método.
    
_connectOut_
  
> [out] Una cadena que contiene las credenciales de inicio de sesión.
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC) llama al método de **LogonWeb** sólo si el proveedor indica que admite la autenticación basada en formularios. El proveedor indica que requiere la autenticación basada en formularios mediante la configuración de **useLogonWebAuth** como **true** en el XML de **las capacidades**. Si el proveedor establece **useLogonWebAuth** como **false**, el OSC usa la autenticación básica y llama al método [ISocialSession::Logon](isocialsession-logon.md) . 
  
Inicie sesión en un sitio de red social mediante la autenticación basada en formularios implica llamar a los métodos **LogonWeb** y [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) en un orden específico: 
  
1. El OSC llama **LogonWeb** la primera vez, pasando **null** para el parámetro de _configuración_ . 
    
2. El proveedor genera el error OSC_E_AUTH_ERROR para el OSC.
    
3. A continuación, el OSC llama a **GetLogonUrl**.
    
4. El proveedor devuelve la dirección URL apropiada a una página de inicio de sesión en el método **GetLogonUrl** . 
    
5. El OSC usa la dirección URL devuelta por **GetLogonUrl** para mostrar la página de inicio de sesión basado en formularios. 
    
6. El OSC, a continuación, llama a **LogonWeb** una segunda vez, pasando la dirección URL para el formulario de inicio de sesión en el parámetro de _configuración_ . 
    
7. Si la autenticación se realiza correctamente, el proveedor devuelve las credenciales de inicio de sesión en el parámetro _connectOut_ para el OSC. Si se produce un error en la autenticación, el proveedor genera el error OSC_E_AUTH_ERROR para el OSC. 
    
Si el proveedor OSC admite el inicio de sesión con credenciales almacenadas en caché, especifica **useLogonCached** como **true** en el XML de las **capacidades** . El proveedor debe colocar todas las credenciales de inicio de sesión en la cadena de _connectOut_ que el proveedor desea el OSC para almacenar a través de conexiones. El OSC no interpreta la cadena _connectOut_ . Una vez que el OSC comprueba que **useLogonCached** es **true**, el OSC cifra la cadena para la seguridad antes de almacenarlos en el registro de Windows. El OSC pasa esta cadena para el parámetro de _configuración_ en los intentos posteriores para iniciar sesión en la red social mediante una llamada a [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticación basada en formularios](forms-based-authentication.md)

