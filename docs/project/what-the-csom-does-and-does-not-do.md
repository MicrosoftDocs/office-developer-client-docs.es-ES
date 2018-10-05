---
title: Lo que hace y lo que no hace el CSOM
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: El modelo de objetos de cliente (CSOM) es un conjunto de API para Project Server 2013 que están diseñados para ambos en línea y local usar en las aplicaciones que se pueden desarrollar para PC, dispositivos móviles y tabletas. En este artículo incluye algunos escenarios típicos para usar el CSOM y también se enumera las limitaciones del CSOM.
ms.openlocfilehash: ad9f9e0404cb0063a1c58c8e66a022372881a24f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399294"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Lo que hace y no hace CSOM

El modelo de objetos de cliente (CSOM) es un conjunto de API para Project Server 2013 que están diseñados para ambos en línea y local usar en las aplicaciones que se pueden desarrollar para PC, dispositivos móviles y tabletas. En este artículo incluye algunos escenarios típicos para usar el CSOM y también se enumera las limitaciones del CSOM.
  
|||
|:-----|:-----|
|||
   
El CSOM permite el desarrollo de aplicaciones para Project Server 2013 y la integración de Project Server con otras aplicaciones. Las aplicaciones se pueden desarrollar para ejecutar en los equipos, dispositivos móviles como Windows Phone 7.5, tabletas como dispositivos de Windows 8, iOS y dispositivos Android. El CSOM proporciona API que abarcan la funcionalidad de los doce con más frecuencia utilizan servicios PSI en Project Server. Las API de CSOM están organizadas de manera diferente y son más fáciles de usar que los servicios PSI basados en ASMX y WCF. El CSOM no usa conjuntos de datos ADO.NET y es accesible a través del Protocolo OData. Puede desarrollar con el CSOM mediante el uso de bibliotecas de .NET Framework 4, JavaScript, o las consultas de Representational State Transfer (REST).
  
Para obtener información general de los artículos que muestran cómo usar JavaScript y .NET Framework 4 con el CSOM y el CSOM, vea [modelo de objetos de cliente (COM) de Project Server](client-side-object-model-csom-for-project-2013.md). Para obtener más información acerca de los ensamblados CSOM, clases y miembros, vea la referencia de espacio de nombres [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="usage-scenarios-for-the-csom"></a>Escenarios de uso para el CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

A continuación se indican ejemplos de algunos tipos de aplicaciones que admite el CSOM. El CSOM se puede usar en lugar del PSI para numerosos escenarios:
  
- **Aplicaciones de desarrollar que ampliación Project Server** El propósito principal del CSOM es el desarrollo de aplicaciones para Project Server 2013, donde se pueden crear aplicaciones para una amplia variedad de dispositivos que incluyen equipos, dispositivos móviles y tabletas. Aplicaciones se pueden distribuir dentro de un catálogo de aplicaciones privado o en la tienda de Office pública. 
    
- **Automatice la creación o administración de entidades de Project Server** El CSOM puede realizar operaciones CRUD para entidades tales como proyectos, tareas, asignaciones, recursos de empresa, campos personalizados, tablas de búsqueda, los partes de horas, los controladores de eventos y fases de flujo de trabajo y etapas. A menudo hay casos donde una aplicación personalizada puede ahorrar tiempo con masiva o las tareas repetitivas. 
    
- **Obtener datos en las tablas de la base de datos de proyecto publicados** Como base de datos directa el acceso a la borrador, publicada y archivar las tablas no es compatible, puede usar el CSOM para leer datos que no está disponibles en las tablas o vistas de informes. Por ejemplo, obtenga información sobre las etapas de flujo de trabajo, fases y actividades. Para leer datos en las tablas de informes, puede utilizar las consultas de OData. 
    
- **Validar los datos de estado y partes de horas** Use el CSOM en controladores de eventos locales o receptores de eventos remotos para eventos anteriores para validar los datos de estado o partes de horas de asignación que los usuarios escribir, antes de que los datos se guardan en Project Web App. 
    
- **Crear proyectos financieros** Creación de proyectos para captura de tiempo a través de la parte de horas para la integración con un sistema financiero. Crear una jerarquía de códigos financieros que reflejen la estructura de desglose de costos del sistema financiero. Proyectos financieros no requieren actualizaciones de estado o programación. 
    
- **Integrar con sistemas de contabilidad** Capturar los costos de recursos y los gastos asociados con proyectos de fuente sistemas financieros y de facturación y con fines de comparación de presupuesto. Sincronizar las tareas, recursos y asignaciones entre los sistemas. Capturar datos del parte de horas en un sistema a la otra fuente (se usa el parte de horas depende de las necesidades de la organización o de proyectos individuales). 
    
- **Actualizaciones de automatizar los miembros del equipo** Para los proyectos que no se administran activamente, actualice automáticamente proyectos en el servidor con progreso y otros cambios de los miembros del equipo de proyecto. Proyectos se pueden actualizar y volver a publicar sin un jefe de proyecto revisar los resultados o realice ajustes en el plan. 
    
    > [!NOTE]
    > El CSOM es compatible con el envío de actualizaciones de estado, pero actualmente no es compatible con las aprobaciones de estado. 
  
- **Datos de evaluación de Project Server en receptores de eventos remotos** Un receptor de eventos remotos para un evento previo **ProjectCreating** puede usar datos de Project Server desde el CSOM para ayudar a determinar si se debe cancelar el evento. Por ejemplo, antes de crear un proyecto, compare la propuesta de proyecto con proyectos existentes. 
    
- **Flujos de trabajo de Project Server declarativos soporte técnico** El CSOM permite que los flujos de trabajo de Project Server que se crean en SharePoint Designer 2013. El CSOM es compatible con las definiciones de flujo de trabajo que usan Windows Workflow Foundation versión 4 (WF4). (La PSI no admite flujos de trabajo de WF4). 
    
- **Crear flujos de trabajo de Project Server complejos** Al desarrollar flujos de trabajo con Visual Studio 2012, puede usar el CSOM para acciones complejas dentro de las etapas de flujo de trabajo o crear acciones de flujo de trabajo personalizado. 
    
## <a name="what-the-csom-does-not-do"></a>Lo que CSOM no hace
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

El CSOM no es un reemplazo completo para la PSI. Debido a que el CSOM internamente utiliza los servicios PSI, el CSOM tiene muchas de las mismas limitaciones funcionales que tiene la PSI. Además de las limitaciones de la PSI, como no tener ningún acceso a los datos en proyectos locales (archivos .mpp), el CSOM no incluye funciones administrativas que normalmente controla Project Web App. Por ejemplo, la creación de grupos de seguridad personalizados puede controlarse en la página Configuración del sitio - permisos de Project Web App. 
  
Para obtener una lista de acciones que controlan la PSI ni CSOM, vea la sección *PSI no hace* en [What the PSI hace y no hace](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Servicios de PSI que no abarca el CSOM
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

El CSOM no incluye funciones de los siguientes servicios de PSI:
  
- **Servicio de administración** Para administrar la configuración administrativa y las operaciones en Project Server y para los sitios de proyecto relacionadas, como la creación de períodos fiscales y realizar la configuración del parte de horas, use los métodos PSI en la clase [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) . Project Web App propio usa los métodos de **administración** en muchas de las páginas que están vinculadas a la página Configuración del servidor (https:// *nombreDeServidor*  /  *ProjectServerName* /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Servicio de archivado** Para guardar y administrar entidades tales como proyectos, recursos y campos personalizados en las tablas de archivado, usan los métodos PSI en la clase de [archivo](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) . 
    
- **Servicio CubeAdmin** Para crear y administrar cubos OLAP para instalaciones locales, use los métodos PSI en la clase [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) o use la página de administración de bases de datos OLAP (https:// *nombreDeServidor*  /  *ProjectServerName* /_layouts/15/pwa / CubeAdmin/CubeAnalysisAdmin.aspx) en Project Web App. 
    
    > [!NOTE]
    > Project Online no es compatible con los cubos OLAP. 
  
- **Servicio de controlador** Para crear y administrar impulsores de negocios para análisis de cartera de proyectos, use los métodos PSI en la clase [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) . 
    
- **Servicios de LoginForms y LoginWindows** Se realiza la autenticación en el CSOM durante la inicialización del objeto de **ProjectContext** , con la autenticación de Windows o de OAuth. Para crear aplicaciones para autenticación múltiple, donde una aplicación de plena confianza local puede usar la autenticación de formularios y la autenticación de Windows, use los métodos PSI en la clase [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) y la [ WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) clase. 
    
- **Servicio de notificación** Para crear y administrar las alertas y avisos, use los métodos PSI en la clase [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) . 
    
- **Servicio ObjectLinkProvider** Para crear y administrar objetos web y vínculos a documentos y elementos de lista de SharePoint, use los métodos PSI en la clase [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) . 
    
- **Servicio PortfolioAnalyses** Para crear y administrar análisis de cartera de proyectos, incluidas soluciones de planificador y las soluciones del optimizador, use los métodos PSI en la clase [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) . 
    
- **Servicio de QueueSystem** El CSOM puede obtener información básica acerca de los trabajos de cola de Project Server e incluye el método [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx) . Para la administración más exhaustiva del sistema de puesta en cola de Project Server, use los métodos PSI en la clase [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) . 
    
- **Servicio de seguridad** Para crear y administrar categorías, plantillas y grupos de seguridad de Project Server y para comprobar los permisos para el usuario actual, use los métodos PSI en la clase [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) . 
    
- **Servicio WssInterop** Para obtener información acerca de y administrar sitios de proyecto, use los métodos PSI en la clase [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) . 
    
    > [!NOTE]
    > Puede usar el CSOM en SharePoint Server 2013. Sitios de proyecto son sitios de SharePoint. 
  
El CSOM no habilita extensiones como las que puede tener el PSI. Por ejemplo, si crea una extensión de PSI para uso local, el CSOM no se puede modificar para usar dicha extensión. Puede implementar escenarios de extensión de otros modos:
  
- Agregue llamadas CSOM dentro de un componente local o de un componente que se ejecuta en Microsoft Azure.
    
- Use consultas OData de los datos del informe, en lugar de obteniendo acceso directamente a las tablas de informes en la base de datos de Project Server.
    
- Integre llamadas del CSOM con aplicaciones de otros fabricantes a través de la autenticación de OAuth de Project Online o con componentes de servidor para uso local.
    
- Las aplicaciones que usan el CSOM también pueden usar bases de datos personalizadas en modo local o con SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Límites de solicitudes del CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

El CSOM en Project Server 2013 se basa en la implementación de CSOM en SharePoint Server 2013 y hereda los límites para el tamaño máximo de una solicitud. SharePoint tiene un límite de 2 MB para una solicitud de operaciones y un límite de 50 MB para el tamaño de un objeto binario enviado. El tamaño de la solicitud se limita a proteger el servidor de las colas excesivamente largos de operaciones y de procesamiento retrasos para objetos binarios grandes.
  
Por ejemplo, si usa el CSOM para crear un proyecto y edita a continuación el proyecto para añadir 252 tareas con una cantidad de información mínima, tal como un nombre corto, el GUID de tarea y una duración de 1d, la cantidad total de datos en la solicitud de **DraftProject.Update** es inferior a 2 MB. Pero si trata de añadir 253 de dichas tareas a un proyecto vacío, se superará el límite de 2 MB y obtendrá la siguiente excepción: **Microsoft.SharePoint.Client.ServerException: La solicitud utiliza demasiados recursos.**
  
Para capturar los datos en una solicitud CSOM a través de HTTP o HTTPS, puede usar una herramienta como [Fiddler](https://www.fiddler2.com) de depuración de web (https://www.fiddler2.com). Para obtener un ejemplo de código que implementa una prueba para el tamaño de la solicitud e incluye una solución que se interrumpe una solicitud de gran tamaño en a grupos más pequeños, vea [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Vea también
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modelo de objeto de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Lo que hace y no hace PSI](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

