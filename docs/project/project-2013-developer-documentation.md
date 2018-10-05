---
title: Documentación para desarrolladores de Project 2013
manager: soliver
ms.date: 04/04/2016
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
- SDK, información general SDK de project 2013, Project 2013,
localization_priority: Normal
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Busque documentación, ejemplos de código, artículos de procedimientos y referencias de programación para ayudar a crear aplicaciones para la tienda de Office o en un catálogo de aplicaciones privada y para personalizar e integrar Project Server y los clientes de Project con una amplia variedad de otros profesionales y de escritorio aplicaciones para la administración de proyectos empresariales.
ms.openlocfilehash: 887b5964d6fa0e4845156e13c7f49a399543c133
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398230"
---
# <a name="project-2013-developer-documentation"></a>Documentación para desarrolladores de Project 2013

Busque documentación, ejemplos de código, artículos de procedimientos y referencias de programación para ayudar a crear aplicaciones para la tienda de Office o en un catálogo de aplicaciones privada y para personalizar e integrar Project Server y los clientes de Project con una amplia variedad de otros profesionales y de escritorio aplicaciones para la administración de proyectos empresariales.
  
Bienvenido a la de Microsoft Project el Kit de desarrollo de Software (SDK) de 2013. El SDK contiene documentación, ejemplos de código, artículos de procedimientos y referencias de programación para ayudar a crear aplicaciones para un almacén público o el catálogo de aplicaciones privada y para personalizar e integrar de Project Server y los clientes de Project con una amplia variedad de otro escritorio y aplicaciones empresariales para la administración de proyectos empresariales.
  
> [!NOTE]
> Project Server 2013 se basa en la plataforma SharePoint Server 2013 y Project 2013 incluye gran parte de la misma estructura que las otras aplicaciones de Office 2013. Para obtener documentación sobre el modelo para SharePoint Add-ins, los flujos de trabajo basado en SharePoint, elementos Web, desarrollo con otras características de SharePoint y la documentación de complementos de Office, vea [SharePoint complementos](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) y [complementos de Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins). 
  
## <a name="introduction-to-the-project-sdk"></a>Introducción al SDK de Project
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 es una plataforma para la creación de soluciones de administración de proyectos local o empresa basados en la nube y la creación de aplicaciones que los usuarios finales pueden detectar y adquirir a través de un almacén público o un catálogo de aplicaciones privada. La arquitectura de Project Server 2013 se basa en la plataforma en Microsoft Office Project Server 2007, con muchas mejoras y adiciones. Las nuevas características incluyen un modelo de objetos de cliente (COM) para permitir el acceso a Project Online, un servicio de OData para acceso en línea a informes de datos, receptores de eventos remotos, arquitectura de flujo de trabajo que se basa en la versión 4 del flujo de trabajo de Windows de Project Server Foundation (WF4) y Office Add-ins, que es una arquitectura común para las extensiones del panel de tareas en las aplicaciones cliente de Microsoft Office 2013.
  
Un cambio importante en Project Server 2013 es el uso de una sola base de datos en lugar de las bases de datos de borrador, publicados, archivo e informes en Project Server 2010. Para obtener más información acerca de las nuevas características y las características en desuso, vea [actualizaciones de programadores de Project 2013](updates-for-developers-in-project-2013.md). Para obtener información acerca de los cambios en la plataforma de Project Server, consulte [arquitectura de Project Server 2013](project-server-2013-architecture.md). Para obtener información general de la plataforma de desarrollo que existe en Project Server 2010 y Project Server 2013 basado en, vea [Introducción al desarrollo para Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) en MSDN. 
  
Project Server 2013 se basa en el Microsoft .NET Framework 4 y Microsoft SharePoint Server 2013. Los artículos y ejemplos en este SDK proporcionan un punto de partida para el desarrollo de soluciones personalizadas y aplicaciones; no tratan todas las características de programación de Project Server o Project Professional. El [Centro de desarrolladores de Project](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) incluye vínculos a artículos Project, blogs, vídeos, difusiones por Web, artículos de procedimientos visual y otros recursos. 
  
El SDK de Project 2013 incluye información para desarrolladores de Project Server 2013, Project Web App, Project Professional 2013 y Project Standard 2013. Los artículos SDK están diseñados para ayudar a los desarrolladores y administradores de evaluación de Project y Project Server para ofrecer extensibilidad y planeación de soluciones personalizadas.
  
### <a name="feedback"></a>Comentarios
<a name="pj15_Welcome_Feedback"> </a>

Nos gustaría conocer su opinión. En los temas en línea en MSDN, puede agregar comentarios, ejemplos de código, o marcar el contenido como un error en la sección **Contenido de la Comunidad** en la parte inferior de cada página. Cuando instala la descarga del SDK de Project 2013, los artículos de la documentación local tienen un vínculo *Enviar comentarios* que se encuentra debajo del título. En cualquier momento en el SDK de lectura, elija el vínculo para enviar un correo electrónico al equipo del SDK. Puede enviar las correcciones, una solicitud de aclaración o un ejemplo de código u otros comentarios y nos ayudará a que el contenido más potente. 
  
### <a name="download"></a>Descarga
<a name="pj15_Welcome_Download"> </a>

La descarga del SDK de Project 2013 está disponible en el [Centro de descarga de Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). La descarga incluye Project2013SDK.HxS (el archivo que se incluye en este artículo), relacionados con ejemplos de código, ensamblados redistribuibles y otros recursos. El SDK de Project 2013 aún no incluye la referencia de tablas de datos de informes.
  
### <a name="whats-new-in-the-project-sdk"></a>Novedades del SDK de Project
<a name="pj15_Welcome_WhatsNew"> </a>

El propósito principal de SDK de Project 2013 es proporcionar una visión general de la programación y la documentación de la CSOM y características relacionadas para la creación de aplicaciones, los servicios de Project Server Interface (PSI) y aplicaciones de panel de tareas de Project Professional 2013. El SDK de Project 2013 incluye ejemplos paso a paso de áreas clave para la personalización de Project Server 2013 y los clientes de proyecto (Project Standard 2013, Project Professional 2013 y Project Web App). La documentación está incompleta; se agregarán más contenido en versiones posteriores. 
  
La tecnología subyacente para la comunicación de red es Windows Communication Foundation (WCF) en Project Server 2013, incluidos los escenarios de nube que usan el CSOM de Project Server y desarrollo local mediante la interfaz PSI. Las referencias de servicio web de ASMX heredadas también se basan en la arquitectura de WCF. Establecer una referencia a un servicio web PSI (archivo ASMX) en Project Server 2013 requiere anexando la `?wsdl` opción de dirección URL a la ruta de acceso. Por ejemplo, `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Aunque resuelve sólo se utiliza con más frecuencia a las características de Project Server, se recomienda que use el CSOM siempre que sea posible para aplicaciones tanto local y en la nube. Si bien se sigue estando disponible en Project Server 2013, la interfaz ASMX para la PSI está en desuso. Para las aplicaciones locales que requieren acceso total a la PSI, debe usar la interfaz WCF para la interfaz PSI, en lugar de la interfaz ASMX. 
  
Desarrollo en un equipo con Windows 7 es compatible con copiar los ensamblados CSOM de Project Server 2013 y SharePoint Server 2013 en el equipo de desarrollo. La descarga del SDK incluye los ensamblados CSOM de Project Server y una licencia de redistribución. Para obtener el CSOM de SharePoint los ensamblados, vea [SDK de componentes de cliente de SharePoint Server 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Para el desarrollo con los servicios WCF, puede establecer una referencia a un ensamblado proxy de PSI o agregar archivos proxy de PSI a la solución. Puede establecer referencias directas a los servicios web ASMX front-end de Project Server desde un equipo remoto del mismo dominio o usar un ensamblado proxy o archivos proxy. La descarga del SDK incluye archivos proxy para los servicios web WCF y ASMX, además de scripts para crear los ensamblados proxy y para generar archivos proxy actualizados.
  
En Project Server 2013, puede crear flujos de trabajo declarativos en Project Server mediante Microsoft SharePoint Designer 2013, tanto local y usar en línea. SharePoint Designer 2013 usa los métodos y propiedades de actividad de flujo de trabajo en el CSOM. Desarrollo e implementación de soluciones de Visual Studio 2012 que incluyen elementos Web de Project Server o las personalizaciones de Project Web App, sólo se admite en un equipo de Project Server.
  
Para obtener información general de las nuevas características de programación y las características desusadas en Project Server 2013, vea [actualizaciones de programadores de Project 2013](updates-for-developers-in-project-2013.md). Otro cambio importante en Project Server 2013 es el uso de flujos de trabajo basados en WF4 para administrar la creación y aprobación de propuestas de proyectos que se basan en plantillas de proyecto de empresa. 
  
Los nuevos temas incluyen lo siguiente:
  
- [Crear un servidor de Project Server hospedada en SharePoint complemento](create-a-sharepoint-hosted-project-server-add-in.md) se muestra cómo usar Visual Studio para el desarrollo remoto de una aplicación que puede usarse con Project Server 2013 y Project Online. 
    
- [Project Server 2013 architecture](project-server-2013-architecture.md) explica las características principales nuevas de la plataforma Project Server. 
    
- [Getting started with el modelo de objetos de JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) muestra cómo desarrollar aplicaciones web que se pueden obtener acceso a Project Server. 
    
- [Getting started con Project Server CSOM y .NET](getting-started-with-the-project-server-csom-and-net.md) se muestra cómo usar el modelo de objetos de cliente para desarrollar aplicaciones, en lugar de usar los servicios de PSI. 
    
- [Aplicaciones de panel de tareas para Project Professional](task-pane-add-ins-for-project.md) presenta Office Add-ins, tal como se aplica a Project 2013. El SDK de Office 2013 incluye artículos que muestran cómo desarrollar aplicaciones de panel de tareas de proyecto y otros clientes de Office 2013. 
    
- [Crear un flujo de trabajo de Project Server para la administración de propuestas](create-a-project-server-workflow-for-demand-management.md) se muestra cómo se puede usar SharePoint Designer 2013 para crear flujos de trabajo de Project Server. 
    
- [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/library/office/jj163015.aspx) incluye información general de la interfaz de OData para informes de Project Server, además de temas de referencia XML para el servicio **ProjectData** . 
    
Los temas en el espacio de nombres **Microsoft.ProjectServer.Client** y nuevos métodos en los servicios de PSI tienen sólo una documentación mínima. La mayoría de los temas de referencia para los servicios PSI se ha modificado desde la versión de julio de 2011 de SDK de Project 2010. 
  
### <a name="future-sdk-releases"></a>Futuras versiones del SDK
<a name="pj15_Welcome_FutureReleases"> </a>

El SDK de Project 2013 se actualizará con nuevos artículos y contenido de referencia para la versión de la disponibilidad general.
  
## <a name="sections-in-the-project-sdk"></a>Secciones del SDK de Project
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Hay dos secciones de nivel superior en el SDK de Project 2013:
  
- La sección de [artículos con conceptos e instrucciones de proyecto](project-conceptual-and-how-to-articles.md) contiene información general sobre las características principales y artículos con procedimientos paso a paso para el desarrollo. 
    
- La sección de [referencia de servicio web y biblioteca de clases de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) documenta el modelo de objetos de los ensamblados públicos, el ensamblado Microsoft.ProjectServer.Client.dll para el CSOM y los servicios de PSI. 
    
La sección **Artículos conceptuales y de procedimientos** incluye lo siguiente: 
  
- [Novedades y ¿qué es para desarrolladores](updates-for-developers-in-project-2013.md) describe las principales nuevas características de programación y características en Project 2013 en desuso. 
    
- [Información general de Project para desarrolladores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) se incluyen artículos acerca de la arquitectura de Project Server, artículos que muestran cómo obtener una introducción al desarrollo con el CSOM, información acerca de las nuevas características de VBA para Project y una referencia al SDK de 2013 Office, que contiene temas sobre el desarrollo de aplicaciones de panel de tareas para Project Professional 2013. 
    
- [Tareas de programación de proyecto](project-programming-tasks.md) incluye artículos de procedimientos sobre la creación de aplicaciones de Project Server, uso de JavaScript con el CSOM y crear propuestas de proyectos y flujos de trabajo de administración de propuestas. 
    
- [Referencias de programación de Project 2013](project-2013-programming-references.md) incluye una introducción a la referencia de PSI de Project Server 2013, información acerca de los códigos de error de Project Server y la referencia del esquema OData para el servicio **ProjectData** . 
    
> [!NOTE]
>  A continuación se muestran los requisitos para desarrollar e implementar soluciones EPM y aplicaciones de la tienda de Office pública que se integren con Project Server 2013: > debe instalar .NET Framework 4 o .NET Framework 4.5 en el equipo de desarrollo y en la implementación equipos. Para determinar si está instalada la versión correcta, abra **programas y características** en el Panel de Control de Windows. > Visual Studio 2012 se instala y usa .NET Framework 4.5. Cuando se crea un proyecto de Visual Studio, puede seleccionar **.NET Framework 4.0** o **NET Framework 4.5** en la lista desplegable del cuadro de diálogo **Nuevo proyecto** . También puede seleccionar el **Marco de destino** en la ficha **aplicación** de la ventana de **Propiedades** del proyecto. > Puede usar Visual Studio 2010 para las aplicaciones que usan el CSOM o la interfaz PSI y para aplicaciones de panel de tareas de proyecto. Sin embargo, Visual Studio 2010 no contiene las plantillas de complementos de Office, herramientas de desarrollo de Office o herramientas de desarrollo de SharePoint para Office 2013. Para descargar Visual Studio 2012 y el instalador de plataforma Web (WebPI) que incluye las herramientas de desarrollo de Office y SharePoint, vea [descargas de aplicaciones para Office y SharePoint](https://msdn.microsoft.com/office/apps/fp123627). > Se recomienda que desarrollar soluciones personalizadas en un entorno de prueba. Si desarrolla soluciones para el actual compilaciones de Project Server 2013 y Project 2013, se deben volver a compilar con referencias actualizadas y es posible que necesite cambios adicionales, para que funcione con versiones posteriores. Soluciones desarrolladas para cualquier versión preliminar puede que no funcione con la versión de lanzamiento. 
  
## <a name="see-also"></a>Vea también
<a name="pj15_Welcome_AR"> </a>

- [Actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)
    
- [Project Server 2013 architecture](project-server-2013-architecture.md)
    
- [Descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SDK de componentes de cliente de SharePoint Server 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project para desarrolladores](https://msdn.microsoft.com/project)
    
- [Documentación para desarrolladores de Office](https://msdn.microsoft.com/office)
    
- [Introducción al desarrollo para Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [Convenciones de documentos](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Accesibilidad en SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Accesibilidad en Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Aviso de privacidad en línea de Microsoft](https://privacy.microsoft.com/en-us/privacystatement)
    

