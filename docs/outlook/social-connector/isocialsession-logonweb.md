---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Inicia sesión en el sitio de la red social mediante la autenticación basada en formularios.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430339"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Inicia sesión en el sitio de la red social mediante la autenticación basada en formularios.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parámetros

_connectIn_
  
> [entrada] Una cadena que es **nula,** una dirección URL a un formulario de inicio de sesión en la Web o una cadena que contiene credenciales de inicio de sesión, según el contexto del proceso de inicio de sesión cuando se llama a este método.
    
_connectOut_
  
> [salida] Cadena que contiene credenciales de inicio de sesión.
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC) llama al método **LogonWeb** solo si el proveedor indica que admite la autenticación basada en formularios. El proveedor indica que requiere autenticación basada en formularios estableciendo **useLogonWebAuth** como **true** en el XML para las **capacidades.** Si el proveedor establece **useLogonWebAuth** como **false,** el OSC usa la autenticación básica y llama al método [ISocialSession::Logon.](isocialsession-logon.md) 
  
Iniciar sesión en un sitio de red social mediante la autenticación basada en formularios implica llamar a los métodos **LogonWeb** e [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) en un orden específico: 
  
1. El OSC llama **a LogonWeb** la primera vez y pasa **null** al _parámetro connectIn._ 
    
2. El proveedor genera el OSC_E_AUTH_ERROR error al OSC.
    
3. A continuación, el OSC **llama a GetLogonUrl**.
    
4. El proveedor devuelve la dirección URL adecuada a una página de inicio de sesión en el **método GetLogonUrl.** 
    
5. El OSC usa la dirección URL devuelta por **GetLogonUrl** para mostrar la página de inicio de sesión basada en formularios. 
    
6. A continuación, el OSC llama a **LogonWeb** una segunda vez y pasa la dirección URL al formulario de inicio de sesión en el _parámetro connectIn._ 
    
7. Si la autenticación se realiza correctamente, el proveedor devuelve las credenciales de inicio de sesión en el parámetro  _connectOut_ al OSC. Si se produce un error en la autenticación, el proveedor genera OSC_E_AUTH_ERROR error al OSC. 
    
Si el proveedor de OSC admite el inicio de sesión con credenciales almacenadas en caché, especifica **useLogonCached** como **true** en el XML **de funcionalidades.** El proveedor debe colocar las credenciales de inicio de sesión en la cadena  _connectOut_ que el proveedor desea que el OSC almacene entre conexiones. El OSC no interpreta la _cadena connectOut._ Una vez que el OSC comprueba que **useLogonCached** es **true,** el OSC cifra la cadena por motivos de seguridad antes de almacenarla en el Registro de Windows. El OSC pasa esta cadena al parámetro  _connectIn_ en intentos posteriores de iniciar sesión en la red social llamando a [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticación basada en formularios](forms-based-authentication.md)

