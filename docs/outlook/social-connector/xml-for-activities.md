---
title: XML de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Este tema contiene un escenario de ejemplo que muestra las llamadas a la API de extensibilidad de proveedores de Outlook Social Connector (OSC) que implementa un proveedor de OSC y el OSC realiza para obtener información de actividades. La información se expresa en cadenas XML que se ajustan al esquema XML del proveedor OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409632"
---
# <a name="xml-for-activities"></a>XML de actividades

Este tema contiene un escenario de ejemplo que muestra las llamadas a la API de extensibilidad de proveedores de Outlook Social Connector (OSC) que implementa un proveedor de OSC y el OSC realiza para obtener información de actividades. La información se expresa en cadenas XML que se ajustan al esquema XML del proveedor OSC.
  
El esquema XML del proveedor OSC permite a un proveedor OSC definir actividades. La información de actividad puede incluir la red social en la que se originaron los elementos de la fuente de actividad, los detalles de cada elemento de la fuente de actividades (como el propietario, el tipo y la fecha de publicación de la actividad) y la plantilla para mostrar la actividad. Para admitir la visualización de actividades en el panel de personas o la tarjeta de contacto, el proveedor OSC de una red social debe implementar y devolver el XML de las actividades correctas. Para obtener un ejemplo de XML de fuente de actividades, consulte ejemplo de XML de la [fuente de actividades](activity-feed-xml-example.md). Para obtener más información acerca de la sincronización de las actividades de amigos, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). Para obtener una definición completa del esquema XML del proveedor de OSC, incluidos los elementos necesarios u opcionales, vea el [esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md). 
  
En el siguiente escenario, el OSC sincroniza dinámicamente las actividades de una persona seleccionada en el panel de personas y obtiene detalles sobre esa persona:
  
1. Un proveedor de OSC que admite la sincronización a petición de actividades indica el en el OSC mediante los elementos **getActivities** y **dynamicActivitiesLookupEx** . El proveedor OSC también establece el elemento **hashFunction** . Los tres elementos son elementos secundarios de **capacidades**. 
    
2. El proveedor OSC implementa los métodos **ISocialProvider:: GetCapabilities** y [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. El OSC llama a **ISocialProvider:: GetCapabilities** para comprobar el valor de **getActivities** y **dynamicActivitiesLookupEx** para comprobar que el proveedor OSC admite la sincronización a petición de las actividades. El OSC también anota el valor del elemento **hashFunction** compatible con el proveedor de OSC. 
    
4. El OSC actualiza el panel de personas o la tarjeta de contacto para permitir que el usuario vea las actividades más recientes de la persona seleccionada. El OSC cifra la dirección SMTP de la persona mediante la función hash especificada en el elemento **hashFunction** , formando una cadena XML que se ajusta a la definición del esquema XML para el elemento **hashedAddresses** . 
    
5. El OSC llama a **ISocialSession2:: GetActivitiesEx**y proporciona esta cadena XML de la dirección hash como el parámetro _hashedAddresses_ , para obtener una colección actual de actividades para esa persona en el parámetro _Activities_ . La __ cadena del parámetro Activities cumple con la definición del esquema XML del elemento **activityFeed** . 
    
6. En función de la definición del esquema XML para **activityFeed**, OSC analiza aún más la cadena de _actividades_ para averiguar el tipo, la fecha de publicación y otra información sobre cada actividad y cómo mostrar la actividad. 
    
7. Para obtener detalles sobre la persona seleccionada, OSC llama a [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)y proporciona la misma cadena XML de direcciones hash que el argumento para el parámetro _personsAddresses_ . Los detalles sobre la persona se devuelven en el parámetro _personsCollection_ . Estos detalles pueden incluir **FirstName**, **LastName**y **emailAddress**. El parámetro _personsCollection_ se ajusta a la definición del esquema XML para el elemento **Person** . 
    
Puede encontrar más información sobre cómo especificar XML para actividades en los siguientes temas de esta sección:
  
- [Información general sobre XML para un elemento de fuente de actividades](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
- [Directrices para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Ver también

- [Ejemplo de XML de fuente de actividades](activity-feed-xml-example.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [XML para funcionalidades](xml-for-capabilities.md)  
- [XML para amigos](xml-for-friends.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

