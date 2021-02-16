---
title: Información general sobre XML de un elemento de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Una fuente de actividades consta de una o más actividades que se producen en una red social. Cada fuente de actividad está representada por un elemento activityFeed y se caracteriza por estos tres fragmentos de información:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439950"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Información general sobre XML de un elemento de fuente de actividades

Una fuente de actividades consta de una o más actividades que se producen en una red social. Cada fuente de actividad está representada por un **elemento activityFeed** y se caracteriza por estos tres fragmentos de información: 
  
- **network:** nombre de la red social desde la que se originaron las actividades.
    
- **actividades:** contenedor de actividades que se están produciendo en la cuenta del usuario que ha iniciado sesión en esa red social.
    
- **templates:** contenedor de plantillas que se usan para mostrar el elemento de actividad correspondiente en **las actividades.**
    
Para crear un elemento de fuente de actividades, debe cumplir con el esquema XML de extensibilidad del proveedor de Outlook Social Connector (OSC). La figura 1 muestra la estructura XML de fuente de actividades.
  
**Figura 1. Estructura XML de fuente de actividades**

![Estructura XML de la actividad](media/odc_ol14_ta_OSC_Fig06.gif)
  
Para cada elemento de fuente de actividades, las dos partes más importantes de este esquema son los **elementos activityDetails** y **activityTemplateContainer:** 
  
- El **elemento activityDetails** almacena información específica para cada elemento de fuente de actividades, como el nombre del propietario de la actividad o la dirección URL de las imágenes cargadas. 
    
- El **elemento activityTemplateContainer** almacena el formato o el diseño de cada elemento de fuente de actividades. Consta de plantillas, representadas por elementos **activityTemplate** individuales, que se pueden reutilizar para varios elementos de fuente. 
    
Para un elemento de fuente de actividades individual, el **elemento activityTemplate** especifica los siguientes cuatro fragmentos de información: 
  
- **:** especifica la dirección URL del icono para mostrar el elemento de fuente de actividades.
    
- **title:** describe el elemento de fuente de actividades.
    
- **type:** especifica el tipo de actividad, como un estado, una foto o una actualización de documento.
    
- **data:** especifica cualquier información adicional que se muestre con el elemento de fuente de actividades.
    
> [!TIP]
> El icono que se muestra en la fuente de actividades siempre es el mismo que el icono de proveedor devuelto por la propiedad **ISocialProvider::SocialNetworkIcon.** 
  
Consulta los siguientes temas para obtener más información sobre el **elemento activityDetails,** el elemento **activityTemplateContainer,** los tokens de plantilla y las variables de plantilla: 
  
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
- [Directrices para mostrar actividades correctamente](guidelines-for-properly-displaying-activities.md)
    
Para obtener un ejemplo de XML de fuente de actividades, vea [el ejemplo XML de fuente de actividades](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Consulte también

- [XML para actividades](xml-for-activities.md) 
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

