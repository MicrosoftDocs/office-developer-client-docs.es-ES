---
title: Secuencias de llamada típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: En esta sección se describe las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad de proveedor OSC, que implementa un proveedor de OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821205"
---
# <a name="osc-typical-calling-sequences"></a>Secuencias de llamada típicas de OSC

En esta sección se describe las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad de proveedor OSC, que implementa un proveedor de OSC. Las secuencias de llamada típicas ilustran cómo y cuándo la OSC usa estas interfaces y métodos que permiten una mejor determinación del procedimiento para implementar un miembro dado en una interfaz de extensibilidad del proveedor. La secuencia de llamada real puede variar dependiendo de las capacidades devueltas por el método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) . Algunos ejemplos de capacidades son las siguientes: 
  
- Proveedor de compatibilidad para obtener, almacenamiento en caché o buscar dinámicamente amigos y actividades de la red social.
    
- La interfaz de usuario que se debe mostrar el OSC para inicio de sesión de usuario.
    
- El tipo de autenticación (por ejemplo, la autenticación basada en formularios) que se debe usar el OSC.
    
## <a name="in-this-section"></a>En esta sección

- [La autenticación básica](basic-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que está iniciando sesión en una red social, si el proveedor OSC admite la autenticación básica.
    
- [Autenticación basada en formularios](forms-based-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que está iniciando sesión en una red social, si el proveedor de OSC admite la autenticación basada en formularios.
    
- [Actividades de introducción](getting-activities.md): describe la secuencia de llamada típica del OSC para sincronizar las actividades de amigos del usuario de Office desde una red social, si el proveedor OSC de redes sociales admite la sincronización de actividades.
    
- [Obtención de información sobre amigos](getting-friends-information.md): describe la secuencia de llamada típica del OSC para sincronizar la lista de amigos del usuario de Office desde una red social, si el proveedor OSC de redes sociales admite la sincronización en caché de los contactos.
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo OSC](osc-sample-templates.md)
  
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Prácticas recomendadas para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Vea también

- [XML de capacidades](xml-for-capabilities.md)

