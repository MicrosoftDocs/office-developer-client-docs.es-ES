---
title: Autenticación basada en formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook Social Connector (OSC) llama al método de ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821097"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="902b2-103">Autenticación basada en formularios</span><span class="sxs-lookup"><span data-stu-id="902b2-103">Forms-based authentication</span></span>

<span data-ttu-id="902b2-104">Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="902b2-105">El OSC usa las capacidades devueltas para determinar cómo se admite un usuario de Office que está iniciando sesión en esta red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="902b2-106">Si el elemento **useLogonWebAuth** en devuelto **capacidades** XML indica que el proveedor de OSC admite la autenticación basada en formularios, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social:</span><span class="sxs-lookup"><span data-stu-id="902b2-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="902b2-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC la carga el proveedor.</span><span class="sxs-lookup"><span data-stu-id="902b2-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="902b2-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; El OSC Obtiene una cadena que representa el número de versión del proveedor para esta red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="902b2-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; El OSC Obtiene una cadena que representa el nombre de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="902b2-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="902b2-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; El OSC Obtiene un GUID inmutable que representa la red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="902b2-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; El OSC Obtiene una cadena que representa las funciones del proveedor y que cumple con la definición del esquema para el elemento **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="902b2-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="902b2-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; El OSC Obtiene una matriz de bytes que representa el icono para el sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="902b2-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; El OSC Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="902b2-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="902b2-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC inicializa inicie sesión en el sitio de red social mediante la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="902b2-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="902b2-115">Para esta llamada inicial de inicio de sesión, el OSC pasa **null** para el parámetro de _configuración_ .</span><span class="sxs-lookup"><span data-stu-id="902b2-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="902b2-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; El OSC Obtiene la dirección URL para mostrar un formulario basado en explorador al usuario durante la autenticación web.</span><span class="sxs-lookup"><span data-stu-id="902b2-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="902b2-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC finaliza el inicio de sesión para el sitio de red social mediante la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="902b2-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="902b2-118">El OSC llama a este método una segunda vez, pasando la dirección URL del formulario de inicio de sesión para el proveedor en el parámetro de _configuración_ .</span><span class="sxs-lookup"><span data-stu-id="902b2-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="902b2-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; El OSC Obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="902b2-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="902b2-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; El OSC Obtiene una cadena que representa un identificador único para un sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="902b2-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="902b2-121">El identificador de la red puede ser equivalente al nombre de red.</span><span class="sxs-lookup"><span data-stu-id="902b2-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="902b2-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="902b2-122">See also</span></span>

- [<span data-ttu-id="902b2-123">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="902b2-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="902b2-124">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="902b2-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

