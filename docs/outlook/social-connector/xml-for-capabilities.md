---
title: XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'El elemento de funciones en el esquema XML de proveedor (OSC) permite que un proveedor de OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821215"
---
# <a name="xml-for-capabilities"></a>XML de capacidades

El elemento de **funciones** en el esquema XML de proveedor (OSC) permite que un proveedor de OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente: 
  
- Si el proveedor admite la introducción, el almacenamiento en caché o buscar dinámicamente amigos y actividades de la red social.
    
- Cómo el OSC debe mostrar ciertas interfaces de usuario de inicio de sesión.
    
- Si el OSC debe usar la autenticación basada en formularios o configurar automáticamente las redes sociales y los registros en el usuario en la red social.
    
El esquema XML de **las capacidades** es fundamental ya que identifica a la OSC la funcionalidad admitida por el proveedor. Un proveedor de OSC debe implementar el método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que devuelve una cadena de _resultado_ . El OSC llama a **ISocialProvider::GetCapabilities** para obtener información acerca de las capacidades del proveedor de OSC en la cadena de _resultado_ , que cumple con la definición del esquema XML para el elemento **capabilities** . Esta información permite las llamadas posteriores desde el OSC para el proveedor de OSC funcionar correctamente. 
  
Para especificar las capacidades de un proveedor de OSC como un parámetro de salida del método **ISocialProvider::GetCapabilities** , debe cumplir el esquema XML de extensibilidad de proveedor OSC. La siguiente ilustración muestra la estructura XML de **las capacidades** . 
  
**En la figura 1. \<capacidades\> estructura XML**

![Estructura XML de capacidades](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Para obtener descripciones detalladas de los elementos secundarios del elemento de **funciones** , vea [Los elementos XML de las capacidades](capabilities-xml-elements.md). Para obtener un ejemplo de XML de las **capacidades** , vea [Ejemplo de XML de las capacidades](capabilities-xml-example.md). Para ver una definición completa del esquema XML de proveedor OSC, incluido qué elementos son obligatorios u opcionales, vea [Esquema de XML de Outlook Social Connector proveedor](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de capacidades](capabilities-xml-example.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML de amigos](xml-for-friends.md)  
- [XML de actividades](xml-for-activities.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)

