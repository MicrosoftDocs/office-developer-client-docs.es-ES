---
title: Pasos rápidos para aprender a desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: En este tema se sugieren algunos pasos para obtener información sobre cómo desarrollar un Outlook de Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424220"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Pasos rápidos para aprender a desarrollar un proveedor

Para desarrollar un proveedor de OSC, debe completar los siguientes pasos generales:
  
- Implemente las cuatro interfaces obligatorias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)y [ISocialPerson](isocialpersoniunknown.md). Dependiendo de la compatibilidad de la red social para almacenar en caché las credenciales de inicio de sesión, seguir a una persona en la red social o sincronizar dinámicamente amigos y sus actividades, es posible que desee implementar la interfaz [ISocialSession2.](isocialsession2iunknown.md) 
    
- En paralelo con la implementación de interfaces, pruebe y depure el proveedor de OSC. 

- Implemente el proveedor de OSC.  

- Realice las pruebas finales antes del lanzamiento.
    
## <a name="step-a-implementing-interfaces"></a>Paso A: Implementar interfaces

Un proveedor de OSC implementa interfaces para que el OSC pueda usar estas interfaces para obtener información necesaria sobre o desde la red social, a través del proveedor de OSC. Esta información incluye lo siguiente:
  
- Cómo presentar el cuadro de diálogo de inicio de sesión de la cuenta a un usuario.    
- Si el proveedor admite mostrar amigos o actividades como se muestra en la red social.    
- Cómo mostrar amigos y actividades en la tarjeta de contacto o en el panel Outlook personas.     
- Cuándo actualizar la información de amigos o actividades en la tarjeta de contacto o el panel de personas.
    
La información normalmente se pasa del proveedor al OSC, en forma de cadenas XML como parámetros de salida de métodos de interfaz. Tanto el OSC como un proveedor de OSC cumplen con el esquema XML del proveedor de OSC. Por lo tanto, en el transcurso de la implementación de las interfaces, necesita una buena comprensión de cómo el esquema XML le permite especificar información como se indica anteriormente. 

Los siguientes recursos explican cómo especificar XML para las capacidades del proveedor, los amigos y las actividades:
  
- [Secuencias de llamadas típicas de OSC](osc-typical-calling-sequences.md)    
- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md)    
- [Ejemplo XML de funcionalidades](capabilities-xml-example.md)   
- [XML para funcionalidades](xml-for-capabilities.md)    
- [Ejemplo de XML de amigos](friends-xml-example.md)    
- [XML para amigos](xml-for-friends.md)   
- [Ejemplo XML de fuente de actividad](activity-feed-xml-example.md)   
- [XML para actividades](xml-for-activities.md)
    
Antes de iniciar la implementación, consulte también los siguientes temas para ahorrar tiempo más adelante en el proceso de depuración:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)    
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Paso B: Depuración

El tema [Depuración de un proveedor](debugging-a-provider.md) sugiere procedimientos de depuración que puede usar al desarrollar un proveedor de OSC. 
  
Durante el desarrollo, también puede hacer referencia a Getting [Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) para comprender mejor el comportamiento esperado en determinados escenarios (por ejemplo, autenticación básica y basada en formularios). 
  
## <a name="step-c-deploying"></a>Paso C: Implementación

Consulte los siguientes temas para obtener información sobre los requisitos de implementación:
  
- [Implementación de un proveedor](deploying-a-provider.md)    
- [Registro de un proveedor](registering-a-provider.md)   
- [Lista de comprobación de instalación](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Paso D: Prueba final antes del lanzamiento

Según la red social y el proveedor de OSC, normalmente hay pruebas específicas del proveedor que debe llevar a cabo antes de liberar al proveedor. Para obtener una lista sugerida de pruebas, vea [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Vea también

- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

