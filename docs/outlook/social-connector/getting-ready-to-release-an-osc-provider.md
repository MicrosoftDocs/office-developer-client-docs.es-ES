---
title: Prepararse para publicar un proveedor de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugieren pruebas que puede realizar antes de lanzar el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414665"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Prepararse para publicar un proveedor de OSC

En esta sección se sugieren pruebas que puede realizar antes de lanzar el proveedor de Outlook Social Connector (OSC). Puedes empezar a hacer referencia a los temas de esta sección y llevar a cabo algunas de estas pruebas durante las fases de desarrollo y pruebas, pero debes haber completado estas pruebas en el momento de publicar. 

Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces del proveedor de OSC con respecto a las funcionalidades que especifique para el proveedor de OSC. Además, aunque el OSC es una característica compartida por varias aplicaciones cliente de Office, estas pruebas usan Outlook como cliente para probar la funcionalidad fundamental. Debe determinar si son necesarias otras pruebas para características específicas de su proveedor.
  
## <a name="in-this-section"></a>En esta sección

- [Implementación de](testing-deployment.md)pruebas: describe los escenarios que debes probar en torno a la instalación y desinstalación de un proveedor de OSC.
    
- [Capacidades de prueba, autenticación](testing-capabilities-authentication-and-configuration.md)y configuración: describe las pruebas para obtener funcionalidades y escenarios en torno a la configuración de una cuenta y la autenticación de un usuario para una red social.
    
- [Pruebas siguientes y Stop-Following personas:](testing-following-and-stop-following-persons.md)describe escenarios para probar la capacidad del proveedor de OSC para agregar a una persona como un amigo o para quitar a un amigo de la red social. 
    
- [Pruebas](testing-friends.md)de amigos: describe pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente datos de amigos y no amigos, si procede, según el modo de sincronización que admita el proveedor.
    
- [Actividades](testing-activities.md)de prueba: describe pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente las actividades de amigos y no amigos, si procede, según el modo de sincronización que admita el proveedor.
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  

