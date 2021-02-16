---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Inicia sesión en el sitio de la red social con el nombre de usuario y la contraseña especificados.
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361043"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Inicia sesión en el sitio de la red social con el nombre de usuario y la contraseña especificados.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parámetros

_username_
  
> [entrada] Cadena que contiene el nombre de usuario al que se debe iniciar sesión.
    
_password_
  
> [entrada] Cadena que contiene la contraseña para iniciar sesión.
    
## <a name="see-also"></a>Consulte también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

