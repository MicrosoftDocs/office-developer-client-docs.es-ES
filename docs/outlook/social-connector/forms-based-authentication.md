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
# <a name="forms-based-authentication"></a>Autenticación basada en formularios

Outlook Social Connector (OSC) llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. El OSC usa las capacidades devueltas para determinar cómo se admite un usuario de Office que está iniciando sesión en esta red social. 

Si el elemento **useLogonWebAuth** en devuelto **capacidades** XML indica que el proveedor de OSC admite la autenticación basada en formularios, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC la carga el proveedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; El OSC Obtiene una cadena que representa el número de versión del proveedor para esta red social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; El OSC Obtiene una cadena que representa el nombre de redes sociales. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; El OSC Obtiene un GUID inmutable que representa la red social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; El OSC Obtiene una cadena que representa las funciones del proveedor y que cumple con la definición del esquema para el elemento **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; El OSC Obtiene una matriz de bytes que representa el icono para el sitio de red social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; El OSC Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC inicializa inicie sesión en el sitio de red social mediante la autenticación basada en formularios. Para esta llamada inicial de inicio de sesión, el OSC pasa **null** para el parámetro de _configuración_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; El OSC Obtiene la dirección URL para mostrar un formulario basado en explorador al usuario durante la autenticación web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC finaliza el inicio de sesión para el sitio de red social mediante la autenticación basada en formularios. El OSC llama a este método una segunda vez, pasando la dirección URL del formulario de inicio de sesión para el proveedor en el parámetro de _configuración_ . 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; El OSC Obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado la sesión. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; El OSC Obtiene una cadena que representa un identificador único para un sitio de red social. El identificador de la red puede ser equivalente al nombre de red. 
    
## <a name="see-also"></a>Vea también

- [XML de capacidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

