---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtiene una cadena que representa los detalles de la persona, como el nombre, el apellido y una dirección URL de una imagen de perfil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427335"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtiene una cadena que representa los detalles de la persona, como el nombre, el apellido y una dirección URL de una imagen de perfil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameters

_details_
  
> [salida] Valor de cadena XML que representa los detalles de una persona.
    
## <a name="remarks"></a>Comentarios

La _cadena_ XML de detalles devueltos debe cumplir con la definición de esquema para persona **,** tal como se define en el esquema para la extensibilidad del proveedor Outlook Social Connector (OSC).
  
El OSC llama **a GetDetails** si el proveedor de OSC admite la sincronización híbrida o en caché de amigos en la red social. Cuando el OSC obtiene inicialmente las actividades de los amigos para el usuario que ha iniciado sesión, llama a [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y almacena la información de los amigos en una carpeta de contactos específica de la red social, en el almacén de Outlook predeterminado del usuario. Posteriormente, el OSC no llama a **GetFriendsAndColleagues** o **GetDetails** a menos que el intervalo de actualización de la memoria caché haya expirado. Para obtener más información acerca de cómo el OSC almacena en caché la información de los amigos en una carpeta de contactos, vea [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Vea también

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

