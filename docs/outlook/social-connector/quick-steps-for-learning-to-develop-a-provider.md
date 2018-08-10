---
title: Pasos rápidos para aprender a desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: En este tema se sugiere algunos pasos para obtener más información acerca de cómo desarrollar un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821212"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Pasos rápidos para aprender a desarrollar un proveedor

Para desarrollar un proveedor de OSC, debe completar los siguientes pasos generales:
  
- Implementar las cuatro interfaces obligatorias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)y [ISocialPerson](isocialpersoniunknown.md). Función de soporte técnico de su red social para almacenar en caché las credenciales de inicio de sesión, seguimiento de una persona en la red social, o dinámicamente sincronización amigos y sus actividades, es posible que desee implementar la interfaz [ISocialSession2](isocialsession2iunknown.md) . 
    
- En paralelo con la implementación de interfaces, probar y depurar el proveedor de OSC. 

- Implementar el proveedor de OSC.  

- Realice pruebas finales antes del lanzamiento.
    
## <a name="step-a-implementing-interfaces"></a>Paso A: implementar interfaces

Un proveedor de OSC implementa interfaces para que el OSC puede usar estas interfaces para obtener la información necesaria sobre o desde la red social, a través del proveedor OSC. Dicha información incluye lo siguiente:
  
- Procedimiento para presentar el cuadro de diálogo de inicio de sesión de cuenta para un usuario.    
- Si el proveedor admite que muestra amigos o actividades, tal como se muestra en la red social.    
- Cómo mostrar amigos y actividades en la tarjeta de contacto o el panel de personas de Outlook.     
- Cuándo se debe actualizar la información de amigos o actividades en la tarjeta de contacto o el panel de personas.
    
La información normalmente se pasa desde el proveedor al OSC, con el formato de cadenas XML como parámetros de salida de los métodos de interfaz. El OSC y un proveedor de OSC cumplan con el esquema XML de proveedor OSC. Por lo tanto, en el transcurso de implementar las interfaces, necesita una buena comprensión de cómo el esquema XML permite especificar información como enumerados anteriormente. 

Los siguientes recursos explican cómo especificar XML de actividades, amigos y capacidades de proveedor:
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)    
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)    
- [Ejemplo de XML de capacidades](capabilities-xml-example.md)   
- [XML de capacidades](xml-for-capabilities.md)    
- [Ejemplo de XML de amigos](friends-xml-example.md)    
- [XML de amigos](xml-for-friends.md)   
- [Ejemplo de XML de fuentes de actividades](activity-feed-xml-example.md)   
- [XML de actividades](xml-for-activities.md)
    
Antes de comenzar la implementación, consulte también los temas siguientes para ahorrar tiempo más adelante en el proceso de depuración:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Prácticas recomendadas para desarrollar un proveedor](best-practices-for-developing-a-provider.md)    
- [Plantillas de ejemplo OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Depuración de paso B:

El tema [Depurar un proveedor](debugging-a-provider.md) se sugieren procedimientos que puede utilizar al desarrollar un proveedor de OSC de depuración. 
  
Mientras desarrolla, también puede hacer referencia a [Introducción listo para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md) para obtener una mejor comprensión del comportamiento esperado en ciertos escenarios (por ejemplo, la autenticación básica y basada en formularios). 
  
## <a name="step-c-deploying"></a>Implementación de paso C:

Consulte los siguientes temas para obtener más información acerca de los requisitos de implementación:
  
- [Implementación de un proveedor](deploying-a-provider.md)    
- [Registrar un proveedor](registering-a-provider.md)   
- [Lista de comprobación de instalación](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Paso D: las pruebas antes del lanzamiento de Final

Dependiendo de su red social y el proveedor de OSC, existen pruebas específicas del proveedor normalmente que debe llevar a cabo antes de liberar su proveedor. Para obtener una lista sugerida de pruebas, vea [Introducción listo para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Vea también

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

