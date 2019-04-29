---
title: Pasos rápidos para aprender a desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: En este tema se sugieren algunos pasos para aprender a desarrollar un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424220"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Pasos rápidos para aprender a desarrollar un proveedor

Para desarrollar un proveedor OSC, debe completar los siguientes pasos generales:
  
- Implemente las cuatro interfaces obligatorias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)y [ISocialPerson](isocialpersoniunknown.md). Según la compatibilidad de su red social con el almacenamiento en caché de las credenciales de inicio de sesión, el seguimiento de una persona en la red social o la sincronización dinámica de amigos y sus actividades, es posible que desee implementar la interfaz de [ISocialSession2](isocialsession2iunknown.md) . 
    
- En paralelo con la implementación de interfaces, pruebe y Depure el proveedor de OSC. 

- Implemente el proveedor de OSC.  

- Realice las pruebas finales antes de la publicación.
    
## <a name="step-a-implementing-interfaces"></a>Paso A: implementación de interfaces

Un proveedor OSC implementa interfaces para que el OSC pueda usarlas para obtener información necesaria sobre o desde la red social a través del proveedor de OSC. Esta información incluye lo siguiente:
  
- Cómo presentar el cuadro de diálogo de inicio de sesión de la cuenta a un usuario.    
- Si el proveedor admite la visualización de amigos o actividades como se muestra en la red social.    
- Cómo mostrar amigos y actividades en el panel de la tarjeta de contacto o de personas de Outlook.     
- Cuándo actualizar la información de amigos o actividades en la tarjeta de contacto o en el panel de personas.
    
Normalmente, la información se pasa del proveedor al OSC, en forma de cadenas XML como parámetros de salida de los métodos de interfaz. Tanto OSC como un proveedor de OSC cumplen con el esquema XML del proveedor OSC. Por lo tanto, en el transcurso de la implementación de las interfaces, necesitará una buena comprensión de cómo el esquema XML le permite especificar la información indicada anteriormente. 

Los siguientes recursos explican cómo especificar XML para capacidades, amigos y actividades del proveedor:
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)    
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)    
- [Ejemplo de XML de capacidades](capabilities-xml-example.md)   
- [XML para funcionalidades](xml-for-capabilities.md)    
- [Ejemplo de XML de amigos](friends-xml-example.md)    
- [XML para amigos](xml-for-friends.md)   
- [Ejemplo de XML de fuente de actividades](activity-feed-xml-example.md)   
- [XML para actividades](xml-for-activities.md)
    
Antes de comenzar con la implementación, consulte también los siguientes temas para ahorrar tiempo más adelante en el proceso de depuración:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)    
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Paso B: dePurar

El tema [depuración de un proveedor](debugging-a-provider.md) sugiere procedimientos de depuración que puede usar al desarrollar un proveedor de OSC. 
  
Mientras está desarrollando, también puede consultar el tema [Getting Ready to release a OSC Provider](getting-ready-to-release-an-osc-provider.md) para obtener una mejor comprensión del comportamiento esperado en determinados escenarios (por ejemplo, autenticación básica y basada en formularios). 
  
## <a name="step-c-deploying"></a>Paso C: implementación

Consulte los siguientes temas para obtener información sobre los requisitos de implementación:
  
- [Implementación de un proveedor](deploying-a-provider.md)    
- [Registrar un proveedor](registering-a-provider.md)   
- [Lista de comprobación de instalación](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Paso D: pruebas finales antes de la publicación

En función de su red social y del proveedor de OSC, normalmente hay pruebas específicas del proveedor que debe realizar antes de publicar el proveedor. Para obtener una lista de pruebas recomendadas, vea [Getting Ready to release a OSC Provider](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Ver también

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

