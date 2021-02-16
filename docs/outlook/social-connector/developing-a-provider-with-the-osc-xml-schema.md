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

El esquema XML del proveedor de Outlook Social Connector (OSC) define el formato de una cantidad significativa de información que se pasa desde una red social a través del proveedor de OSC de la red al OSC. El esquema XML permite a un proveedor de OSC especificar las capacidades del proveedor, los amigos y los elementos de fuente de actividades en la red social, mediante el uso de los tres elementos principales, **capacidades,** amigos y **activityFeed,** y sus elementos secundarios. El proveedor de OSC implementa interfaces y sus métodos en la extensibilidad del proveedor de OSC, devolviendo cadenas XML como parámetros de salida que cumplen con el esquema XML del proveedor de OSC. El OSC llama a estos métodos para obtener información que puede comprender según lo definido por el esquema XML.
  
> [!NOTE]
> La extensibilidad del proveedor de OSC admite la depuración de proveedores estableciendo el `DebugProviders` valor de la clave del Registro en  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 1. Al activar la depuración del proveedor, el OSC valida el XML del proveedor con la versión del esquema XML de OSC que especifique en el atributo XML **xmlns.** Para OSC 1.1 y versiones del OSC desde Outlook Social Connector 2013, especifique el atributo **xmlns** de la siguiente manera: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>En esta sección

- [Sincronización de amigos](synchronizing-friends-and-activities.md)y actividades: describe las distintas formas en que los proveedores de OSC pueden sincronizar amigos, no amigos y actividades en una red social. 
    
- Ejemplos XML del proveedor de [OSC:](osc-provider-xml-examples.md)incluye ejemplos XML que muestran cómo especificar funcionalidades de un proveedor de OSC, amigos y elementos de fuente de actividades en una red social mediante el esquema XML de OSC.
    
- [XML para](xml-for-capabilities.md)funcionalidades: explica el método - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que el OSC usa para obtener información de capacidades, expresada en **XML** de capacidades, del proveedor de OSC. En esta sección también se describen los elementos XML del esquema XML del proveedor de OSC que permiten a un proveedor de OSC especificar su funcionalidad, incluido cómo autentica a los usuarios y sincroniza amigos y actividades. 
    
- [XML para amigos:](xml-for-friends.md)proporciona ejemplos de las API que el OSC usa para obtener información de amigos, expresada en **XML** de amigos, del proveedor de OSC. En esta sección también se describen los elementos del XML **de amigos.** 
    
- [XML para actividades:](xml-for-activities.md)proporciona ejemplos de las API que el OSC usa para obtener información de actividades, expresada en **activityFeed** XML, del proveedor de OSC. En esta sección también se describen los elementos XML del esquema XML del proveedor de OSC que permiten a un proveedor de OSC especificar una fuente de actividades. Una fuente de actividades incluye la red en la que se originaron los elementos de la fuente de actividades, los detalles de cada elemento de fuente de actividades (como el propietario, el tipo y la fecha de publicación de la actividad) y la plantilla para mostrar la actividad. 
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Depurar un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Consulte también

- [Depurar un proveedor](debugging-a-provider.md)

