---
title: Desarrollar un proveedor con el esquema XML de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: El esquema XML del proveedor de Outlook Social Connector (OSC) define el formato de una cantidad significativa de información que se pasa desde una red social a través del proveedor de OSC de la red al OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539258"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Desarrollar un proveedor con el esquema XML de OSC

El esquema XML del proveedor de Outlook Social Connector (OSC) define el formato de una cantidad significativa de información que se pasa desde una red social a través del proveedor de OSC de la red al OSC. El esquema XML permite a un proveedor OSC especificar capacidades del proveedor, amigos y elementos de la fuente de actividades de la red social mediante los tres elementos principales, **funciones**, **amigos**y **activityFeed**, y sus hijos elemento. El proveedor OSC implementa interfaces y sus métodos en la extensibilidad del proveedor OSC, devolviendo cadenas XML como parámetros de salida que cumplen con el esquema XML del proveedor OSC. El OSC llama a estos métodos para obtener información que puede entender como definida por el esquema XML.
  
> [!NOTE]
> La extensibilidad de proveedores de OSC admite la depuración de proveedores estableciendo el `DebugProviders` valor de la `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` clave del registro en 1. Cuando se activa la depuración del proveedor, el OSC valida el XML del proveedor con respecto a la versión del esquema XML de OSC que se especifica en el atributo XML **xmlns** . Para OSC 1,1 y versiones de OSC desde Outlook Social Connector 2013, especifique el atributo **xmlns** de la siguiente manera:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>En esta sección

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md): describe las distintas formas en que los proveedores de OSC pueden sincronizar amigos, no amigos y actividades en una red social. 
    
- [Ejemplos de XML del proveedor OSC](osc-provider-xml-examples.md): incluye ejemplos de XML que muestran cómo especificar funcionalidades de un proveedor OSC, amigos y elementos de fuentes de actividades en una red social mediante el esquema XML OSC.
    
- [XML para capacidades](xml-for-capabilities.md): explica el método- [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) que utiliza el OSC para obtener información de capacidades, expresada en el XML de **capacidades** , del proveedor OSC. En esta sección también se describen los elementos XML en el esquema XML del proveedor OSC que permiten a un proveedor de OSC especificar su funcionalidad, incluido cómo autentica a los usuarios y sincroniza amigos y actividades. 
    
- [XML para amigos](xml-for-friends.md): proporciona ejemplos de las API que el OSC utiliza para obtener información sobre amigos, expresada en XML de **amigos** , del proveedor de OSC. En esta sección también se describen los elementos del XML de **amigos** . 
    
- [XML for Activities](xml-for-activities.md): proporciona ejemplos de las API que el OSC utiliza para obtener información de actividades, expresada en **activityFeed** XML, del proveedor de OSC. En esta sección también se describen los elementos XML en el esquema XML del proveedor OSC que permiten a un proveedor OSC especificar una fuente de actividades. Una fuente de actividades incluye la red en la que se originaron los elementos de la fuente de actividades, los detalles de cada elemento de la fuente de actividades (como el propietario, el tipo y la fecha de publicación de la actividad) y la plantilla para mostrar la actividad. 
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Depuración de un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Vea también

- [Depuración de un proveedor](debugging-a-provider.md)

