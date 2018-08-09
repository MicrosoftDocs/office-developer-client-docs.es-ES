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
# <a name="basic-authentication"></a>Autenticación básica

Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. El OSC usa las capacidades devueltas para determinar cómo se admite un usuario de Office que está iniciando sesión en esta red social. Si el elemento **useLogonWebAuth** en devuelto **capacidades** XML indica que el proveedor de OSC admite la autenticación básica, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) : el OSC carga el proveedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) : el OSC Obtiene una cadena que representa el número de versión del proveedor de OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) : el OSC Obtiene una cadena que representa el nombre de redes sociales. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) : el OSC Obtiene un GUID inmutable que representa la red social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) : el OSC Obtiene una cadena que representa las funciones del proveedor y que cumple con la definición del esquema para el elemento **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) : el OSC Obtiene una matriz de bytes que representa el icono para el sitio de red social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) : el OSC Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::Logon](isocialsession-logon.md) : el OSC inicia la sesión de usuario en el sitio de red social mediante el nombre de usuario especificado y la contraseña. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : el OSC Obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado la sesión. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) : el OSC Obtiene una cadena que representa un identificador único para un sitio de red social. El identificador de la red puede ser equivalente al nombre de red. 
    
## <a name="see-also"></a>Vea también

- [XML de capacidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

