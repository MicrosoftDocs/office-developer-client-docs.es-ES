---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Agrega a la persona identificada por el parámetro emailAddress como amigo para el usuario ha iniciado sesión en la red social.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821118"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Agrega a la persona identificada por el parámetro _emailAddress_ como amigo para el usuario ha iniciado sesión en la red social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parámetros

_emailAddress_
  
> [entrada] Una cadena que contiene una dirección de correo electrónico de una persona.
    
## <a name="remarks"></a>Comentarios

El parámetro _emailAddress_ debe ser una dirección SMTP válida. Si el proveedor de Outlook Social Connector (OSC) ha establecido el método **followPerson** como **true** en **las capacidades**y el argumento para _emailAddress_ no coincide con un usuario en la red, el proveedor debe devolver el OSC_E_NOT_FOUND error. Si el proveedor ha establecido **followPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL.
  
Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en **funciones**, el OSC llamará a [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) en lugar de **ISocialSession::FollowPerson **. Si el proveedor no implementa la interfaz **ISocialSession2** o **ISocialSession2::FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llamará a **ISocialSession::FollowPerson** siempre que el proveedor ha establecido ** followPerson** como **true** en **funciones**. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
La hora de decidir si implementar **ISocalSession::FollowPerson** o **ISocialSession2::FollowPersonEx**, se debe tener en cuenta si su proveedor de las necesidades de los otros métodos de **ISocialSession2**y si puede usar el _ djsplayName_ parámetro en **FollowPersonEx**.
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

