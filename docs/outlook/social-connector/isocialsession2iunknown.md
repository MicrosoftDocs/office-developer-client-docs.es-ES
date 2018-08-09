---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Admite la adición de amigos, sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821130"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Admite la adición de amigos, sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.
  
## <a name="members"></a>Members

La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialSession2** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Método  <br/> |Agrega a la persona identificada por los parámetros _emailAddresses_ y _displayName_ como amigo para el usuario ha iniciado sesión en la red social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Método  <br/> |Obtiene una cadena que representa una colección de las actividades de los usuarios especificados por el parámetro _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Método  <br/> |Devuelve una cadena que contiene una colección de detalles de imagen y la persona para los usuarios especificados por el parámetro _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Método  <br/> |Inicie sesión en el sitio de red social mediante credenciales almacenadas en caché.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede elegir un proveedor de Outlook Social Connector (OSC) implementar esta interfaz si el proveedor admite la sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché. Si el proveedor de OSC implementa **ISocialSession2** y admite las siguientes a personas en la red social, el OSC llamaría a [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md), y el proveedor debe implementar **ISocialSession2::FollowPersonEx**, así como.
  
## <a name="see-also"></a>Vea también

- [Interfaces del proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

