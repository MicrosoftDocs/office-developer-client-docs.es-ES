---
title: Autenticación basada en formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: El Outlook Social Connector (OSC) llama al método ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435533"
---
# <a name="forms-based-authentication"></a>Autenticación basada en formularios

El Outlook Social Connector (OSC) llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. El OSC usa las funcionalidades devueltas para determinar cómo admitir un usuario Office que inicia sesión en esta red social. 

Si el elemento **useLogonWebAuth** del **XML** de funcionalidades devueltas indica que el proveedor de OSC admite la autenticación basada en formularios, el OSC puede realizar la siguiente secuencia de llamadas para permitir que un usuario inicie sesión en esa red social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; El OSC carga el proveedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; El OSC obtiene una cadena que representa el número de versión del proveedor de esta red social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; El OSC obtiene una cadena que representa el nombre de la red social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; El OSC obtiene un GUID inmutable que representa la red social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; El OSC obtiene una cadena que representa las capacidades del proveedor y que cumple con la definición de esquema para el **elemento capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; El OSC obtiene una matriz de bytes que representa el icono del sitio de red social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; El OSC obtiene una [interfaz ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC inicializa el inicio de sesión en el sitio de red social mediante la autenticación basada en formularios. Para esta llamada de inicio de sesión inicial, el OSC pasa **null** para el _parámetro connectIn._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; El OSC obtiene la dirección URL para mostrar un formulario basado en explorador al usuario durante la autenticación web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; El OSC completa el inicio de sesión en el sitio de red social mediante la autenticación basada en formularios. El OSC llama a este método por segunda vez y pasa la dirección URL del formulario de inicio de sesión al proveedor en el _parámetro connectIn._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; El OSC obtiene una [interfaz ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado sesión. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; El OSC obtiene una cadena que representa un identificador único para un sitio de red social. El identificador de red puede ser equivalente al nombre de red. 
    
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)
- [Secuencias de llamadas típicas de OSC](osc-typical-calling-sequences.md)

