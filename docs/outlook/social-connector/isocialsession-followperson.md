---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Agrega la persona identificada por el parámetro emailAddress como un amigo para el usuario que ha iniciado sesión en la red social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285367"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Agrega la persona identificada por el parámetro _emailAddress_ como un amigo para el usuario que ha iniciado sesión en la red social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameters

_emailAddress_
  
> a Una cadena que contiene una dirección de correo electrónico de una persona.
    
## <a name="remarks"></a>Comentarios

El parámetro _emailAddress_ debe ser una dirección SMTP válida. Si el proveedor de Outlook Social Connector (OSC) ha establecido el método **followPerson** como **true** en las **funciones**y el argumento de _emailAddress_ no coincide con un usuario de la red, el proveedor debe devolver el OSC_E_NOT_FOUND error. Si el proveedor ha establecido **followPerson** como **false** en las **funciones**, el proveedor debe devolver el error OSC_E_FAIL.
  
Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en las **funciones**, el OSC llamará a [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) en lugar de **ISocialSession:: followPerson **. Si el proveedor no implementa la interfaz **ISocialSession2** , o **ISocialSession2:: FollowPersonEx** devuelve el error OSC_E_NOTIMPL, OSC llamará a **ISocialSession:: FollowPerson** siempre que el proveedor haya establecido ** followPerson** como **true** en **funciones**. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
A la hora de decidir si implementar **ISocalSession:: FollowPerson** o **ISocialSession2:: FollowPersonEx**, debe tener en cuenta si el proveedor necesita los otros métodos en **ISocialSession2**y si puede usar el _ parámetro djsplayName_ en **FollowPersonEx**.
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

