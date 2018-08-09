---
title: Información general sobre XML de un elemento de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Una fuente de actividades consta de una o más actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento activityFeed y se caracteriza por estos tres fragmentos de información:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821226"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Información general sobre XML de un elemento de fuente de actividades

Una fuente de actividades consta de una o más actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento **activityFeed** y se caracteriza por estos tres fragmentos de información: 
  
- **red**: nombre de la red social desde el que se originaron las actividades.
    
- **actividades**: contenedor de actividades que ocurren en la cuenta del usuario ha iniciado la sesión de esa red social.
    
- **plantillas**: contenedor de plantillas que se usan para mostrar el elemento correspondiente de la actividad en **las actividades**.
    
Para crear un elemento de fuente de actividades, debe cumplir el esquema XML de extensibilidad de proveedor de Outlook Social Connector (OSC). La figura 1 muestra la que estructura XML de la fuente de la actividad.
  
**En la figura 1. Estructura XML de la fuente de actividades**

![Estructura XML de la actividad](media/odc_ol14_ta_OSC_Fig06.gif)
  
Para cada elemento de fuente de actividades, las dos partes más importantes de este esquema son los elementos **activityDetails** y **activityTemplateContainer** : 
  
- El elemento **activityDetails** almacena información específica para cada elemento, como el nombre del propietario de la actividad o la dirección URL de las imágenes que se cargan de fuente de actividades. 
    
- El elemento **activityTemplateContainer** almacena el formato o elemento de la fuente de diseño para cada actividad. Se compone de plantillas, representadas por elementos individuales **activityTemplate** , que se pueden reutilizar para varios elementos de la fuente. 
    
Para un elemento de fuente de actividades de individuales, el elemento **activityTemplate** especifica las cuatro piezas de la información siguientes: 
  
- **icono**— especifica el elemento de fuente de la dirección URL del icono para mostrar la actividad.
    
- **título**: describe la actividad fuente item.
    
- **tipo**: especifica el tipo de actividad, como un estado, fotografía o actualización de documentos.
    
- **datos**— especifica cualquier información adicional que se muestra con el elemento de fuente de actividades.
    
> [!TIP]
> El icono que se muestra en la fuente de actividades siempre es el mismo que el icono de proveedor devuelto por la propiedad **ISocialProvider::SocialNetworkIcon** . 
  
Consulte los siguientes temas para obtener más información sobre el elemento **activityDetails** , el elemento **activityTemplateContainer** , los tokens de plantilla y variables de plantilla: 
  
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
- [Instrucciones para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)
    
Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Vea también

- [XML de actividades](xml-for-activities.md) 
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

