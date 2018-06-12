---
title: Autenticación básica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) llama al método de ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821109"
---
# <a name="basic-authentication"></a><span data-ttu-id="ee471-103">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="ee471-103">Basic authentication</span></span>

<span data-ttu-id="ee471-104">Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social.</span><span class="sxs-lookup"><span data-stu-id="ee471-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="ee471-105">El OSC usa las capacidades devueltas para determinar cómo se admite un usuario de Office que está iniciando sesión en esta red social.</span><span class="sxs-lookup"><span data-stu-id="ee471-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="ee471-106">Si el elemento **useLogonWebAuth** en devuelto **capacidades** XML indica que el proveedor de OSC admite la autenticación básica, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social:</span><span class="sxs-lookup"><span data-stu-id="ee471-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="ee471-107">[ISocialProvider::Load](isocialprovider-load.md) : el OSC carga el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ee471-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="ee471-108">[ISocialProvider::Version](isocialprovider-version.md) : el OSC Obtiene una cadena que representa el número de versión del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="ee471-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="ee471-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) : el OSC Obtiene una cadena que representa el nombre de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="ee471-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="ee471-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : el OSC Obtiene un GUID inmutable que representa la red social.</span><span class="sxs-lookup"><span data-stu-id="ee471-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="ee471-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) : el OSC Obtiene una cadena que representa las funciones del proveedor y que cumple con la definición del esquema para el elemento **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ee471-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="ee471-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) : el OSC Obtiene una matriz de bytes que representa el icono para el sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="ee471-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="ee471-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) : el OSC Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ee471-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="ee471-114">[ISocialSession::Logon](isocialsession-logon.md) : el OSC inicia la sesión de usuario en el sitio de red social mediante el nombre de usuario especificado y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="ee471-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="ee471-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : el OSC Obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="ee471-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="ee471-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) : el OSC Obtiene una cadena que representa un identificador único para un sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="ee471-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="ee471-117">El identificador de la red puede ser equivalente al nombre de red.</span><span class="sxs-lookup"><span data-stu-id="ee471-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ee471-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="ee471-118">See also</span></span>

- [<span data-ttu-id="ee471-119">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="ee471-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="ee471-120">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="ee471-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

