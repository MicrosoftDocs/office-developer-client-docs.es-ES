---
title: Obtener actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: 'El OSC llama al método ISocialProvider:: GetCapabilities para determinar las capacidades del proveedor OSC para una red social.'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327191"
---
# <a name="getting-activities"></a>Obtener actividades

El OSC llama al método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar las capacidades del proveedor OSC para una red social. Si los elementos **getActivities** y **dynamicActivitiesLookupEx** del XML de **funcionalidades** devueltas indican que el proveedor de OSC admite la obtención de actividades a petición y el almacenamiento de actividades en la memoria, el OSC puede hacer lo siguiente: secuencia de llamada. El OSC también anota la función hash especificada en el elemento **hashFunction** en el XML de **capacidades** . El OSC llama a los métodos de la siguiente secuencia para obtener actividades e información (como la admitida por la interfaz [ISocialPerson](isocialpersoniunknown.md) ) para amigos y no amigos en la red social: 
  
1. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) : al final del proceso de autenticación, OSC llama a **GetLoggedOnUser** para obtener una interfaz de [ISocialProfile](isocialprofileisocialperson.md) del usuario que se va a autenticar. Para obtener más información acerca de la autenticación, consulte [autenticación básica](basic-authentication.md) y [autenticación basada en formularios](forms-based-authentication.md).
    
2. [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) : para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica un algoritmo hash a sus direcciones SMTP, llama a **ISocialSession2:: GetActivitiesEx**y almacena (en la memoria) los datos de actividades devueltos para estas personas. OSC se obtiene en un parámetro de salida __, Activities, que es una cadena que contiene una colección de actividades para amigos del usuario que ha iniciado sesión. Esta cadena se ajusta a la definición de esquema del elemento **activityFeed** . 
    
3. [ISocialSession:: GetPerson](isocialsession-getperson.md) : para cada elemento **activityDetails** en el XML de **activityFeed** devuelto por **GetActivitiesEx**, hay un elemento **ownerID** que indica la persona que posee dicha actividad. El OSC usa ese valor de **ownerID** para llamar a **GetPerson** para obtener una interfaz **ISocialPerson** para esa persona. 
    
4. [ISocialPerson:: GetDetails](isocialperson-getdetails.md) : basado en el objeto **ISocialPerson** que se obtuvo en el paso 3, el OSC llama a **GetDetails** para obtener detalles de esa persona, como el nombre y el apellido. El OSC puede hacer lo mismo para cada actividad especificada en un elemento **activityDetails** del XML **activityFeed** devuelto por **GetActivitiesEx** en el paso 2. 
    
> [!NOTE]
> El OSC actualiza la memoria caché de actividades en un intervalo predeterminado. Para obtener más información acerca de la actualización de la caché de actividades, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)

