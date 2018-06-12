---
title: Desarrollar un proveedor con el esquema XML de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: El esquema XML de proveedor de Outlook Social Connector (OSC) define el formato de una gran cantidad de información que se pasa de una red social a través de proveedor OSC de la red para el OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821100"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Desarrollar un proveedor con el esquema XML de OSC

El esquema XML de proveedor de Outlook Social Connector (OSC) define el formato de una gran cantidad de información que se pasa de una red social a través de proveedor OSC de la red para el OSC. El esquema XML permite que un proveedor de OSC especificar las capacidades del proveedor, amigos y fuente de elementos de la red social, mediante el uso de los tres elementos principales, **capacidades**, **amigos**y **activityFeed**y sus secundarios de actividades elementos. El proveedor OSC implementa interfaces y sus métodos en la extensibilidad del proveedor OSC, devolver cadenas XML como parámetros de salida que cumplen con el esquema XML de proveedor OSC. El OSC llama a estos métodos para obtener información que puede comprender como se define en el esquema XML.
  
> [!NOTE]
> Extensibilidad de proveedores OSC es compatible con los proveedores de depuración estableciendo el `DebugProviders` valor de la `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` clave del registro en 1. Cuando se activa el proveedor de depuración, el OSC valida el proveedor XML frente a la versión del esquema XML de OSC que especifique en el atributo XML **xmlns** . Para 1.1 OSC y versiones de la OSC desde Outlook Social Connector 2013, especifique el atributo **xmlns** como se indica a continuación:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>En esta sección

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md): describe las distintas maneras en que pueden sincronizar proveedores de OSC amigos, que no sean de amigos y actividades en una red social. 
    
- [Ejemplos de XML de proveedor de OSC](osc-provider-xml-examples.md): ejemplos de XML incluye que muestran cómo especificar las capacidades de un proveedor de OSC, amigos y actividad de fuente de los elementos en una red social utilizando el esquema XML de OSC.
    
- [XML de capacidades](xml-for-capabilities.md): se explica el - método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que usa el OSC para obtener información sobre las capacidades, expresado en el XML de las **capacidades** , desde el proveedor de OSC. Esta sección también describen los elementos XML en el esquema XML de proveedor OSC que permiten a un proveedor de OSC especificar su funcionalidad, incluido cómo autentica a los usuarios y se sincroniza amigos y actividades. 
    
- [XML para amigos](xml-for-friends.md): se proporcionan ejemplos de las API que usa el OSC para obtener información de amigos, expresado en **amigos** XML, desde el proveedor de OSC. Esta sección también describen los elementos de **amigos** XML. 
    
- [XML para actividades](xml-for-activities.md): se proporcionan ejemplos de las API que usa el OSC para obtener información sobre actividades, expresado en **activityFeed** XML, desde el proveedor de OSC. Esta sección también describen los elementos XML en el esquema XML de proveedor OSC que permiten a un proveedor de OSC especificar una fuente de actividades. Una fuente de actividades incluye la red donde la actividad de fuente de los elementos de origen, detalles de cada elemento de la fuente de actividades (como propietario, escriba y fecha de publicación de la actividad) y la plantilla para mostrar la actividad. 
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Depurar un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Prácticas recomendadas para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Ver también

- [Depurar un proveedor](debugging-a-provider.md)

