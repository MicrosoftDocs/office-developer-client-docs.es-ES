---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Agrega la persona identificada por los parámetros emailAddresses y displayName como un amigo del usuario que ha iniciado sesión en la red social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429834"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Agrega la persona identificada por los parámetros  _emailAddresses_ y  _displayName_ como un amigo del usuario que ha iniciado sesión en la red social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parámetros

_emailAddresses_
  
> [entrada] Matriz que contiene una o varias direcciones SMTP válidas para una persona en la red social.
    
_displayName_
  
> [entrada] Cadena que contiene el nombre para mostrar de la persona que se agregará como amigo.
    
## <a name="remarks"></a>Comentarios

Si outlook Social Connector (OSC) proporciona más que la dirección SMTP en la matriz en el parámetro **emailAddresses,** el proveedor de OSC puede suponer que el primer elemento es la dirección SMTP principal. 
  
Si el proveedor ha establecido el elemento **followPerson** como **true** en el **XML** de capacidades y ninguno de los elementos de  _emailAddresses_ coincide con un usuario de la red, el proveedor debe devolver el error OSC_E_NOT_FOUND. Si el proveedor ha establecido **followPerson** como **false** en las capacidades, el proveedor debe devolver el OSC_E_FAIL error. 
  
Si el método **FollowPersonEx** se realiza correctamente, el proveedor puede usar la cadena del parámetro  _displayName_ para dirigirse a la persona en cualquier correo electrónico de confirmación de amigos posterior, en lugar de dirigirse a la persona por la dirección SMTP. Por otro lado, el proveedor debe ser capaz de controlar el OSC pasando una cadena vacía para el _parámetro displayName._ 
  
Si el proveedor implementa la interfaz [ISocialSession2](isocialsession2iunknown.md) y ha establecido **followPerson** como **true** en el XML de capacidades, el OSC llama **a FollowPersonEx** en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md). Si el proveedor ha establecido **followPerson** como **true** pero no implementa la interfaz **ISocialSession2,** o **FollowPersonEx** devuelve el error OSC_E_NOTIMPL, el OSC llama a **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Consulte también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

