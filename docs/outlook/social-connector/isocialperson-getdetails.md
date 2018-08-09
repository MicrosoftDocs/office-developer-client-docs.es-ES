---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtiene una cadena que representa los detalles de la persona, como el nombre, apellidos y una dirección URL a una imagen de perfil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821093"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtiene una cadena que representa los detalles de la persona, como el nombre, apellidos y una dirección URL a una imagen de perfil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parámetros

_detalles_
  
> [out] Un valor de cadena XML que representa los detalles de una persona.
    
## <a name="remarks"></a>Comentarios

La cadena XML devuelto _Detalles_ debe cumplir con la definición del esquema para la **persona**, tal como se define en el esquema para la extensibilidad de proveedor de Outlook Social Connector (OSC).
  
Las llamadas de OSC **GetDetails** si el proveedor OSC es compatible con caché o sincronización híbrido de amigos en la red social. Cuando el OSC inicialmente Obtiene las actividades de amigos para que el usuario ha iniciado la sesión, llama a [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y almacena información de amigos en una carpeta de contactos específica a la red social, en el almacén de Outlook predeterminado del usuario conectado . Posteriormente el OSC no llama a **GetFriendsAndColleagues** o **GetDetails** a menos que el intervalo de actualización de la memoria caché ha expirado. Para obtener más información acerca de cómo el OSC recopila información de amigos en una carpeta de contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Vea también

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

