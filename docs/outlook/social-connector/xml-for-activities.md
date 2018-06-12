---
title: XML de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Este tema contiene un escenario de ejemplo que muestra al proveedor de Outlook Social Connector (OSC) de las llamadas de API de extensibilidad que implementa un proveedor de OSC y hace que el OSC para obtener información sobre actividades. Información se expresa en las cadenas XML que se ajustan al esquema XML de proveedor OSC.
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821229"
---
# <a name="xml-for-activities"></a>XML de actividades

Este tema contiene un escenario de ejemplo que muestra al proveedor de Outlook Social Connector (OSC) de las llamadas de API de extensibilidad que implementa un proveedor de OSC y hace que el OSC para obtener información sobre actividades. Información se expresa en las cadenas XML que se ajustan al esquema XML de proveedor OSC.
  
El esquema XML de proveedor OSC permite que un proveedor de OSC definir las actividades. Información de actividad puede incluir la red social donde la actividad de fuente de los elementos de origen, detalles de cada elemento de la fuente de actividades (como propietario, escriba y fecha de publicación de la actividad) y la plantilla para mostrar la actividad. Para admitir actividades que muestra en el panel de personas o de la tarjeta de contacto, proveedor de OSC de una red social debe implementar y devolver las actividades correctas XML. Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md). Para obtener más información acerca de cómo sincronizar las actividades de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md). Para ver una definición completa del esquema XML de proveedor OSC, incluido qué elementos son obligatorios u opcionales, vea [Esquema de XML de Outlook Social Connector proveedor](outlook-social-connector-provider-xml-schema.md). 
  
En el siguiente escenario, el OSC dinámicamente sincroniza las actividades de una persona seleccionada en el panel de personas y obtiene los detalles sobre esa persona:
  
1. Un proveedor de OSC que admite la sincronización a petición de actividades indica el OSC mediante el uso de los elementos **getActivities** y **dynamicActivitiesLookupEx** . El proveedor de OSC también establece el elemento **hashFunction** . Los tres elementos son elementos secundarios de **las capacidades**. 
    
2. El proveedor OSC implementa los métodos **ISocialProvider::GetCapabilities** y [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. Las llamadas OSC **ISocialProvider::GetCapabilities** para comprobar el valor de **getActivities** y **dynamicActivitiesLookupEx** para comprobar el proveedor de OSC admite la sincronización de petición de actividades. El OSC notas también el valor del elemento **hashFunction** admitido por el proveedor OSC. 
    
4. El OSC actualiza la tarjeta de contacto o el panel de personas para permitir que el usuario vea las actividades más recientes de la persona seleccionada. El OSC cifra la dirección SMTP de la persona mediante la función de hash especificada en el elemento **hashFunction** , que forman una cadena XML que se ajusta a la definición del esquema XML para el elemento **hashedAddresses** . 
    
5. El OSC llama a **ISocialSession2::GetActivitiesEx**, proporcionar esta cadena XML de la dirección del algoritmo hash como el parámetro _hashedAddresses_ , para obtener una colección actual de las actividades de esa persona en el parámetro de _actividades_ . La cadena de parámetro _actividades_ cumple con la definición del esquema XML del elemento **activityFeed** . 
    
6. En función de la definición del esquema XML para **activityFeed**, aún más el OSC analiza la cadena de _actividades_ para averiguar el tipo, fecha y otra información acerca de cada actividad y cómo mostrar la actividad de publicación. 
    
7. Para obtener detalles acerca de la persona seleccionada, el OSC llama a [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), que proporciona la misma cadena XML de direcciones con algoritmo hash como el argumento para el parámetro _personsAddresses_ . Los detalles acerca de la persona se devuelven en el parámetro _personsCollection_ . Pueden incluir estos detalles **emailAddress**, **firstName**y **LastName (apellidos)**. El parámetro _personsCollection_ se ajusta a la definición del esquema XML para el elemento de la **persona** . 
    
Puede encontrar más información acerca de cómo especificar XML para las actividades de los siguientes temas de esta sección:
  
- [Elemento de la fuente de información general de XML de una actividad](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
- [Instrucciones para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Ver también

- [Ejemplo de XML de fuentes de actividades](activity-feed-xml-example.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [XML de capacidades](xml-for-capabilities.md)  
- [XML de amigos](xml-for-friends.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

