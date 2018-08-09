---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Agrega a la persona identificada por los parámetros emailAddresses y displayName como amigo para el usuario ha iniciado sesión en la red social.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821136"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Agrega a la persona identificada por los parámetros _emailAddresses_ y _displayName_ como amigo para el usuario ha iniciado sesión en la red social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parámetros

_emailAddresses_
  
> [entrada] Una matriz que contiene una o varias direcciones SMTP válidas para una persona en la red social.
    
_displayName_
  
> [entrada] Una cadena que contiene el nombre para mostrar de la persona que se agregará como un amigo.
    
## <a name="remarks"></a>Comentarios

Si Outlook Social Connector (OSC) proporciona más información que en la dirección SMTP de la matriz en el parámetro **emailAddresses** , el proveedor de OSC puede asumir que el primer elemento es la dirección SMTP principal. 
  
Si el proveedor ha establecido el elemento **followPerson** como **true** en el XML de las **capacidades** y ninguno de los elementos de _emailAddresses_ coincide con un usuario en la red, el proveedor debe devolver el error OSC_E_NOT_FOUND. Si el proveedor ha establecido **followPerson** como **false** en **funciones**, el proveedor debe devolver el error OSC_E_FAIL. 
  
Si el método **FollowPersonEx** se realiza correctamente, el proveedor puede utilizar la cadena en el parámetro _displayName_ a la persona en cualquier correo electrónico de confirmación de amigo subsiguientes, en lugar de hacer frente a la persona por la dirección SMTP de direcciones. Por otro lado, el proveedor debe ser capaz de controlar el OSC pasando una cadena vacía para el parámetro _displayName_ . 
  
Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en el XML de las capacidades, el OSC llama a **FollowPersonEx** en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md). Si el proveedor ha establecido **followPerson** como **true** pero no implementa la interfaz **ISocialSession2** , o **FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llama **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Vea también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

