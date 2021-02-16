---
title: Programación y arquitectura de Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, arquitectura y programación,Programación, Project Server,Project 2013, ventajas para EPM,Architecture y Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413790"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Programación y arquitectura de Project Server 2013

Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
  
Project Server 2013 se creó con .NET Framework 4 y es la tercera versión principal de Project Server que proporciona una verdadera arquitectura de varios mundos. Para el acceso a la nube, Project Server 2013 implementa un modelo de objetos de cliente (CSOM) y un servicio OData para los informes que se pueden usar en aplicaciones web, aplicaciones móviles y aplicaciones de Silverlight. Para aplicaciones locales, los clientes pueden usar el CSOM o bien los servicios de Interfaz de Project Server (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Introducción a la arquitectura de Project Server

En los temas de esta sección se describe la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
  
Para obtener acceso mediante programación a Project Server, debe usar el CSOM o los servicios de PSI con la interfaz de Windows Communication Foundation (WCF). La interfaz del servicio web ASMX de PSI está en desuso en Project Server 2013, pero sigue funcionando. La PSI permite el acceso eficiente utilizando conjuntos de datos y puede crear controladores para eventos de servidor. El CSOM utiliza la PSI para acceder a la capa de objeto de negocios de Project Server. En lugar de cuatro bases de datos de Project Server, Project Server 2013 usa una sola base de datos en el nivel de acceso a datos.
  
Project Server 2013 se integra profundamente con SharePoint Server 2013. El Servicio de aplicación de Project puede asociarse con otros grupos de sitio de SharePoint de la granja de servidores. Project Server puede funcionar con las listas de tareas de SharePoint en el grupo de sitios y elaborar informes sobre ellas y tambi{en puede obtener control pleno cuando Project Server importa y administra las listas de tareas como proyectos empresariales. Project Server también usa la versión 4 de Windows Workflow Foundation (WF4) y agrega actividades de flujo de trabajo para soluciones de administración de demanda.
  
Para obtener una explicación de las muchas características nuevas que Project 2013 proporciona a los desarrolladores y de las características que están en desuso, vea Actualizaciones para desarrolladores en [Project 2013.](updates-for-developers-in-project-2013.md)
  
## <a name="in-this-section"></a>En esta sección

[La arquitectura de Project Server 2013](project-server-2013-architecture.md) describe las partes principales de la plataforma de Project 2013, incluidos los clientes y servidores. 
  
[La programación](project-server-programmability.md) de Project Server analiza las principales características de extensibilidad de Project Server 2013, la personalización de Project Web App y la actualización de aplicaciones creadas para versiones anteriores de Project Server. 
  
[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describe escenarios en los que la PSI puede utilizarse y menciona cosas que la PSI no puede realizar. 
  
[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describe escenarios en los que el CSOM puede utilizarse y menciona cosas que el CSOM no puede realizar. 
  
### <a name="topics-not-covered"></a>Temas no abordados

Los artículos  de la sección Arquitectura y programación no documentan las características de los clientes de escritorio de Project (Project Standard 2013 y Project Professional 2013) ni Project Web App. 
  
La ayuda de Visual Basic para aplicaciones (VBA) está disponible en el editor de Visual Basic dentro de Project Standard y Project Professional.
  
## <a name="see-also"></a>Consulte también
<a name="bk_addresources"> </a>

- [Actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)
    
- [Introducción al desarrollo de flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md)
    

