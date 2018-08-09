---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Quita a la persona identificada por el parámetro userID como amigo en la red social.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821127"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Quita a la persona identificada por el parámetro _userID_ como amigo en la red social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parámetros

_userID_
  
> [entrada] Una cadena que contiene un identificador de usuario de redes sociales de una persona.
    
## <a name="remarks"></a>Comentarios

El parámetro _userID_ debe ser un identificador de usuario válido para la persona en la red social. 
  
Si el proveedor de Outlook Social Connector (OSC) ha establecido **doNotFollowPerson** como **true** en el XML de **las capacidades**, el proveedor debe devolver el error OSC_E_NOT_FOUND en el caso de que el usuario identificador que se pasó no coincide con un usuario en la red. Si el proveedor ha establecido **doNotFollowPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

