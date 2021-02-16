---
title: Autenticación básica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) llama al método ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439929"
---
# <a name="basic-authentication"></a><span data-ttu-id="949b1-103">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="949b1-103">Basic authentication</span></span>

<span data-ttu-id="949b1-104">Outlook Social Connector (OSC) llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="949b1-105">El OSC usa las funcionalidades devueltas para determinar cómo admitir un usuario de Office que inicia sesión en esta red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="949b1-106">Si el elemento **useLogonWebAuth** en el **XML** de funcionalidades devueltas indica que el proveedor de OSC admite la autenticación básica, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social:</span><span class="sxs-lookup"><span data-stu-id="949b1-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="949b1-107">[ISocialProvider::Load:](isocialprovider-load.md) el OSC carga el proveedor.</span><span class="sxs-lookup"><span data-stu-id="949b1-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="949b1-108">[ISocialProvider::Version—](isocialprovider-version.md) El OSC obtiene una cadena que representa el número de versión del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="949b1-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="949b1-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — El OSC obtiene una cadena que representa el nombre de la red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="949b1-110">[ISocialProvider::SocialNetworkGuid—](isocialprovider-socialnetworkguid.md) El OSC obtiene un GUID inmutable que representa la red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="949b1-111">[ISocialProvider::GetCapabilities:](isocialprovider-getcapabilities.md) el OSC obtiene una cadena que representa las capacidades del proveedor y que cumple con la definición de esquema para el elemento **capabilities.**</span><span class="sxs-lookup"><span data-stu-id="949b1-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="949b1-112">[ISocialProvider::SocialNetworkIcon—](isocialprovider-socialnetworkicon.md) El OSC obtiene una matriz de bytes que representa el icono del sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="949b1-113">[ISocialProvider::GetSession:](isocialprovider-getsession.md) el OSC obtiene una [interfaz ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="949b1-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="949b1-114">[ISocialSession::Logon:](isocialsession-logon.md) el OSC inicia sesión en el sitio de la red social con el nombre de usuario y la contraseña especificados.</span><span class="sxs-lookup"><span data-stu-id="949b1-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="949b1-115">[ISocialSession::GetLoggedOnUser—](isocialsession-getloggedonuser.md) El OSC obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="949b1-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="949b1-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — El OSC obtiene una cadena que representa un identificador único para un sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="949b1-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="949b1-117">El identificador de red puede ser equivalente al nombre de red.</span><span class="sxs-lookup"><span data-stu-id="949b1-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="949b1-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="949b1-118">See also</span></span>

- [<span data-ttu-id="949b1-119">XML para funcionalidades</span><span class="sxs-lookup"><span data-stu-id="949b1-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="949b1-120">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="949b1-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

