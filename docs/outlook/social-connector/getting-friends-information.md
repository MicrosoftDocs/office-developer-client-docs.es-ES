---
title: Obtener información de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) llama al método ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428798"
---
# <a name="getting-friends-information"></a>Obtener información de amigos

Outlook Social Connector (OSC) llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. Si los elementos **getFriends** y **cacheFriends** en el **XML** de funcionalidades devueltas indican que el proveedor de OSC admite la obtención de amigos y el almacenamiento en caché de amigos como elementos de contacto de Outlook en una carpeta de contactos correspondiente, el OSC puede realizar la siguiente secuencia de llamada. El OSC llama a métodos en esta secuencia para obtener información e imágenes (como admite la interfaz [ISocialPerson)](isocialpersoniunknown.md) para amigos en la red social. 
  
> [!NOTE]
> El OSC actualiza la memoria caché en un intervalo predeterminado. Si se produce un error durante la actualización de la memoria caché, el OSC vuelve a iniciarse en otro intervalo preestablecido, que también se puede controlar especificando el elemento **contactSyncRestartInterval** en el XML de **funcionalidades.** Para obtener más información acerca de la actualización de la memoria caché de contactos, [vea Sincronizar amigos y actividades.](synchronizing-friends-and-activities.md) 
  
1. [ISocialSession::LoggedOnUserID:](isocialsession-loggedonuserid.md) el OSC obtiene el identificador de usuario del usuario de Office que ha iniciado sesión en la red social. 
    
2. [ISocialSession::GetPerson:](isocialsession-getperson.md) mediante el identificador de usuario del usuario de Office, el OSC obtiene un objeto **ISocialPerson** para ese usuario. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — El OSC obtiene la lista de amigos del usuario en la red social. 
    
4. [ISocialSession::GetPerson—](isocialsession-getperson.md) Para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC obtiene una interfaz **ISocialPerson.** 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — Para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC obtiene un recurso de imagen.
    
## <a name="see-also"></a>Consulte también

- [XML para funcionalidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

