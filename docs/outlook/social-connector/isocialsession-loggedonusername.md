---
title: ISocialSessionLoggedOnUserName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c0e7b788-3198-499c-ae21-b2032f929ed9
description: Devuelve un valor de tipo string que representa el nombre de usuario que se usa al inicio de sesión.
ms.openlocfilehash: 02485ad2a510a81c64406ea6ec9a0f85c0e4d2f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821241"
---
# <a name="isocialsessionloggedonusername"></a>ISocialSession::LoggedOnUserName

Devuelve un valor de tipo string que representa el nombre de usuario que se usa al inicio de sesión.
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserName([out, retval] BSTR* result);
```

## <a name="property-value"></a>Valor de propiedad

Una cadena que representa el nombre de usuario del usuario que ha iniciado la sesión.
  
## <a name="see-also"></a>Vea también

- [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md)  
- [ISocialSession : IUnknown](isocialsessioniunknown.md)

