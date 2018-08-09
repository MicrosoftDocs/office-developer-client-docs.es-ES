---
title: Prepararse liberar un proveedor de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugiere las pruebas que se puede hacer antes de liberar su proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821092"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Prepararse liberar un proveedor de OSC

En esta sección se sugiere las pruebas que se puede hacer antes de liberar su proveedor de Outlook Social Connector (OSC). Puede iniciar con respecto a los temas de esta sección y realizar algunas de estas pruebas durante el desarrollo y las fases de pruebas, pero debe haber completado estas pruebas en el momento en que se suelte. 

Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces de proveedor OSC con respecto a las capacidades que especifique para el proveedor de OSC. Además, aunque el OSC es una característica compartida por varias aplicaciones de cliente de Office, estas pruebas utilizan Outlook como el cliente para probar la funcionalidad fundamental. Debe determinar si otras pruebas son necesarias para características específicas a su proveedor.
  
## <a name="in-this-section"></a>En esta sección

- [Pruebas de implementación](testing-deployment.md): describe escenarios en los que se debe probar a la instalación y desinstalación de un proveedor de OSC.
    
- [Capacidades de las pruebas, la autenticación y la configuración](testing-capabilities-authentication-and-configuration.md): describe las pruebas de introducción, características y escenarios de configuración de una cuenta y la autenticación de un usuario para una red social.
    
- [Las pruebas siguientes y las personas o deje de seguir](testing-following-and-stop-following-persons.md): se describen escenarios para comprobar la capacidad de un proveedor OSC para agregar una persona como un amigo, o para quitar un amigo desde la red social. 
    
- [Prueba de amigos](testing-friends.md): describe las pruebas y escenarios para comprobar que el proveedor de OSC adecuadamente devuelve datos de amigos y que no sean-amigos, en su caso, según el modo de sincronización que admite el proveedor.
    
- [Las actividades de pruebas](testing-activities.md): describe las pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente las actividades de amigos y que no sean-amigos, en su caso, según el modo de sincronización que admite el proveedor.
    
## <a name="reference"></a>Referencia

- [Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Secciones relacionadas

- [Plantillas de ejemplo OSC](osc-sample-templates.md)
  
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)
  
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar un proveedor](debugging-a-provider.md)
  
- [Implementación de un proveedor](deploying-a-provider.md)
  

