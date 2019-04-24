---
title: Lo que hace y no hace CSOM
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: El modelo de objetos de cliente (CSOM) es un conjunto de varias API para Project Server 2013 diseñadas para ser usadas en línea y de forma local en aplicaciones que se pueden desarrollar para PC, tabletas y dispositivos móviles. Este artículo incluye escenarios típicos de uso de CSOM, así como las limitaciones de este.
localization_priority: Priority
ms.openlocfilehash: 6cdcb72c24e352365b6dcc9268ddf0bd249369af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315228"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Lo que hace y no hace CSOM

El modelo de objetos de cliente (CSOM) es un conjunto de varias API para Project Server 2013 diseñadas para ser usadas en línea y de forma local en aplicaciones que se pueden desarrollar para PC, tabletas y dispositivos móviles. Este artículo incluye escenarios típicos de uso de CSOM, así como las limitaciones de este.
  
|||
|:-----|:-----|
|||
   
El CSOM permite el desarrollo de aplicaciones para Project Server 2013 y la integración de Project Server con otras aplicaciones. Las aplicaciones se pueden desarrollar para ejecutarse en equipos, en dispositivos móviles como Windows Phone 7.5 y en tabletas como los dispositivos de Windows 8, además de en dispositivos iOS y Android. El CSOM proporciona API que cubren la funcionalidad de los doce servicios PSI más comunes en Project Server. Las API de CSOM están organizadas de manera diferente y son más fáciles de usar que los servicios PSI basados en WCF y ASMX. El CSOM no usa conjuntos de datos ADO.NET y es accesible mediante el protocolo de OData. Es posible desarrollar con el CSOM mediante el uso de las bibliotecas de .NET Framework 4, JavaScript o las consultas de Servicio Transferencia de estado representacional (REST).
  
Para obtener información general acerca del CSOM y artículos que muestran cómo usar JavaScript y .NET Framework 4 con el CSOM, consulte [Modelo de objeto de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md). Para más información sobre los ensamblados, clases y miembros del CSOM, consulte la referencia de espacio de nombres [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="usage-scenarios-for-the-csom"></a>Escenarios de uso para el CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

A continuación se indican ejemplos de algunos tipos de aplicaciones que admite el CSOM. El CSOM se puede usar en lugar de la PSI para numerosos escenarios:
  
- **Desarrollar aplicaciones que amplían Project Server** El principal objetivo del CSOM es el desarrollo de aplicaciones para Project Server 2013, donde pueden crearse aplicaciones para una amplia variedad de dispositivos, incluidos equipos, dispositivos móviles y tabletas. Las aplicaciones pueden distribuirse en un catálogo privado de aplicaciones o en la tienda pública Office Store. 
    
- **Automatizar la creación o administración de entidades en Project Server** El CSOM puede llevar a cabo operaciones CRUD para entidades tales como proyectos, tareas, asignaciones, recursos empresariales, campos personalizados, tablas de búsqueda, partes de horas, controladores de eventos y fases y etapas de flujos de trabajo. En muchos casos, una aplicación personalizada puede ahorrar tiempo con trabajos masivos o repetitivos. 
    
- **Obtener datos en las tablas publicadas de la base de datos de Project** Dado que no se admite el acceso directo de la base de datos a las tablas borrador, publicadas y de archivado, puede usar el CSOM para leer los datos que no están disponibles en las tablas o vistas de informes. Por ejemplo, puede obtener información acerca de etapas, fases y actividades del flujo de trabajo. Para leer datos en las tablas de informes, puede usar consultas OData. 
    
- **Validar datos de estado y partes de horas** Use el CSOM en gestores de eventos locales o en receptores de eventos remotos para preeventos para validar el estado de asignación o los datos de partes de horas que introduzca el usuario, antes de que los datos se guarden en Project Web App. 
    
- **Crear proyectos financieros** Cree proyectos para obtener tiempo mediante el parte de horas para la integración en un sistema financiero. Cree una jerarquía de códigos financieros que refleje la estructura de desglose de costes del sistema financiero. Los proyectos financieros no requieren actualizaciones de estado o programación. 
    
- **Integrar con sistemas de contabilidad** Obtenga los costes y gastos de los recursos relacionados con los proyectos para enviarlos a los sistemas financieros y de facturación, y para realizar comparaciones de presupuestos. Sincronice tareas, recursos y asignaciones entre los sistemas. Obtenga los datos del parte de horas en un sistema para enviarlos a otro (el parte de horas que se use dependerá de las necesidades de la organización o de proyectos individuales). 
    
- **Actualizar el proceso para integrantes del grupo** Si los proyectos no se administran de forma activa, actualícelos automáticamente en el servidor mediante el progreso y otros cambios de los integrantes del grupo del proyecto. Los proyectos se pueden actualizar y volver a publicar sin un jefe de proyecto que revise los resultados o realice ajustes en el plan. 
    
    > [!NOTE]
    > El CSOM admite enviar actualizaciones de estado, pero actualmente no es compatible con las aprobaciones de estado. 
  
- **Evaluar datos de Project Server en receptores de eventos remotos** Un receptor de eventos remoto para un preevento **ProjectCreating** puede usar datos de Project Server de CSOM para ayudar a determinar si cancela o no el evento. Por ejemplo, antes de crear un proyecto, compare la propuesta del proyecto con los proyectos existentes. 
    
- **Admitir flujos de trabajo declarativos de Project Server** El CSOM permite flujos de trabajo de Project Server creados en SharePoint Designer 2013. El CSOM es compatible con las definiciones de flujo de trabajo que usan Windows Workflow Foundation versión 4 (WF4). (La PSI no admite los flujos de trabajo WF4). 
    
- **Crear flujos de trabajo complejos de Project Server** Al desarrollar flujos de trabajo con Visual Studio 2012, puede usar el CSOM para acciones complejas en las etapas del flujo de trabajo o crear acciones de flujo de trabajo personalizadas. 
    
## <a name="what-the-csom-does-not-do"></a>Lo que no hace CSOM
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

El CSOM no puede sustituir por completo a la PSI. Dado que el CSOM usa internamente los servicios PSI, el CSOM comparte muchas de las limitaciones funcionales con la PSI. Además de las limitaciones de la PSI, como no tener acceso a los datos de los proyectos locales (archivos .mpp), el CSOM no incluye las funciones administrativas que normalmente controla Project Web App. Por ejemplo, la creación de grupos de seguridad personalizados se puede controlar desde la configuración del sitio, más específicamente, desde la página de permisos para Project Web App. 
  
Para obtener una lista de acciones que no gestionan ni PSI ni CSOM, consulte la sección *Lo que PSI no hace* en [Lo que hace y no hace PSI](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Servicios PSI que no cubre el CSOM
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

El CSOM no incluye la funcionalidad de los siguientes servicios PSI:
  
- **Servicio de administración** Para gestionar la configuración administrativa y las operaciones en Project Server y sitios de proyecto relacionados, como crear períodos fiscales y las opciones de configuración de parte de horas, use métodos de PSI de la clase [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx). Project Web App usa métodos **Administración** en muchas de las páginas que están vinculadas a la página Configuración del servidor (https://  *ServerName*  /  *ProjectServerName*  /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Servicio de archivado** Para guardar y administrar entidades tales como proyectos, recursos y campos personalizados en las tablas de archivado, use métodos PSI de la clase [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx). 
    
- **Servicio CubeAdmin** Para crear y administrar cubos OLAP para instalaciones locales, use métodos PSI en la clase [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) o use la página Administración de bases de datos OLAP (https://  *ServerName*  /  *ProjectServerName*  /_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) en Project Web App. 
    
    > [!NOTE]
    > Project Online no admite los cubos OLAP. 
  
- **Servicio de impulsores** Para crear y administrar impulsores de negocios para análisis de carteras de proyectos, use métodos PSI de la clase [T:WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx). 
    
- **Servicios LoginForms y LoginWindows** La autenticación en el CSOM se realiza durante la inicialización del objeto **ProjectContext**, con autenticación OAuth o Windows. Para crear aplicaciones para la autenticación múltiple, cuando una aplicación local de plena confianza puede usar tanto la autenticación de Formularios como la de Windows, use los métodos PSI de las clases [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) y [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx). 
    
- **Servicio de notificaciones** Para crear y administrar alertas y recordatorios, use métodos PSI de la clase [T:WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx). 
    
- **Servicio ObjectLinkProvider** Para crear y administrar objetos web y vínculos a documentos y elementos de lista de SharePoint, use métodos PSI de la clase [T:WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx). 
    
- **Servicio PortfolioAnalyses** Para crear y administrar análisis de la cartera de proyectos, incluidas soluciones de planificador y de optimizador, use métodos PSI de la clase [T:WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx). 
    
- **Servicio QueueSystem** El CSOM puede obtener información básica sobre los trabajos en cola de Project Server e incluye el método [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx). Para una administración más amplia del sistema de cola de Project Server, use métodos PSI de la clase [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx). 
    
- **Servicio de seguridad** Para crear y administrar los grupos de seguridad, las plantillas y las categorías de Project Server, así como para comprobar los permisos para el usuario actual, use métodos PSI de la clase [T:WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx). 
    
- **Servicio WssInterop** Para obtener información acerca de sitios de proyecto y administrarlos, use métodos PSI de la clase [T:WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx). 
    
    > [!NOTE]
    > Puede usar el CSOM en SharePoint Server 2013. Los sitios de proyecto son sitios de SharePoint. 
  
El CSOM no habilita extensiones como las que puede tener la PSI. Por ejemplo, si crea una extensión de PSI para uso local, el CSOM no se puede modificar para usar dicha extensión. Puede implementar escenarios de extensión de otros modos:
  
- Agregue llamadas CSOM dentro de un componente local o de un componente que se ejecute en Microsoft Azure.
    
- Use las consultas OData de datos de informes en lugar de acceder directamente a las tablas de informes de la base de datos de Project Server.
    
- Integre llamadas del CSOM con aplicaciones de terceros a través de la autenticación OAuth desde Project Online o con componentes del servidor para su uso local.
    
- Las aplicaciones que usan el CSOM también pueden usar bases de datos personalizadas de forma local o con SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Límites de solicitud del CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

En Project Server 2013, el CSOM se basa en la implementación del CSOM en SharePoint Server 2013 y hereda los límites de tamaño máximo de una solicitud. SharePoint tiene un límite de 2 MB para una solicitud de operaciones y un límite de 50 MB para el tamaño de un objeto binario enviado. El tamaño de la solicitud está limitado para proteger al servidor de colas de operaciones demasiado largas y de retrasos a la hora de procesar objetos binarios grandes.
  
Por ejemplo, si usa el CSOM para crear un proyecto y edita a continuación el proyecto para añadir 252 tareas con una cantidad de información mínima, tal como un nombre corto, el GUID de tarea y una duración de 1d, la cantidad total de datos en la solicitud de **DraftProject.Update** es inferior a 2 MB. Pero si trata de añadir 253 de dichas tareas a un proyecto vacío, se superará el límite de 2 MB y obtendrá la siguiente excepción: **Microsoft.SharePoint.Client.ServerException: La solicitud utiliza demasiados recursos.**
  
Para capturar los datos de una solicitud de CSOM sobre HTTP o HTTPS, puede usar una herramienta de depuración web como [Fiddler](https://www.fiddler2.com) (https://www.fiddler2.com). Para ver un ejemplo de código que implementa una prueba de tamaño de la solicitud e incluye una solución que divide una solicitud grande en grupos más pequeños, consulte [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Vea también
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modelo de objetos de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Lo que hace y no hace PSI](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

