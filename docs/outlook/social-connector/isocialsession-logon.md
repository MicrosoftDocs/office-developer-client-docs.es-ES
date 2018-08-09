---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Inicie sesión en el sitio de red social utilizando el nombre de usuario especificado y la contraseña.
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821121"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Inicie sesión en el sitio de red social utilizando el nombre de usuario especificado y la contraseña.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parámetros

_nombre de usuario_
  
> [entrada] Una cadena que contiene el nombre de usuario para iniciar sesión.
    
_contraseña_
  
> [entrada] Una cadena que contiene la contraseña para iniciar sesión.
    
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

