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
# <a name="getting-friends-information"></a><span data-ttu-id="e89af-103">Obtención de información de amigos</span><span class="sxs-lookup"><span data-stu-id="e89af-103">Getting friends information</span></span>

<span data-ttu-id="e89af-104">Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social.</span><span class="sxs-lookup"><span data-stu-id="e89af-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="e89af-105">Si los elementos **getFriends** y **cacheFriends** en el devuelto XML de las **capacidades de** indican que el proveedor de OSC admite a Introducción amigos y amigos de almacenamiento en caché como Outlook, póngase en contacto con los elementos en una carpeta de contactos correspondiente, puede hacer que el OSC la siguiente secuencia de llamada.</span><span class="sxs-lookup"><span data-stu-id="e89af-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="e89af-106">El OSC llama a métodos en esta secuencia para obtener información y las imágenes (como compatible con la interfaz de [ISocialPerson](isocialpersoniunknown.md) ) para amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="e89af-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e89af-107">El OSC actualiza la memoria caché en un intervalo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e89af-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="e89af-108">Si se produce un error durante la memoria caché de actualizar, los reintentos OSC en otro intervalo preestablecido, que también se pueden controlar mediante la especificación del elemento **contactSyncRestartInterval** en el XML de las **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="e89af-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="e89af-109">Para obtener más información acerca de cómo actualizar la memoria caché de los contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="e89af-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="e89af-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) : el OSC Obtiene el identificador de usuario del usuario de Office que ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="e89af-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="e89af-111">[ISocialSession::GetPerson](isocialsession-getperson.md) — con el identificador de usuario del usuario de Office, el OSC Obtiene un objeto **ISocialPerson** para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="e89af-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="e89af-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) : el OSC Obtiene la lista del usuario amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="e89af-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="e89af-113">[ISocialSession::GetPerson](isocialsession-getperson.md) : para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC Obtiene una interfaz **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="e89af-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="e89af-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) : para cada persona en el XML devuelto por **GetFriendsAndColleagues**, el OSC Obtiene un recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="e89af-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e89af-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="e89af-115">See also</span></span>

- [<span data-ttu-id="e89af-116">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="e89af-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="e89af-117">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="e89af-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

