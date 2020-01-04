---
title: Documentación para desarrolladores de Project 2013
manager: lindalu
ms.date: 12/19/2019
ms.audience: Developer
f1_keywords:
- Project
- Project 2013
- Project 2013 SDK
- Project programmability
- Project SDK
- SDK
- SDK Project
keywords:
- sdk, project 2013, Project 2013, información general del SDK
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Encuentre documentación, ejemplos de código, artículos de procedimientos y referencias de programación que le ayuden a crear aplicaciones para la Tienda Office o un catálogo de aplicaciones privado, y a personalizar e integrar Project Server y los clientes de Project con una amplia variedad de aplicaciones de escritorio y empresariales para la administración de proyectos empresariales.
localization_priority: Priority
ms.openlocfilehash: 1b6227bb25810be04bc87abb418f9966b593bf1c
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825761"
---
# <a name="project-2013-developer-documentation"></a>Documentación para desarrolladores de Project 2013

Encuentre documentación, ejemplos de código, artículos de procedimientos y referencias de programación que le ayuden a crear aplicaciones para AppSource. Obtenga información sobre cómo personalizar e integrar Project Server y los clientes de Project con un amplia variedad de aplicaciones de escritorio y empresariales para la administración de proyectos empresariales (EPM).
   
> [!NOTE]
> Project Server 2013 se basa en la plataforma de SharePoint Server 2013 y Project 2013 incluye gran parte de la misma infraestructura que las demás aplicaciones de Office 2013. Para obtener documentación del modelo de complementos de SharePoint, flujos de trabajo basados en SharePoint, elementos web, desarrollo con otras características de SharePoint y documentación de los complementos de Office, vea [Complementos de SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) y [Complementos de Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins). 
  
## <a name="introduction-to-the-project-software-development-kit-sdk"></a>Introducción al kit de desarrollo de software (SDK) de Project
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 es una plataforma para crear soluciones de administración de proyectos empresariales locales o en la nube y aplicaciones que los usuarios finales pueden descubrir y adquirir mediante AppSource (anteriormente Tienda Office). La arquitectura de Project Server 2013 se basa en la plataforma que se presentó en Microsoft Office Project Server 2007, con muchas adiciones y mejoras. Entre las nuevas características se incluyen un modelo de objetos de cliente (CSOM) para habilitar el acceso a Project Online, un servicio OData para el acceso en línea a los datos de informes de Project Server, receptores de eventos remotos, arquitectura de flujo de trabajo que se basa en la versión 4 de Windows Workflow Foundation (WF4) y complementos de Office, que es una arquitectura común de extensiones del panel de tareas en las aplicaciones cliente de Microsoft Office 2013.
  
Un cambio importante en Project Server 2013 es el uso de una única base de datos en lugar de las bases de datos Borrador, Publicado, Archivo e Informes de Project Server 2010. Para obtener más información sobre las características nuevas y en desuso, consulte [Actualizaciones para desarrolladores de Project 2013](updates-for-developers-in-project-2013.md). Para obtener información sobre los cambios en la plataforma de Project Server, consulte [Arquitectura de Project Server 2013](project-server-2013-architecture.md). Para obtener información general sobre la plataforma de desarrollo disponible en Project Server 2010 y en la que se basa Project Server 2013, vea [Getting Started with Development for Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) (Introducción al desarrollo de Project 2010) en MSDN. 
  
Project Server 2013 se basa en Microsoft .NET Framework 4 y Microsoft SharePoint Server 2013. Los artículos y ejemplos de este SDK proporcionan un punto de partida para desarrollar soluciones y aplicaciones personalizadas, pero no cubren todas las características de programación de Project Server o Project Profesional. En el [Centro para desarrolladores de Project](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) se incluyen vínculos a artículos, blogs, vídeos, webcasts, artículos de procedimientos visuales y otros recursos de Project. 
  
El SDK de Project 2013 incluye información para desarrolladores de Project Server 2013, Project Web App, Project Profesional 2013 y Project Standard 2013. Los artículos del SDK están concebidos para ayudar a los desarrolladores y administradores a evaluar la extensibilidad de Project y Project Server, y a planear soluciones personalizadas.
  
### <a name="feedback"></a>Comentarios
<a name="pj15_Welcome_Feedback"> </a>

Nos gustaría conocer su opinión. En los temas en línea de MSDN puede agregar comentarios y ejemplos de código, o bien marcar el contenido como un error en la sección **Contenido de la comunidad** situada en la parte inferior de cada página. Al instalar la descarga del SDK de Project 2013, los artículos de documentación local tienen el vínculo *Enviar comentarios* que se encuentra debajo del título. En cualquier momento durante la lectura del SDK, haga clic en el vínculo para enviar un correo electrónico al equipo del SDK. Puede enviar correcciones, una solicitud de aclaración, un ejemplo de código u otros comentarios; de esta forma, nos ayudará a mejorar el contenido. 
  
### <a name="download"></a>Descargar
<a name="pj15_Welcome_Download"> </a>

El SDK de Project 2013 se puede descargar desde el [Centro de descarga de Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) (`https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). La descarga incluye Project2013SDK.HxS (el archivo que contiene este artículo), ejemplos de código relacionados, ensamblados redistribuibles y otros recursos. El SDK de Project 2013 aún no incluye la referencia de las tablas de datos de informes.
  
### <a name="whats-new-in-the-project-sdk"></a>Novedades del SDK de Project
<a name="pj15_Welcome_WhatsNew"> </a>

La finalidad principal del SDK de Project 2013 es proporcionar información general sobre programación y documentación del CSOM y características relacionadas para crear aplicaciones, servicios de Project Server Interface (PSI) y aplicaciones del panel de tareas de Project Profesional 2013. El SDK de Project 2013 incluye ejemplos detallados de las áreas fundamentales para personalizar Project Server 2013 y los clientes de Project (Project Standard 2013, Project Profesional 2013 y Project Web App). La documentación está incompleta; se agregará más contenido en versiones posteriores. 
  
La tecnología subyacente de comunicación de red es Windows Communication Foundation (WCF) en Project Server 2013, incluidos los escenarios en la nube que usan el CSOM de Project Server y el desarrollo local con la PSI. Las referencias a servicios web ASMX heredados también se basan en la arquitectura de WCF. Para configurar una referencia a un servicio web de la PSI (archivo ASMX) en Project Server 2013, es necesario anexar la opción de URL `?wsdl` a la ruta de acceso. Por ejemplo, `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Aunque solo trata las características de Project Server más usadas, le recomendamos que use el CSOM siempre que sea posible para aplicaciones locales y en la nube. A pesar de que aún está disponible en Project Server 2013, la interfaz ASMX para la PSI está en desuso. Con las aplicaciones locales que requieren acceso completo a la PSI, debe usar la interfaz WCF de la PSI, en lugar de la interfaz ASMX. 
  
Se admite el desarrollo en un equipo con Windows 7 si se copian los ensamblados de CSOM de Project Server 2013 y SharePoint Server 2013 en el equipo de desarrollo. La descarga del SDK incluye los ensamblados de CSOM de Project Server y una licencia de redistribución. Para obtener los ensamblados de CSOM de SharePoint, consulte [SharePoint Server 2013 Client Components SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585) (SDK de componentes cliente de SharePoint Server 2013).
  
Para el desarrollo con los servicios WCF, puede establecer una referencia a un ensamblado proxy de PSI o agregar archivos proxy de PSI a la solución. Puede establecer referencias directas a los servicios web ASMX front-end de Project Server desde un equipo remoto del mismo dominio o usar un ensamblado proxy o archivos proxy. La descarga del SDK incluye archivos proxy para los servicios web WCF y ASMX, además de scripts para crear los ensamblados proxy y para generar archivos proxy actualizados.
  
En Project Server 2013, puede crear flujos de trabajo declarativos de Project Server mediante Microsoft SharePoint Designer 2013, para uso local y en línea. SharePoint Designer 2013 usa los métodos y las propiedades de actividades de flujo de trabajo en el CSOM. El desarrollo y la implementación de las soluciones de Visual Studio 2012 que incluyen elementos web de Project Server o personalizaciones de Project Web App solo se admiten en un equipo de Project Server.
  
Para obtener información general sobre las nuevas características de programación y las que están en desuso en Project Server 2013, consulte [Actualizaciones para desarrolladores de Project 2013](updates-for-developers-in-project-2013.md). Otro cambio importante de Project Server 2013 es el uso de flujos de trabajo basados en WF4 para administrar la creación y la aprobación de propuestas de proyecto basadas en plantillas de proyecto empresariales. 
  
Los nuevos temas incluyen lo siguiente:
  
- En [Crear un complemento de Project Server hospedado por SharePoint](create-a-sharepoint-hosted-project-server-add-in.md) se muestra cómo usar Visual Studio para desarrollar de forma remota una aplicación que se puede usar con Project Server 2013 y Project Online. 
    
- En [Arquitectura de Project Server 2013](project-server-2013-architecture.md) se explican las características principales nuevas de la plataforma Project Server. 
    
- En [Comenzar con el modelo de objetos de JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) se muestra cómo desarrollar aplicaciones web que puedan obtener acceso a Project Server. 
    
- En [Comenzar con CSOM y .NET de Project Server](getting-started-with-the-project-server-csom-and-net.md) se muestra cómo usar el modelo de objetos de cliente para desarrollar aplicaciones, en lugar de los servicios de la PSI. 
    
- En [Aplicaciones del panel de tareas para Project Profesional](task-pane-add-ins-for-project.md) se presentan los complementos de Office, tal como se aplica a Project 2013. El SDK de Office 2013 incluye artículos que muestran cómo desarrollar aplicaciones del panel de tareas para Project y los demás clientes de Office 2013. 
    
- En [Crear un flujo de trabajo de Project Server para la administración de propuestas](create-a-project-server-workflow-for-demand-management.md) se muestra cómo se puede usar SharePoint Designer 2013 para crear flujos de trabajo de Project Server. 
    
- En [ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx) (ProjectData: referencia del servicio OData de Project) se incluye una introducción a la interfaz OData para crear informes de Project Server, además de temas de referencia XML para el servicio **ProjectData**. 
    
Los temas del espacio de nombres **Microsoft.ProjectServer.Client** y los nuevos métodos de los servicios de la PSI solo tienen la documentación mínima. La mayoría de los temas de referencia de los servicios de la PSI no se han modificado desde la versión de julio de 2011 del SDK de Project 2010. 
  
### <a name="future-sdk-releases"></a>Futuras versiones del SDK
<a name="pj15_Welcome_FutureReleases"> </a>

El SDK de Project 2013 se actualizará con nuevos artículos y contenido de referencia para la versión de disponibilidad general.
  
## <a name="sections-in-the-project-sdk"></a>Secciones del SDK de Project
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Hay dos secciones principales en el SDK de Project 2013:
  
- La sección [Artículos con conceptos e instrucciones de Project](project-conceptual-and-how-to-articles.md) contiene información general sobre las principales características y artículos con procedimientos detallados para el desarrollo. 
    
- La sección [Referencia de servicios web y biblioteca de clases de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) documenta el modelo de objetos de los ensamblados públicos, el ensamblado Microsoft.ProjectServer.Client.dll del CSOM y los servicios de la PSI. 
    
La sección **Artículos con conceptos e instrucciones** incluye lo siguiente: 
  
- En [Novedades y descartes para desarrolladores](updates-for-developers-in-project-2013.md) se describen las principales características de programación nuevas y las que han quedado en desuso en Project 2013. 
    
- En [Información general sobre Project para desarrolladores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) se incluyen artículos sobre la arquitectura de Project Server, artículos que muestran cómo comenzar a desarrollar con el CSOM, información sobre nuevas características de VBA para Project y una referencia al SDK de Office 2013, que contiene temas sobre el desarrollo de aplicaciones del panel de tareas para Project Profesional 2013. 
    
- En [Tareas de programación de Project](project-programming-tasks.md) se incluyen artículos de procedimientos sobre cómo crear aplicaciones para Project Server, usar JavaScript con el CSOM y crear propuestas de proyecto y flujos de trabajo para la administración de propuestas. 
    
- En [Referencias de programación de Project 2013](project-2013-programming-references.md) se incluye una introducción a la referencia de la PSI para Project Server 2013, información sobre los códigos de error de Project Server y la referencia del esquema OData para el servicio **ProjectData**. 
    
> [!NOTE]
>  A continuación se indican los requisitos para desarrollar e implementar aplicaciones y soluciones de EPM desde AppSource que se integren con Project Server 2013: > Debe instalar .NET Framework 4 o .NET Framework 4.5 en el equipo de desarrollo y en los equipos de implementación. Para determinar si ha instalado la versión correcta, abra **Programas y características** en el Panel de control de Windows. > Visual Studio 2012 instala y usa .NET Framework 4.5. Al crear un proyecto de Visual Studio, puede seleccionar **.NET Framework 4.0** o **.NET Framework 4.5** en la lista desplegable del cuadro de diálogo **Nuevo proyecto**. También puede seleccionar la **Versión de .NET Framework de destino** en la pestaña **Aplicación** de la ventana **Propiedades** del proyecto. > Puede usar Visual Studio 2010 para las aplicaciones que usan el CSOM o la PSI, así como para aplicaciones del panel de tareas de Project. En cambio, Visual Studio 2010 no contiene las plantillas de complementos de Office, las herramientas de desarrollo de Office ni las herramientas de desarrollo de SharePoint para Office 2013. Para descargar Visual Studio 2012 y el instalador de plataforma web (WebPI) que incluye las herramientas de desarrollo de Office y SharePoint, vea [Downloads for Apps for Office and SharePoint](https://msdn.microsoft.com/office/apps/fp123627) (Descargas de aplicaciones para Office y SharePoint). > Le recomendamos que desarrolle soluciones personalizadas en un entorno de prueba. Si desarrolla soluciones para las compilaciones actuales de Project Server 2013 y Project 2013, debe volver a compilarlas con referencias actualizadas y puede que tenga que hacer cambios adicionales para que funcionen con versiones posteriores. Es posible que las soluciones desarrolladas para cualquier versión preliminar no funcionen con la versión de lanzamiento. 
  
## <a name="see-also"></a>Vea también
<a name="pj15_Welcome_AR"> </a>

- [Actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)
    
- [Arquitectura de Project Server 2013](project-server-2013-architecture.md)
    
- [Descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SDK de componentes cliente de SharePoint Server 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project para desarrolladores](https://msdn.microsoft.com/project)
    
- [Documentación para desarrolladores de Office](https://msdn.microsoft.com/office)
    
- [Getting Started with Development for Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) (Introducción al desarrollo para Project 2010)
    
- [Convenciones de documentos](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Accesibilidad en SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Accesibilidad en Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/es-ES/privacystatement)
    

