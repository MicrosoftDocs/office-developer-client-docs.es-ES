---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Representa una instancia de un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821233"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Representa una instancia de un proveedor de Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialProvider** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Propiedad  <br/> |Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Método  <br/> |Obtiene una cadena que describe las capacidades del proveedor.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Método  <br/> |Este método no se admite actualmente.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Método  <br/> |Inicializa el proveedor de OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Propiedad  <br/> |Devuelve un GUID que representa un identificador único para la red social.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Propiedad  <br/> |Devuelve una matriz de bytes que representa el icono para la red social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Propiedad  <br/> |Devuelve un valor de tipo string que representa el nombre de redes sociales.  <br/> |
|[Versión](isocialprovider-version.md) <br/> |Propiedad  <br/> |Devuelve un valor de tipo string que representa el número de versión del proveedor para esta red social.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un proveedor de OSC debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Vea también

- [Interfaces del proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

