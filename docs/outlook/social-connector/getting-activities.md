---
title: Obtener actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: El OSC llama al método ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420580"
---
# <a name="getting-activities"></a>Obtener actividades

El OSC llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. Si los elementos **getActivities** y **dynamicActivitiesLookupEx** del **XML** de funcionalidades devueltas indican que el proveedor de OSC admite obtener actividades a petición y almacenar actividades en la memoria, el OSC puede realizar la siguiente secuencia de llamadas. El OSC también toma nota de la función hash especificada en el **elemento hashFunction** en el XML **de funcionalidades.** El OSC llama a métodos en la siguiente secuencia para obtener actividades e información (como admite la interfaz [ISocialPerson)](isocialpersoniunknown.md) para amigos y no amigos en la red social: 
  
1. [ISocialSession::GetLoggedOnUser:](isocialsession-getloggedonuser.md) al final del proceso de autenticación, el OSC llama a **GetLoggedOnUser para** obtener una interfaz [ISocialProfile](isocialprofileisocialperson.md) para el usuario autenticado. Para obtener más información sobre la autenticación, [vea Basic Authentication](basic-authentication.md) and [Forms-Based Authentication](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx:](isocialsession2-getactivitiesex.md) para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica hash a sus direcciones SMTP, llama a **ISocialSession2::GetActivitiesEx** y almacena (en la memoria) los datos de actividades devueltos para estas personas. El OSC obtiene un parámetro de salida,  _activities_, que es una cadena que contiene una colección de actividades para los amigos del usuario que ha iniciado sesión. Esta cadena se ajusta a la definición de esquema del **elemento activityFeed.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) : para cada elemento **activityDetails** del xml **activityFeed** devuelto por **GetActivitiesEx**, hay un elemento **ownerID** que indica la persona propietaria de esa actividad. El OSC usa ese **valor ownerID** para llamar a **GetPerson** para obtener una **interfaz ISocialPerson** para esa persona. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) : en función del objeto **ISocialPerson** obtenido del paso 3, el OSC llama a **GetDetails** para obtener detalles de esa persona, como el nombre y el apellido. El OSC puede hacer lo mismo para cada actividad especificada en un **elemento activityDetails** en el **xml activityFeed** devuelto por **GetActivitiesEx** en el paso 2. 
    
> [!NOTE]
> El OSC actualiza la memoria caché de actividades en un intervalo predeterminado. Para obtener más información sobre cómo actualizar la memoria caché de actividades, vea [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)
- [Secuencias de llamadas típicas de OSC](osc-typical-calling-sequences.md)

