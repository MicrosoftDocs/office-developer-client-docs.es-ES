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
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821102"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtiene una cadena que representa una colección de personas.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Sintaxis

_personsCollection_
  
> [out] Una cadena XML que representa un conjunto de amigos de la persona, y que cumple con la definición de **amigos** , tal como se define en el esquema XML de extensibilidad de proveedor de Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Notas

Las llamadas de OSC **GetFriendsAndColleagues** si el proveedor OSC es compatible con caché o sincronización híbrido de amigos en la red social. Cuando el OSC llama inicialmente al método **GetFriendsAndColleagues** para el usuario de Outlook que ha iniciado sesión en la red social, **GetFriendsAndColleagues** devuelve una cadena XML que representa los amigos del usuario ha iniciado sesión en la red social. La cadena XML cumple con la definición de esquema XML de **amigos** y especifica un elemento **person** (que también se ajusta a la definición de esquema de proveedor OSC) para cada uno de ellos. 
  
Cuando **GetFriendsAndColleagues** devuelve los amigos información para el usuario ha iniciado sesión, el OSC almacena esa información en una carpeta de contactos. Esta carpeta es específica de la red social y reside en el almacén de Outlook predeterminado del usuario que ha iniciado la sesión. Para obtener más información acerca de cómo el OSC recopila información de amigos en una carpeta de contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).
  
Información de cada amigo devuelto en el parámetro _personsCollection_ cumple con la definición del esquema XML para la **persona**. El elemento **person** admite muchos elementos de información para cada uno de ellos, incluidas las direcciones de correo electrónico SMTP (que se asignan a los elementos **emailAddress**, **emailAddress2**y **emailAddress3** ) que se ha especificado el amigo en el redes sociales y el identificador de usuario (que se asigna al elemento **userID** ) que identifica ese amigo en la red social. 
  
Para mostrar las actividades de un usuario de Outlook seleccionado en el panel de personas, el OSC intenta hacer coincidir el usuario con cada amigo devuelto desde **GetFriendsAndColleagues**. Para ello, el OSC que coincida con la dirección SMTP del usuario de Outlook seleccionado con las direcciones de correo electrónico que ha especificado cada uno de ellos en la red social. Si el OSC encuentra una dirección de correo electrónico SMTP coincidente, el OSC usa el correspondiente **userID** del amigo para llamar al método [ISocialSession::GetPerson](isocialsession-getperson.md) . Hace esto para obtener un objeto [ISocialPerson](isocialpersoniunknown.md) para ese amigo, que luego se habilita el OSC obtener las imágenes de ese amigo y actividades de la red social. 
  
Sin embargo, si el usuario de Outlook seleccionado no especifica esa misma dirección SMTP en una cuenta en la red social, o si el usuario de Outlook no tienen una cuenta en esa red social, el OSC no será capaz de encontrar a una coincidencia para que el usuario y no mostrará ningún activiti es de dicho usuario en la red social.
  
## <a name="see-also"></a>Ver también

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)
- [Obtener información sobre amigos](getting-friends-information.md)

