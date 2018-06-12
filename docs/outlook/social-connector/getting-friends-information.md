---
title: Obtención de información de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) llama al método de ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821083"
---
# <a name="getting-friends-information"></a>Obtención de información de amigos

Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. Si los elementos **getFriends** y **cacheFriends** en el devuelto XML de las **capacidades de** indican que el proveedor de OSC admite a Introducción amigos y amigos de almacenamiento en caché como Outlook, póngase en contacto con los elementos en una carpeta de contactos correspondiente, puede hacer que el OSC la siguiente secuencia de llamada. El OSC llama a métodos en esta secuencia para obtener información y las imágenes (como compatible con la interfaz de [ISocialPerson](isocialpersoniunknown.md) ) para amigos en la red social. 
  
> [!NOTE]
> El OSC actualiza la memoria caché en un intervalo predeterminado. Si se produce un error durante la memoria caché de actualizar, los reintentos OSC en otro intervalo preestablecido, que también se pueden controlar mediante la especificación del elemento **contactSyncRestartInterval** en el XML de las **capacidades** . Para obtener más información acerca de cómo actualizar la memoria caché de los contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) : el OSC Obtiene el identificador de usuario del usuario de Office que ha iniciado sesión en la red social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) — con el identificador de usuario del usuario de Office, el OSC Obtiene un objeto **ISocialPerson** para ese usuario. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) : el OSC Obtiene la lista del usuario amigo en la red social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) : para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC Obtiene una interfaz **ISocialPerson** . 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) : para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC Obtiene un recurso de imagen.
    
## <a name="see-also"></a>Ver también

- [XML de capacidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

