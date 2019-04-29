---
title: Secuencias de llamada típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: En esta sección se describen las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad del proveedor OSC, que implementa un proveedor OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413615"
---
# <a name="osc-typical-calling-sequences"></a>Secuencias de llamada típicas de OSC

En esta sección se describen las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad del proveedor OSC, que implementa un proveedor OSC. Las secuencias de llamada típicas ilustran cómo y cuándo el OSC utiliza interfaces y métodos tales, para permitirle determinar mejor cómo implementar un miembro determinado en una interfaz de extensibilidad del proveedor. La secuencia de llamada real puede variar en función de las funciones devueltas por el método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) . Algunos ejemplos de capacidades son los siguientes: 
  
- Proveedor admite la obtención, almacenamiento en caché o la búsqueda dinámica de amigos y actividades desde la red social.
    
- Interfaz de usuario que el OSC debe mostrar para el inicio de sesión del usuario.
    
- El tipo de autenticación (por ejemplo, autenticación basada en formularios) que el OSC debe usar.
    
## <a name="in-this-section"></a>En esta sección

- [Autenticación básica](basic-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que inicie sesión en una red social, si el proveedor de OSC admite la autenticación básica.
    
- [Autenticación basada en formularios](forms-based-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que inicie sesión en una red social, si el proveedor de OSC admite la autenticación basada en formularios.
    
- [Getting Activities](getting-activities.md): describe la secuencia de llamada típica de OSC para sincronizar las actividades de los amigos del usuario de Office desde una red social, si el proveedor de Networks OSC admite la sincronización de actividades.
    
- [Obtener información sobre amigos](getting-friends-information.md): describe la secuencia de llamada típica de OSC para sincronizar la lista de amigos del usuario de Office desde una red social, si el proveedor de Networks OSC admite la sincronización de contactos en caché.
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [DePuración de un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Ver también

- [XML para funcionalidades](xml-for-capabilities.md)

