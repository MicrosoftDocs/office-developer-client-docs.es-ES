---
title: Secuencias de llamada típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: En esta sección se describen las secuencias de llamadas típicas de Outlook Social Connector (OSC) de miembros en las interfaces de extensibilidad del proveedor de OSC, que implementa un proveedor de OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413615"
---
# <a name="osc-typical-calling-sequences"></a>Secuencias de llamada típicas de OSC

En esta sección se describen las secuencias de llamadas típicas de Outlook Social Connector (OSC) de miembros en las interfaces de extensibilidad del proveedor de OSC, que implementa un proveedor de OSC. Las secuencias de llamadas típicas ilustran cómo y cuándo el OSC usa estas interfaces y métodos, para determinar mejor cómo implementar un miembro determinado en una interfaz de extensibilidad de proveedor. La secuencia de llamadas real puede variar en función de las capacidades devueltas por el [método ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md) Algunos ejemplos de funcionalidades son los siguientes: 
  
- Compatibilidad del proveedor para obtener, almacenar en caché o buscar dinámicamente amigos y actividades desde la red social.
    
- La interfaz de usuario que el OSC debe mostrar para el inicio de sesión del usuario.
    
- Tipo de autenticación (por ejemplo, autenticación basada en formularios) que debe usar el OSC.
    
## <a name="in-this-section"></a>En esta sección

- [Autenticación](basic-authentication.md)básica: describe la secuencia de llamadas típica del OSC para admitir un usuario de Office que inicia sesión en una red social, si el proveedor de OSC admite la autenticación básica.
    
- [Autenticación](forms-based-authentication.md)basada en formularios: describe la secuencia de llamadas típica del OSC para admitir un usuario de Office que inicia sesión en una red social, si el proveedor de OSC admite la autenticación basada en formularios.
    
- [Obtener actividades:](getting-activities.md)describe la secuencia de llamadas típica del OSC para sincronizar las actividades de los amigos del usuario de Office desde una red social, si el proveedor de OSC de red social admite la sincronización de actividades.
    
- [Obtener](getting-friends-information.md)información de amigos: describe la secuencia de llamadas típica del OSC para sincronizar la lista de amigos del usuario de Office desde una red social, si el proveedor de OSC de red social admite la sincronización en caché de contactos.
    
## <a name="reference"></a>Referencia

- [Outlook Referencia del proveedor de Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depuración de un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)

