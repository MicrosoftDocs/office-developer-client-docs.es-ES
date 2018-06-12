---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: Devuelve un valor de tipo string que representa el identificador de usuario de red social del usuario que ha iniciado sesión actualmente.
ms.openlocfilehash: dcc81d7acf8a839e7fe3249cc0eb06f96c113b56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821119"
---
# <a name="isocialsessionloggedonuserid"></a>ISocialSession::LoggedOnUserID

Devuelve un valor de tipo string que representa el identificador de usuario de red social del usuario que ha iniciado sesión actualmente. 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a>Valor de propiedad

Una cadena que contiene el identificador de usuario de red social del usuario que ha iniciado la sesión.
  
## <a name="see-also"></a>Ver también

- [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)  
- [ISocialSession: IUnknown](isocialsessioniunknown.md)

