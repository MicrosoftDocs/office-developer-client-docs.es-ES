---
title: Información general sobre XML de un elemento de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Una fuente de actividades consta de una o varias actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento activityFeed y se caracteriza por estos tres datos de información:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329298"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Información general sobre XML de un elemento de fuente de actividades

Una fuente de actividades consta de una o varias actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento **activityFeed** y se caracteriza por estos tres datos de información: 
  
- **red**: nombre de la red social desde la que se originaron las actividades.
    
- **actividades**: contenedor para actividades que ocurren en la cuenta del usuario que ha iniciado sesión en esa red social.
    
- **plantillas**: contenedor para plantillas que se usan para mostrar el elemento de actividad correspondiente en **actividades**.
    
Para crear un elemento de fuente de actividad, debe cumplir con el esquema XML de extensibilidad del proveedor de Outlook Social Connector (OSC). En la figura 1 se muestra la estructura XML de la fuente de actividades.
  
**Figura 1. Estructura XML de la fuente de actividades**

![Estructura XML de la actividad](media/odc_ol14_ta_OSC_Fig06.gif)
  
Para cada elemento de la fuente de actividades, las dos partes más importantes de este esquema son los elementos **activityDetails** y **activityTemplateContainer** : 
  
- El elemento **activityDetails** almacena información específica para cada elemento de la fuente de actividades, como el nombre del propietario de la actividad o la dirección URL de las imágenes que se cargan. 
    
- El elemento **activityTemplateContainer** almacena el formato o el diseño de cada elemento de la fuente de actividades. Consta de plantillas, representadas por elementos **activityTemplate** individuales, que se pueden volver a usar para varios elementos de fuente. 
    
Para un elemento de fuente de actividad individual, el elemento **activityTemplate** especifica los cuatro datos siguientes: 
  
- **icono**: especifica la dirección URL del icono para mostrar el elemento de fuente de actividad.
    
- **title**: describe el elemento fuente de actividades.
    
- **tipo**: especifica el tipo de actividad (por ejemplo, una actualización de estado, foto o documento).
    
- **datos**: especifica la información adicional que se muestra con el elemento de la fuente de actividades.
    
> [!TIP]
> El icono que se muestra en la fuente de actividades es siempre el mismo que el icono del proveedor devuelto por la propiedad **ISocialProvider:: SocialNetworkIcon** . 
  
Vea los temas siguientes para obtener más información sobre el elemento **activityDetails** , el elemento **activityTemplateContainer** , los tokens de plantilla y las variables de plantilla: 
  
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
- [Directrices para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)
    
Para obtener un ejemplo de XML de fuente de actividades, consulte ejemplo de XML de la [fuente de actividades](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Vea también

- [XML para actividades](xml-for-activities.md) 
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

