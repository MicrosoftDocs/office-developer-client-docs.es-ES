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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336781"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Quita la persona identificada por el parámetro _userid_ como un amigo en la red social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameters

_Identificado_
  
> a Una cadena que contiene un identificador de usuario de red social para una persona.
    
## <a name="remarks"></a>Comentarios

El parámetro _userid_ debe ser un identificador de usuario válido para la persona en la red social. 
  
Si el proveedor de Outlook Social Connector (OSC) ha establecido **doNotFollowPerson** como **true** en el XML para **funciones**, el proveedor debe devolver el error OSC_E_NOT_FOUND en caso de que el identificador de usuario que se ha pasado no coincide con un usuario de la red. Si el proveedor ha establecido **doNotFollowPerson** como **false** en las **funciones**, el proveedor debe devolver el error OSC_E_FAIL. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

