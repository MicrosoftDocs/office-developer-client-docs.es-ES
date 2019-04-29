---
title: Preparación para la publicación de un proveedor OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugieren las pruebas que puede realizar antes de liberar su proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414665"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Preparación para la publicación de un proveedor OSC

En esta sección se sugieren las pruebas que puede realizar antes de liberar su proveedor de Outlook Social Connector (OSC). Puede empezar a hacer referencia a los temas de esta sección y realizar algunas de estas pruebas durante las fases de desarrollo y pruebas, pero debe haber completado estas pruebas en el momento de la publicación. 

Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces del proveedor de OSC con respecto a las capacidades especificadas para el proveedor de OSC. Además, aunque OSC es una característica compartida por varias aplicaciones cliente de Office, estas pruebas usan Outlook como cliente para probar la funcionalidad fundamental. Debe determinar si hay otras pruebas necesarias para las características específicas de su proveedor.
  
## <a name="in-this-section"></a>En esta sección

- [Prueba](testing-deployment.md)de la implementación: describe los escenarios que se deben probar en la instalación y desinstalación de un proveedor OSC.
    
- [Capacidades de prueba, autenticación y configuración](testing-capabilities-authentication-and-configuration.md): describe las pruebas para obtener capacidades y los escenarios en los que se configura una cuenta y se autentica a un usuario para una red social.
    
- [Pruebas de seguimiento y detención de las siguientes personas](testing-following-and-stop-following-persons.md): describe los escenarios para probar la capacidad del proveedor de OSC para agregar a una persona como amigo o para quitar un amigo de la red social. 
    
- [Probando amigos](testing-friends.md): describe las pruebas y los escenarios para comprobar que el proveedor de OSC devuelve correctamente datos de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.
    
- [Actividades de prueba](testing-activities.md): describe las pruebas y los escenarios para comprobar que el proveedor de OSC devuelve correctamente actividades de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Plantillas de ejemplo de OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [DePuración de un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  

