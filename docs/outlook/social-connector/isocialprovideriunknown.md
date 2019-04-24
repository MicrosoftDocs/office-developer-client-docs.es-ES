---
title: IUnknown ISocialProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Representa una instancia de un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285487"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Representa una instancia de un proveedor de Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

En la siguiente tabla se muestran los miembros que están disponibles en la interfaz **ISocialProvider** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Propiedad  <br/> |Devuelve una matriz de cadenas que especifican las direcciones URL del sitio para el proveedor de OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Método  <br/> |Obtiene una cadena que describe las funciones del proveedor.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Método  <br/> |Actualmente, este método no es compatible.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Método  <br/> |Inicializa el proveedor de OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Propiedad  <br/> |Devuelve un GUID que representa un identificador único para la red social.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Propiedad  <br/> |Devuelve una matriz de bytes que representa el icono de la red social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Propiedad  <br/> |Devuelve una cadena que representa el nombre de la red social.  <br/> |
|[Versión](isocialprovider-version.md) <br/> |Propiedad  <br/> |Devuelve una cadena que representa el número de versión del proveedor de esta red social.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un proveedor OSC debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Vea también

- [Interfaces de proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

