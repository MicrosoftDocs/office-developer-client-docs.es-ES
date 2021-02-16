---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtiene una cadena que representa una colección de personas.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407658"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtiene una cadena que representa una colección de personas.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parámetros

_personsCollection_
  
> [salida] Cadena XML que representa un conjunto de amigos de la persona  y que cumple con la definición de amigos definida en el esquema XML para la extensibilidad del proveedor de Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Comentarios

El OSC llama a **GetFriendsAndColleagues** si el proveedor de OSC admite la sincronización híbrida o en caché de amigos en la red social. Cuando el OSC llama inicialmente al método **GetFriendsAndColleagues** para el usuario de Outlook que ha iniciado sesión en la red social, **GetFriendsAndColleagues** devuelve una cadena XML que representa a los amigos del usuario que ha iniciado sesión en la red social. La cadena XML cumple con la definición del esquema **XML** de amigos y especifica un elemento **person** (que también cumple con la definición de esquema del proveedor de OSC) para cada amigo. 
  
Cuando **GetFriendsAndColleagues** devuelve la información de amigos del usuario que ha iniciado sesión, el OSC almacena esa información en una carpeta de contactos. Esta carpeta es específica de la red social y reside en el almacén de Outlook predeterminado del usuario que ha iniciado sesión. Para obtener más información sobre cómo el OSC almacena en caché la información de los amigos en una carpeta de contactos, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)
  
La información de cada amigo devuelto en el  _parámetro personsCollection_ cumple con la definición del esquema XML para **la persona**. El elemento **person** admite muchas partes de información para cada amigo, incluidas las direcciones de correo electrónico SMTP (que se asignan a los elementos **emailAddress**, **emailAddress2** y **emailAddress3)** que el amigo ha especificado en la red social, y el identificador de usuario (que se asigna al elemento **userID)** que identifica a ese amigo en la red social. 
  
Para mostrar actividades para un usuario de Outlook seleccionado en el panel de personas, el OSC intenta hacer coincidir al usuario con cada amigo devuelto de **GetFriendsAndColleagues**. Para ello, el OSC hace coincidir la dirección SMTP del usuario de Outlook seleccionado con las direcciones de correo electrónico que cada amigo ha especificado en la red social. Si el OSC encuentra una dirección de correo electrónico SMTP que coincida, el OSC usa el **userID** correspondiente del amigo para llamar al método [ISocialSession::GetPerson.](isocialsession-getperson.md) Lo hace para obtener un objeto [ISocialPerson](isocialpersoniunknown.md) para ese amigo, lo que permite al OSC obtener actividades e imágenes de ese amigo de la red social. 
  
Sin embargo, si el usuario de Outlook seleccionado no especifica esa misma dirección SMTP en una cuenta de la red social, o si el usuario de Outlook no tiene una cuenta en esa red social, el OSC no podrá encontrar una coincidencia para ese usuario y no mostrará ninguna actividad para ese usuario en la red social.
  
## <a name="see-also"></a>Consulte también

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtener información de amigos](getting-friends-information.md)

