---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Representa una conexión a un sitio de red social.
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821135"
---
# <a name="isocialsession--iunknown"></a>ISocialSession: IUnknown

Representa una conexión a un sitio de red social.
  
## <a name="members"></a>Miembros

La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialSession** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Método  <br/> |Obtiene un valor de tipo string que representa a una o más personas que coinciden con el parámetro _userID_ .  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Método  <br/> |Agrega a la persona identificada por el parámetro _emailAddress_ como amigo para el usuario ha iniciado sesión en la red social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Método  <br/> |Este método ha quedado obsoleto en Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialProfile](isocialprofileisocialperson.md) que representa al usuario que ha iniciado la sesión.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Método  <br/> |Obtiene un valor de tipo string que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Método  <br/> |Obtiene una cadena que representa un identificador único de redes sociales para una conexión de red social determinado.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Método  <br/> |Obtiene una interfaz [ISocialPerson](isocialpersoniunknown.md) basándose en el parámetro _userID_ .  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Property  <br/> |Devuelve un valor de tipo string que representa el identificador de usuario de red social del usuario que ha iniciado sesión actualmente.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Property  <br/> |Devuelve un valor de tipo string que representa el nombre de usuario que se usa al inicio de sesión.  <br/> |
|[Inicio de sesión](isocialsession-logon.md) <br/> |Método  <br/> |Inicie sesión en el sitio de red social utilizando el nombre de usuario especificado y la contraseña.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Método  <br/> |Inicie sesión en el sitio de red social mediante la autenticación basada en formularios.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Property  <br/> |Establece la dirección URL de sitio de red social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Método  <br/> |Quita a la persona identificada por el parámetro _userID_ como amigo en la red social.  <br/> |
   
## <a name="remarks"></a>Notas

Un proveedor de OSC debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Ver también

- [Interfaces del proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

