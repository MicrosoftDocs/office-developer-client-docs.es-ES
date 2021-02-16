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
# <a name="basic-authentication"></a>Autenticación básica

Outlook Social Connector (OSC) llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. El OSC usa las funcionalidades devueltas para determinar cómo admitir un usuario de Office que inicia sesión en esta red social. Si el elemento **useLogonWebAuth** en el **XML** de funcionalidades devueltas indica que el proveedor de OSC admite la autenticación básica, el OSC puede realizar la siguiente secuencia de llamada para permitir que un usuario inicie sesión en esa red social: 
  
1. [ISocialProvider::Load:](isocialprovider-load.md) el OSC carga el proveedor. 
    
2. [ISocialProvider::Version—](isocialprovider-version.md) El OSC obtiene una cadena que representa el número de versión del proveedor de OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — El OSC obtiene una cadena que representa el nombre de la red social. 
    
4. [ISocialProvider::SocialNetworkGuid—](isocialprovider-socialnetworkguid.md) El OSC obtiene un GUID inmutable que representa la red social. 
    
5. [ISocialProvider::GetCapabilities:](isocialprovider-getcapabilities.md) el OSC obtiene una cadena que representa las capacidades del proveedor y que cumple con la definición de esquema para el elemento **capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon—](isocialprovider-socialnetworkicon.md) El OSC obtiene una matriz de bytes que representa el icono del sitio de red social. 
    
7. [ISocialProvider::GetSession:](isocialprovider-getsession.md) el OSC obtiene una [interfaz ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::Logon:](isocialsession-logon.md) el OSC inicia sesión en el sitio de la red social con el nombre de usuario y la contraseña especificados. 
    
9. [ISocialSession::GetLoggedOnUser—](isocialsession-getloggedonuser.md) El OSC obtiene una interfaz [ISocialProfile](isocialprovideriunknown.md) que representa al usuario que ha iniciado sesión. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — El OSC obtiene una cadena que representa un identificador único para un sitio de red social. El identificador de red puede ser equivalente al nombre de red. 
    
## <a name="see-also"></a>Consulte también

- [XML para funcionalidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

