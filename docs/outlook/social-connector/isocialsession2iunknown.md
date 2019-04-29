---
title: IUnknown ISocialSession2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Admite la adición de amigos, a petición o la sincronización híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408834"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Admite la adición de amigos, a petición o la sincronización híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.
  
## <a name="members"></a>Members

En la siguiente tabla se muestran los miembros que están disponibles en la interfaz **ISocialSession2** . 
  
|**Nombre**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Método  <br/> |Agrega la persona identificada por los parámetros _emailAddresses_ y _displayName_ como un amigo para el usuario que ha iniciado sesión en la red social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Método  <br/> |Obtiene una cadena que representa una colección de actividades de los usuarios especificados por el parámetro _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Método  <br/> |Devuelve una cadena que contiene una colección de personas y detalles de la imagen para los usuarios especificados por el parámetro _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Método  <br/> |Inicia sesión en el sitio de red social con las credenciales almacenadas en caché.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un proveedor de Outlook Social Connector (OSC) puede optar por implementar esta interfaz si el proveedor admite la sincronización a petición o híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social con las credenciales almacenadas en la memoria caché. Si el proveedor de OSC implementa **ISocialSession2** y admite seguimiento de personas en la red social, OSC llamaría a [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) en lugar de [ISocialSession:: FollowPerson](isocialsession-followperson.md)y el proveedor debe implementar **ISocialSession2:: FollowPersonEx**también.
  
## <a name="see-also"></a>Ver también

- [Interfaces de proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

