---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Quita la persona identificada por el parámetro userID como un amigo en la red social.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418438"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Quita la persona identificada por el parámetro  _userID_ como un amigo en la red social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameters

_userID_
  
> [in] Cadena que contiene un identificador de usuario de red social para una persona.
    
## <a name="remarks"></a>Comentarios

El  _parámetro userID_ debe ser un identificador de usuario válido para la persona de la red social. 
  
Si el proveedor de Outlook Social Connector (OSC) ha establecido **doNotFollowPerson** como **true** en el XML para las funcionalidades, el proveedor debe devolver el error OSC_E_NOT_FOUND en caso de que el identificador de usuario pasado no coincida con un usuario de la red. Si el proveedor ha establecido **doNotFollowPerson** como **false** en las capacidades, el proveedor debe devolver el OSC_E_FAIL error. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

