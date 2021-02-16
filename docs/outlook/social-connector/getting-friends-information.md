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
# <a name="getting-friends-information"></a><span data-ttu-id="a8fd8-103">Obtener información de amigos</span><span class="sxs-lookup"><span data-stu-id="a8fd8-103">Getting friends information</span></span>

<span data-ttu-id="a8fd8-104">Outlook Social Connector (OSC) llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="a8fd8-105">Si los elementos **getFriends** y **cacheFriends** en el **XML** de funcionalidades devueltas indican que el proveedor de OSC admite la obtención de amigos y el almacenamiento en caché de amigos como elementos de contacto de Outlook en una carpeta de contactos correspondiente, el OSC puede realizar la siguiente secuencia de llamada.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="a8fd8-106">El OSC llama a métodos en esta secuencia para obtener información e imágenes (como admite la interfaz [ISocialPerson)](isocialpersoniunknown.md) para amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a8fd8-107">El OSC actualiza la memoria caché en un intervalo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="a8fd8-108">Si se produce un error durante la actualización de la memoria caché, el OSC vuelve a iniciarse en otro intervalo preestablecido, que también se puede controlar especificando el elemento **contactSyncRestartInterval** en el XML de **funcionalidades.**</span><span class="sxs-lookup"><span data-stu-id="a8fd8-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="a8fd8-109">Para obtener más información acerca de la actualización de la memoria caché de contactos, [vea Sincronizar amigos y actividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="a8fd8-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="a8fd8-110">[ISocialSession::LoggedOnUserID:](isocialsession-loggedonuserid.md) el OSC obtiene el identificador de usuario del usuario de Office que ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="a8fd8-111">[ISocialSession::GetPerson:](isocialsession-getperson.md) mediante el identificador de usuario del usuario de Office, el OSC obtiene un objeto **ISocialPerson** para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="a8fd8-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — El OSC obtiene la lista de amigos del usuario en la red social.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="a8fd8-113">[ISocialSession::GetPerson—](isocialsession-getperson.md) Para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC obtiene una interfaz **ISocialPerson.**</span><span class="sxs-lookup"><span data-stu-id="a8fd8-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="a8fd8-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) — Para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC obtiene un recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="a8fd8-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8fd8-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8fd8-115">See also</span></span>

- [<span data-ttu-id="a8fd8-116">XML para funcionalidades</span><span class="sxs-lookup"><span data-stu-id="a8fd8-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="a8fd8-117">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="a8fd8-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

