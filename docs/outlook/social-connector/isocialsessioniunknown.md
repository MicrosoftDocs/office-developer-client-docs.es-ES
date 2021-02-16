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
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437829"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Representa una conexión a un sitio de red social.
  
## <a name="members"></a>Miembros

En la tabla siguiente se muestran los miembros que están disponibles en la **interfaz ISocialSession.** 
  
|**Nombre**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Method  <br/> |Obtiene una cadena que representa una o varias personas que coinciden con el _parámetro userID._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Method  <br/> |Agrega la persona identificada por el parámetro  _emailAddress_ como un amigo del usuario que ha iniciado sesión en la red social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Method  <br/> |Este método ha quedado obsoleto en Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Method  <br/> |Obtiene una [interfaz ISocialProfile](isocialprofileisocialperson.md) que representa al usuario que ha iniciado sesión.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Method  <br/> |Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Method  <br/> |Obtiene una cadena que representa un identificador de red social único para una conexión de red social determinada.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Method  <br/> |Obtiene una [interfaz ISocialPerson](isocialpersoniunknown.md) basada en el _parámetro userID._  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Propiedad  <br/> |Devuelve una cadena que representa el identificador de usuario de la red social del usuario que ha iniciado sesión.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Propiedad  <br/> |Devuelve una cadena que representa el nombre de usuario que se usa al iniciar sesión.  <br/> |
|[Inicio de sesión](isocialsession-logon.md) <br/> |Method  <br/> |Inicia sesión en el sitio de la red social con el nombre de usuario y la contraseña especificados.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Method  <br/> |Inicia sesión en el sitio de la red social mediante la autenticación basada en formularios.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Propiedad  <br/> |Establece la dirección URL del sitio de red social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Method  <br/> |Quita la persona identificada por el parámetro  _userID_ como un amigo en la red social.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un proveedor de OSC debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Consulte también

- [Interfaces de proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

