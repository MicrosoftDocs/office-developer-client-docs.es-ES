---
title: Obtener actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: El OSC llama al método de ISocialProvider::GetCapabilities para determinar las capacidades del proveedor de OSC para una red social.
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821086"
---
# <a name="getting-activities"></a>Obtener actividades

El OSC llama al método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor de OSC para una red social. Si los elementos **getActivities** y **dynamicActivitiesLookupEx** en el devuelto XML de las **capacidades de** indican que el proveedor OSC admite las actividades de introducción a petición y almacenar las actividades en la memoria, el OSC puede hacer lo siguiente secuencia de llamada. El OSC también la función de hash especificada en el elemento **hashFunction** en el XML de las **capacidades de** las notas. El OSC llama a métodos en la siguiente secuencia para obtener información y actividades (como compatible con la interfaz de [ISocialPerson](isocialpersoniunknown.md) ) de amigos y amigos de la red social: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : al final del proceso de autenticación, el OSC llama a **GetLoggedOnUser** para obtener una interfaz de [ISocialProfile](isocialprofileisocialperson.md) para el usuario autenticado. Para obtener más información acerca de la autenticación, vea [Autenticación básica](basic-authentication.md) y [la autenticación basada en formularios](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) : para las personas que se muestra en el panel de personas de Outlook, se obtiene el OSC y devuelven los valores hash de su SMTP resuelve, llama a **ISocialSession2::GetActivitiesEx**y almacena (en memoria) de los datos de las actividades de Estas personas. Obtiene el OSC en un parámetro de salida, _las actividades_, que es una cadena que contiene una colección de actividades para amigos del usuario que ha iniciado la sesión. Esta cadena se ajusta a la definición del esquema para el elemento **activityFeed** . 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) : para cada elemento **activityDetails** en el XML devuelto por **GetActivitiesEx** **activityFeed** , hay un elemento **ownerID** que indica la persona que posee dicha actividad. El OSC utiliza ese valor **ownerID** para llamar a **GetPerson** para obtener una interfaz **ISocialPerson** de esa persona. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) : basado en el objeto de **ISocialPerson** que obtuvo en el paso 3, el OSC llama a **GetDetails** para obtener detalles de esa persona, como el nombre y el apellido. El OSC puede hacer lo mismo con cada actividad especificado en un elemento **activityDetails** **activityFeed** XML devuelto por **GetActivitiesEx** en el paso 2. 
    
> [!NOTE]
> El OSC actualiza la caché de actividades en un intervalo predeterminado. Para obtener más información acerca de cómo actualizar la memoria caché de las actividades, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Vea también

- [XML de capacidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

