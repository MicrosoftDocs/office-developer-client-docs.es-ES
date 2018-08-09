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
- Project 2013, programación, programación, Project Server, Project 2013 y la arquitectura de beneficios para EPM, arquitectura y Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821439"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Programación y arquitectura de Project Server 2013

Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
  
Project Server 2013 se ha creado con .NET Framework 4 y es la tercera versión principal de Project Server para proporcionar una arquitectura de varios niveles es true. Obtener acceso a la nube, Project Server 2013 implementa un modelo de objetos de cliente (COM) y un servicio de OData para informes que se puede usar en las aplicaciones web, aplicaciones móviles y aplicaciones de Silverlight. Para las aplicaciones locales, los clientes pueden utilizar el CSOM o los servicios de Project Server Interface (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Introducción a la arquitectura de Project Server

En los temas de esta sección se describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
  
Para obtener acceso mediante programación a Project Server, debe usar el CSOM o los servicios de PSI con la interfaz de Windows Communication Foundation (WCF). La interfaz de servicio web ASMX de la PSI está en desuso en Project Server 2013, pero sigue funcionando. PSI permite un acceso eficaz mediante el uso de conjuntos de datos y se pueden crear controladores de eventos del lado del servidor. El CSOM propio usa la PSI para obtener acceso a la capa de objetos de negocios de Project Server. En lugar de cuatro bases de datos de Project Server, Project Server 2013 usa una sola base de datos de la capa de acceso a datos.
  
Project Server 2013 se integra profundamente con SharePoint Server 2013. El servicio de aplicación de Project se puede asociar con otras colecciones de sitios de SharePoint en la granja de servidores. Project Server puede funcionar con e informar sobre SharePoint las listas de tareas en la colección de sitios y puede también obtener control total, donde Project Server importa y administra que listas de la tarea como proyectos de empresa. Project Server también usa la versión 4 de Windows Workflow Foundation (WF4) y agrega las actividades de flujo de trabajo para soluciones de administración de propuestas.
  
Para obtener una explicación de las muchas nuevas características que ofrece Project 2013 para desarrolladores y de las características que están en desuso, vea [actualizaciones de programadores de Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>En esta sección

[Arquitectura de Project Server 2013](project-server-2013-architecture.md) describe los principales elementos de la plataforma de Project 2013, incluidos los clientes y servidores. 
  
[Programación de Project Server](project-server-programmability.md) se describen las características de extensibilidad principal de Project Server 2013, personalización de Project Web App y actualización de aplicaciones que se crean para versiones anteriores de Project Server. 
  
[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describe escenarios en los que la PSI puede utilizarse y menciona cosas que la PSI no puede realizar. 
  
[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describe escenarios en los que el CSOM puede utilizarse y menciona cosas que el CSOM no puede realizar. 
  
### <a name="topics-not-covered"></a>Temas no abordados

Los artículos en la sección *programación y arquitectura* de documentos no las características de los clientes de escritorio de proyecto (Project Standard 2013 y Project Professional 2013) o Project Web App. 
  
La ayuda de Visual Basic para aplicaciones (VBA) está disponible en el editor de Visual Basic dentro de Project Standard y Project Professional.
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)
    
- [Comenzar desarrollando flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md)
    

