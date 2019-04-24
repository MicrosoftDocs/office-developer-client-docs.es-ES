---
title: XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'El elemento Capabilities del esquema XML del proveedor (OSC) permite a un proveedor OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356451"
---
# <a name="xml-for-capabilities"></a>XML de capacidades

El elemento **Capabilities** del esquema XML del proveedor (OSC) permite a un proveedor OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente: 
  
- Si el proveedor admite la obtención, el almacenamiento en caché o la búsqueda dinámica de amigos y actividades desde la red social.
    
- Cómo el OSC debe mostrar ciertas interfaces de inicio de sesión de usuario.
    
- Si OSC debe usar la autenticación basada en formularios o configurar automáticamente la red social e iniciar sesión en el usuario en la red social.
    
El esquema XML para **capacidades** es crítico porque identifica a la funcionalidad admitida por el proveedor para el OSC. Un proveedor OSC debe implementar el método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) que devuelve una cadena de _resultado_ . El OSC llama a **ISocialProvider:: GetCapabilities** para obtener información sobre las funciones del proveedor OSC en la cadena de _resultado_ , que cumple con la definición del esquema XML para el elemento **Capabilities** . Esta información permite que las llamadas posteriores desde el OSC al proveedor de OSC funcionen correctamente. 
  
Para especificar las capacidades de un proveedor de OSC como un parámetro de salida del método **ISocialProvider:: GetCapabilities** , debe cumplir con el esquema XML de extensibilidad del proveedor OSC. En la siguiente figura se muestra la estructura XML **Capabilities** . 
  
**Figura 1. \<estructura\> XML de capacidades**

![Estructura XML de capacidades](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Para obtener descripciones detalladas de los elementos secundarios del elemento **Capabilities** , vea [Capabilities XML Elements](capabilities-xml-elements.md). Para obtener un ejemplo de XML de **capacidades** , vea el [ejemplo de XML de Capabilities](capabilities-xml-example.md). Para obtener una definición completa del esquema XML del proveedor de OSC, incluidos los elementos necesarios u opcionales, vea el [esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de capacidades](capabilities-xml-example.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para actividades](xml-for-activities.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

