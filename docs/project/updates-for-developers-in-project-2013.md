---
title: Actualizaciones para programadores de Project
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Las nuevas características incluyen un modelo de objetos de cliente (COM), interfaces REST, un servicio de OData para informes, receptores de eventos remotos, flujos de trabajo declarativos y complementos de panel de tareas para clientes de Project.
ms.openlocfilehash: e524fe7b8cfa813bd198e99a99cf77d6e2b1905d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567842"
---
# <a name="updates-for-developers-in-project"></a>Actualizaciones para programadores de Project

Características de extensibilidad de Project Server 2013 trabajar con complementos para Project Online y con instalaciones locales. Las nuevas características incluyen un modelo de objetos de cliente (COM), interfaces REST, un servicio de OData para informes, receptores de eventos remotos, flujos de trabajo declarativos y complementos de panel de tareas para clientes de Project. También Obtenga información acerca de las características en desuso que no se deben usar para el desarrollo de nuevas.
  
Project Server 2013 se basa en el marco de trabajo introducido en Microsoft Office Project Server 2007 y extiende con Project Server 2010. Project Server 2013 agrega un modelo de objetos de cliente (COM) que es refactorizar y simplificado de Project Server Interface (PSI) e incluye una biblioteca de JavaScript y las bibliotecas de .NET Framework 4 para aplicaciones de Windows, Windows Phone 8 y Microsoft Silverlight. El CSOM está diseñado para el desarrollo para Project Online y también funciona con una instalación de Project Server local. 

Las bases de datos de Project Server se combinan en una sola base de datos; puede tener acceso a las vistas y tablas de informes en línea a través de un servicio OData. El CSOM y el servicio de OData incluyen una interfaz de Representational State Transfer (REST). Flujos de trabajo de Project Server se pueden crear mediante el uso de SharePoint Designer 2013. Project Professional 2013 puede integrarse con informes de datos, listas de tareas de SharePoint y otro contenido externo mediante el modelo de extensibilidad de Office Add-ins para paneles de tareas de Project Server. Project Standard 2013 puede usar complementos de panel de tareas para integrar con contenido externo general.
  
Para obtener más información acerca de los principales cambios en Project Server 2013 y los diagramas, vea [arquitectura de Project Server 2013](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 se basa en la plataforma SharePoint Server 2013 y Project 2013 incluye gran parte de la misma estructura que las otras aplicaciones de Office 2013. Para obtener documentación sobre el modelo para SharePoint Add-ins, los flujos de trabajo basado en SharePoint, elementos Web, desarrollo con otras características de SharePoint y la documentación de complementos de Office, vea [SharePoint Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [complementos de Office](https://docs.microsoft.com/en-us/office/dev/add-ins/overview/office-add-ins)y SharePoint [ Introducción al desarrollo de 2013](http://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Principales características nuevas de Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Las nuevas características de Project Standard 2013 y Project Professional 2013 incluyen una interfaz de usuario mejorada que coincide con otras aplicaciones de Office 2013 y es compatible con la interfaz de usuario de estilo moderno en Windows 8, integración con objetos de Office Art para los informes, evolución informes y nuevas características de programación para los informes. Más amplio uso compartido y la sincronización de proyectos en SharePoint Server 2013, junto con la tarea panel complementos que también se implementan en otras aplicaciones de Office 2013, como Word, Excel y Outlook de Project Professional 2013 permite.
  
Hay muchas características nuevas en Project Server 2013. Algunos no tienen un artículo de programación principales, como la nueva escala de tiempo en Project Web App. Esas características se se documentan en la documentación de ayuda y del usuario final del producto en Microsoft Office Online y en temas dirigidos a los administradores y profesionales de TI en Microsoft TechNet. Otras características nuevas, como los partes de horas mejorada, facilitan a los programadores de terceros interactuar con los partes de horas y estado a través de Project Server Interface (PSI).
  
La adición de Project Online y la tienda de Office (http://office.microsoft.com/store) para complementos de proyecto son cambios de gran alcance, donde Project Server es accesible a través de Microsoft Azure. Acceso basado en la nube a Project Server usa un modelo de objetos de cliente (CSOM) para el desarrollo de complementos con Microsoft .NET Framework, Microsoft Silverlight, Windows Phone y aplicaciones web que usan JavaScript. Un requisito de Project Online es que las cuatro bases de datos de Project Server de versiones anteriores se combinan en una base de datos.
  
Escalabilidad y rendimiento de project Server 2013 se ha mejorado en muchas áreas como el estado de la tarea, los partes de horas y administración de proyectos. Flujos de trabajo de Project Server se han rediseñado con la versión 4 de Windows Workflow Foundation (WF4). Uso del .NET Framework 4 y Windows Communication Foundation (WCF) con la interfaz PSI mejora la seguridad, rendimiento y escalabilidad. Por ejemplo, puede cambiar el protocolo de transporte de aplicaciones basadas en WCF mediante el uso de los archivos de configuración, sin cambiar el código de la aplicación o volver a compilar. Muchas de las llamadas PSI donde datos no cambian significativamente cachés de Project Web App.
  
> [!NOTE]
> Para el desarrollo con Project Server 2013, puede usar Visual Studio con las extensiones de herramientas de Office y SharePoint, que pueden crear de forma nativa complementos para los productos de Office 2013. Project Server 2013 requiere Visual Studio habilitar totalmente el desarrollo de características, como páginas de detalles del proyecto y las aplicaciones basadas en WCF. Las extensiones de herramientas de SharePoint en Visual Studio pueden implementar elementos Web y otras características de SharePoint directamente en Project Web App y otros sitios de SharePoint. 
>
> Ya no se requiere Visual Studio para desarrollar flujos de trabajo de Project Server que utilizan los campos personalizados, las etapas, fases y tipos de proyecto empresarial que se pueden administrar en Project Web App. Aunque se puede usar Visual Studio para desarrollar flujos de trabajo, a menudo son más fácil y más rápidas crear mediante SharePoint Designer. Visual Studio puede usarse para los flujos de trabajo que requieren acceso a la CSOM u otras API externo. 
  
### <a name="project-add-ins"></a>Complementos para Project
<a name="pj15_WhatsNew_Apps"> </a>

Distribución y comercialización de software ha se han revolucionado con el concepto de un complemento. Para Project 2013, los complementos se pueden a disposición de compra y la descarga de la tienda de Office pública o distribuidos dentro de un catálogo privado en SharePoint. Un complemento es normalmente un programa interactivo, autocontenido que realiza un pequeño número de tareas relacionadas. Un complemento de Project puede ser un complemento de panel de tareas para los clientes de Project Standard 2013 o Project Standard 2013, o un complemento de Project Server 2013 o Project Online.
  
Para obtener información acerca de complementos para los clientes de escritorio de Project, vea [tareas panel complementos en el proyecto](#pj15_WhatsNew_Agave). Para obtener un ejemplo de Project Server 2013, vea [Agregar en crear un grupo de SharePoint-hosted Project Server](create-a-sharepoint-hosted-project-server-add-in.md). Además de los artículos de [Office y SharePoint Add-ins SDK](http://msdn.microsoft.com/library/fp161507.aspx), el [Blog de Office](https://blogs.office.com/dev/) tiene muchas entradas que también son relevantes para 2013 de Project y Project Online. 
  
Un complemento de Project Server 2013 puede trabajar con una instalación local y Project Online. Complementos de servidor de proyecto pueden incluir elementos Web, receptores de eventos remotos y lógica de negocios. Acceso al modelo de objetos de Project Server en un complemento es a través de CSOM, no la PSI. Almacenamiento de datos puede ser basados en la nube como SQL Azure, externo como a través de Microsoft conectividad servicios empresarial (BCS), interno con una base de datos local, o mixto.
  
#### <a name="add-in-security"></a>Complemento de seguridad

En general, se llevan a cabo acciones que un complemento realiza en nombre del usuario que se ejecuta el complemento; no explícitamente con suplantación o especificar quién puede ejecutar el complemento. Acciones no pueden superar el nivel de permisos del usuario que se ejecuta el complemento. 
  
En Office Developer Tools para Visual Studio 2012, el archivo AppManifext.xml tiene un editor gráfico donde puede establecer el ámbito de solicitud de permiso. Por ejemplo, para crear un complemento que permite a los jefes de proyecto actualizar sus proyectos, en la ficha **permisos** del panel Diseñador **AppManifest.xml** , seleccione **Varios proyectos** para el ámbito y **escribir** para el permiso. Si el usuario tiene permisos de administrador del proyecto, puede ejecutar el complemento para los proyectos que administra. El código en el archivo AppManifest.xml incluir lo siguiente: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabla 1. Ámbitos de solicitud de permisos para complementos de Project Server**

|Ámbito|Permisos|
|:-----|:-----|
|**Project Server** <br/> |**Administrar** (exige permisos de administrador de Project Server).  <br/> |
|**Varios proyectos** <br/> |**Leer**, **Escribir** (exige permisos de jefe de proyecto para algunas operaciones; permisos de miembro de equipo de proyecto para operaciones de lectura básicas, como asignaciones de tareas).  <br/> |
|**Único proyecto** <br/> |**Leer**, **Escribir** (exige al menos permisos de miembro de equipo de proyecto; el acceso a algunos datos de un proyecto depende de otros niveles de permisos).  <br/> |
|**Recursos empresariales** <br/> |**Leer**, **Escribir** (exige permisos de jefe de recursos).  <br/> |
|**Estado** <br/> |**SubmitStatus** (exige permiso para enviar el estado de los proyectos).  <br/> |
|**Informes** <br/> |**Leer** (exige permiso para iniciar sesión en Project Server).  <br/> |
|**Flujo de trabajo** <br/> |**Elevar** (exige permiso para ejecutar flujos de trabajo. El complemento se ejecuta con permisos elevados para permitir las transiciones de fase a fase en un flujo de trabajo. La lógica empresarial del complemento controla las transiciones de fase).<br/> |
   
> [!NOTE]
> Project Server 2013 y Project Online no usar el modelo de autenticación solo de aplicación en SharePoint 2013 (vea [Agregar en tipos de directiva de autorización en SharePoint 2013](http://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Para obtener información acerca de cómo desarrollar, distribuir, hospedar y administrar complementos, vea [SharePoint complementos](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins) y [complementos de Office](https://docs.microsoft.com/en-us/office/dev/add-ins/overview/office-add-ins)y otros temas relacionados en la documentación para desarrolladores de SharePoint Server 2013 y Office 2013. Para obtener información sobre el alcance de solicitud de permisos para otros complementos de SharePoint, vea [Add-in permissions in SharePoint 2013](http://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integración con SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Muchas características en Project Web App requieren la nueva infraestructura de SharePoint Server 2013 como OAuth y la autenticación basada en notificaciones, autorización de Project Server y los permisos a través de grupos de SharePoint, sincronización de proyectos con tareas de SharePoint listas y flujos de trabajo declarativos de Project Server. La aplicación de servicio de Project puede asociarse con cualquier colección de sitios en una granja de servidores de SharePoint. Sincronización de Project puede ser con una lista de tareas de SharePoint, donde SharePoint Team Services mantiene el proyecto. Un proyecto de empresa también puede sincronizarse con una lista de tareas de SharePoint, donde Project Server mantiene el control total. Para obtener una explicación de la sincronización del proyecto y los diagramas de arquitectura, vea [arquitectura de Project Server 2013](project-server-2013-architecture.md).
  
Hay muchas características nuevas en SharePoint Server 2013. Para obtener más información, vea [SharePoint para desarrolladores](http://msdn.microsoft.com/en-US/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integración con flujos de trabajo
<a name="pj15_WhatsNew_Workflow"> </a>

Los flujos de trabajo son una característica fundamental de la administración de la cartera de proyectos. El ciclo de vida de un proyecto puede incluir procesos a largo plazo que comprenden muchas fases. Las fases de gobernanza incluyen las propuestas, los análisis de impacto empresarial y la selección, creación, planeación, administración y el seguimiento de los proyectos.
  
Flujos de trabajo de Project Server 2013 se basan en la plataforma de flujo de trabajo de SharePoint 2013, que usa WF4. A diferencia de en versiones anteriores, flujos de trabajo declarativos para Project Server 2013 pueden crearse mediante el uso de SharePoint Designer 2013 y son accesibles para uso en línea y local. Flujos de trabajo de Project Server usa el modelo de seguridad de flujo de trabajo de SharePoint con OAuth y se pueden instalar en un sitio de Project Web App. La figura 1 muestra que SharePoint Designer 2013 puede agregar fases a un flujo de trabajo para la administración de propuestas, donde se definen las etapas en Project Web App.
  
**Ilustración 1. Uso de SharePoint Designer para agregar una fase a un flujo de trabajo de Project Web App**

![Adición de una fase a un flujo de trabajo en SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adición de una fase a un flujo de trabajo en SPD")

<br/>

Crear un flujo de trabajo declarativo mediante la adición de fases de flujo de trabajo, acciones, condiciones y otros elementos en una herramienta de diseño, que puede ser SharePoint Designer 2013 o Visual Studio 2012. La herramienta de diseño, a continuación, guarda el flujo de trabajo como código XAML, que se interpreta en tiempo de ejecución. Pueden ejecutar flujos de trabajo declarativos en Project Server 2013 local o en Project Online. Mediante el uso de Visual Studio 2012, también puede crear acciones personalizadas y formularios para un control adicional y guardar plantillas de flujo de trabajo para su reutilización con varias instancias de Project Web App. SharePoint Designer 2013 puede consumir acciones personalizadas que se crean en Visual Studio 2012.
  
Un flujo de trabajo de Project Server 2013 actúa como una aplicación, donde un administrador: quién tiene permisos de diseño para Project Web App, puede publicar un flujo de trabajo declarativo y asociarlo con un tipo de proyecto empresarial (EPT). El EPT debe ser para un proyecto de empresa, donde Project Server mantiene el control total. Una lista de tareas de SharePoint no puede usar un flujo de trabajo de Project Server. 
  
OAuth permite a los jefes de proyecto que tienen permisos de creación de proyecto para invocar el flujo de trabajo sin usar suplantación. Las llamadas de flujo de trabajo a Project Server, por ejemplo, para leer un valor de campo personalizado para decidir la rama que debe seguir, se realizan en nombre del jefe de proyecto. Para evitar que el jefe de proyecto de la creación de un flujo de trabajo que avanza automáticamente a la siguiente fase, la llamada para pasar a la siguiente etapa de flujo de trabajo se ejecuta como el autor del flujo de trabajo (el administrador). Por el contrario, los usuarios de flujos de trabajo de Project Server 2010 heredados realizan llamadas suplantadas a través de la cuenta de usuario de Proxy de flujo de trabajo para tener acceso de administrador a lo largo de todo el flujo de trabajo.
  
Aunque Project Server 2013 local puede usar compilados flujos de trabajo basados en WF3.5, se recomienda que actualice los flujos de trabajo heredados a flujos de trabajo declarativos basados en WF4. La tecnología más reciente es más escalable y sólida. Los analistas de negocios y el personal PMO puede crear o actualizar los diseños de flujo de trabajo mediante el uso de Visio 2013 e implementar flujos de trabajo de Project Server sin codificación mediante el uso de SharePoint Designer 2013.
  
Para obtener información acerca de cómo crear un flujo de trabajo declarativo para Project Web App, consulte [Getting started desarrollar flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md). Para obtener una comparación de SharePoint Designer y capacidades de Visual Studio para flujos de trabajo, vea [los flujos de trabajo de desarrollo de SharePoint 2013 con Visual Studio](http://msdn.microsoft.com/en-us/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modelo de objetos del lado cliente
<a name="pj15_WhatsNew_CSOM"> </a>

Acceso mediante programación a Project Online requiere un CSOM que se basa en el CSOM de SharePoint. Autenticación de Project Online será con OAuth con un Windows Live ID, la autenticación de formularios de Project Server no o la autenticación de Windows.
  
A continuación se muestran los principios y características del CSOM en Project Server 2013:
  
- El CSOM está diseñado para facilitar su uso. Por ejemplo, los métodos y propiedades directamente usarán o proporcionan datos por nombre, en lugar de requerir muchos GUID, _changeXml_ parámetros o pasando alrededor de los conjuntos de datos. 
    
- El CSOM de Project Server implementa un subconjunto de la funcionalidad de PSI basado en los requisitos más comunes de las soluciones de terceros.
    
- El CSOM llama internamente a PSI, pero se factoriza de forma distinta. Por ejemplo, las actualizaciones de todos los cambios de estado se realizan con el método **StatusAssignmentCollection.SubmitAllStatusUpdates**, no con el método de PSI **Statusing.SubmitStatus** del usuario ni el método **SubmitStatusForResource** de otros recursos. 
    
- El CSOM es accesible a través de un servicio WCF (Client.svc) en lugar de a través de los 22 servicios públicos de PSI.
    
- La inicialización del CSOM de Project Server directamente a través de la clase de [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) con la dirección URL de Project Web App, no es mediante el uso de un ensamblado de referencia o el proxy WCF. 
    
- El CSOM implementa varias bibliotecas de cliente e interfaces, que son compatibles con la infraestructura interna del CSOM de SharePoint. Las bibliotecas de cliente e interfaces son las siguientes:
    
  - Biblioteca de cliente de Microsoft .NET del ensamblado Microsoft.ProjectServer.Client.dll
    
  - Biblioteca de Silverlight en el ensamblado de Microsoft.ProjectServer.Client.Silverlight.dll
    
  - Biblioteca de Windows Phone 8 del ensamblado Microsoft.ProjectServer.Client.Phone.dll
    
  - Biblioteca de JavaScript para aplicaciones web en el archivo PS.js o el archivo PS.debug.js
    
  - Extremos REST, para el acceso con el protocolo OData
    
  - Compatibilidad nativa con consultas LINQ con filtrado para limitar la cantidad de datos devueltos
    
- El CSOM puede usarse para soluciones de Project Online y para las soluciones locales, independientemente de la PSI y otros ensamblados de Project Server, como Microsoft.Office.Project.Server.Library.dll.
    
- Funciones adicionales de Project Server 2013 CSOM pueden considerarse de actualizaciones acumulativas y service packs, en función de las solicitudes de los socios de Project Server y la Comunidad de desarrolladores.
    
> [!NOTE]
> El CSOM es la interfaz preferida por los desarrolladores ajenos de Project Server. Le recomendamos que use el CSOM para desarrollar nuevas aplicaciones, si es que incluye las características que la aplicación necesita. 
  
Para obtener información sobre el desarrollo con el CSOM, vea [modelo de objetos de cliente (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). Para obtener información acerca de la interfaz REST en las aplicaciones de SharePoint, vea *programar con el servicio REST de SharePoint* en la documentación para desarrolladores de SharePoint 2013. 
  
### <a name="changes-in-the-reporting-database"></a>Cambios en la base de datos de informes
<a name="pj15_WhatsNew_RDBChanges"> </a>

Las cuatro bases de datos de Project Server 2010 se combinan en una sola base de datos de proyecto en Project Server 2013. El nombre predeterminado de la base de datos de proyecto es ProjectService. Informes de tablas y vistas conservan sus nombres anteriores, y las tablas y vistas de las bases de datos de borrador, publicados y de archivo tienen los prefijos `draft`, `pub`, y `ver` en la base de datos ProjectService. Por ejemplo, la tabla de proyectos publicados es pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Dirigir acceso no es compatible con el borrador (`draft` prefijo), publicado (`pub`) y de archivo (`ver`) tablas y vistas. Deben usar informes sólo las tablas y vistas, que tienen informes la `dbo` prefijo. Por ejemplo, dbo. Tabla MSP_EpmProject incluye la lista de proyectos en la instancia de Project Web App. 
>
> No hay nada que le impida usar el acceso directo mediante programación a la base de datos para actualizar datos en cualquiera de las tablas y vistas de la base de datos de Project. Debería tener en cuenta que la caché de Project Professional, las tablas de datos de borrador y publicados y las tablas de informes se basan en un protocolo de sincronización de la caché que se puede alterar por la edición directa de datos. Si daña las bases de datos de Project Server o las cachés del lado cliente de Project Professional usando el acceso directo para cambiar datos, no obtendrá ayuda alguna del servicio de soporte del producto. 
  
Project Server 2013 presenta un servicio OData para en línea y local de acceso. Las tablas de informes en línea y vistas se exponen sólo por la interfaz de OData; para su uso local, puede usar la interfaz de OData o tener acceso directamente a las tablas de informes y vistas en la base de datos de ProjectService en la granja de servidores de SharePoint. Project Online no es compatible con una base de datos de varios inquilinos. Es decir, varias instancias de proyecto de aplicación Web cada tienen su propia base de datos de Project. El servicio de OData internamente ejecuta consultas SQL en las tablas y vistas de informes y ofrece una carga XML o JSON. Para obtener una introducción al servicio de OData para la creación de informes en Project Server 2013 y para la referencia del esquema **ProjectData** , consulte [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
Para obtener información general acerca de las consultas de OData, vea [OData: convenciones URI](https://www.odata.org/documentation/). Por ejemplo, puede ver todos los proyectos en una instancia local de Project Web App, donde el nombre del proyecto comienza con "Test" mediante el uso de la siguiente consulta en un explorador. Pulse el botón derecho en la página del explorador y, a continuación, haga clic en **Ver código fuente**.
  
```html
http://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Para importar datos de project en PowerPivot en Excel 2013, en la cinta de opciones de datos, seleccione la **fuente de datos de OData** en el menú de lista desplegable **Desde otros orígenes** . En el cuadro de diálogo **Asistente para la conexión de datos** , escriba http://ServerName/ProjectServerName/_api/ProjectData/ en los datos de ubicación de fuente, elija **siguiente**y, a continuación, seleccione la tabla de **proyectos** en la página **Seleccionar tablas** del asistente. Nombre y guarde el archivo .odc y, a continuación, seleccione **Finalizar**. En el cuadro de diálogo **Importar datos** , elija **Informe de tabla dinámica**. En la hoja de cálculo de Excel, elija los campos de las filas de la tabla dinámica y columnas que desea mostrar.
  
Los usuarios de Project Server local, que tienen los permisos correctos, pueden acceso directamente a las tablas y vistas de informes a través de Microsoft SQL Server para crear informes, tal y como lo hacen en Project Server 2010. En Project Server 2013, los usuarios también pueden acceso local en tablas de informes a través de la interfaz de OData. Puede recuperar datos de Project Server en línea o local a través de extremos de REST para el servicio de OData. Por ejemplo, dbo. Tabla MSP_PROJECT y dbo. Vista de MSP_EpmProject_UserView se puede usar para los informes. Las tablas o vistas que tienen un `draft`, `pub`, o `ver` prefijo están sólo para uso interno de Project Server y no para informes de uso. Por ejemplo, el borrador. Tabla MSP_TASKS y pub. Vista MSP_PROJECTS_WORKING_VIEW no se documentan y son solo para uso interno. 
  
> [!NOTE]
> Puede ampliar los informes locales agregando tablas, vistas, campos y procedimientos almacenados en una base de datos independiente. No debería modificar las tablas y vistas de informes existentes en la base de datos de Project Server. 
  
Informes tablas, vistas y campos de la base de datos de Project se se documentan en un archivo de Ayuda HTML en una actualización posterior de la descarga del SDK de Project 2013. Para obtener documentación sobre el esquema XML de OData para el servicio **ProjectData** , consulte [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx). En la mayoría de los casos, las consultas de las tablas y vistas que se crearon para Project Server 2010 informes funcionarán con la base de datos de proyecto en Project Server 2013. Los usuarios locales pueden tener acceso a los cubos OLAP de Project Server en SQL Server Analysis Services, tal y como lo hacen actualmente. En Project Online, cubos OLAP no están disponibles.
  
### <a name="task-pane-add-ins-in-project"></a>Complementos de panel de tareas de Project
<a name="pj15_WhatsNew_Agave"> </a>

Project Standard 2013 y Project Professional 2013 admiten tareas panel complementos, que se pueden utilizar para integrar con y mostrar contenido externo en una página Web. El panel de tareas muestra el contenido de la página Web que tiene acceso a través de JavaScript para tareas, recursos, vistas y datos generales del proyecto. El modelo de objetos de JavaScript para Project puede obtener información acerca de una tarea o recurso seleccionado y puede obtener datos de la celda seleccionada en la cuadrícula para las vistas, como el gráfico de Gantt. Complementos de tarea panel proyecto también pueden implementar controladores de eventos para tareas, recursos, o ver los eventos de cambio de selección. 
  
La figura 2 muestra la **Hola ProjectData** tarea panel complemento que consulta el servicio de **ProjectData** y, a continuación, se compara datos en el proyecto actual con el valor promedio de todos los proyectos. La descarga del SDK de Project 2013 incluye el código fuente completo para el complemento. 
  
**Ilustración 2. Un complemento de panel de tareas de Project Professional puede obtener acceso a datos de Project Server**

![Comparar el proyecto actual con todos los proyectos] (media/pj15_RestQueryApp_CompareProject.gif "Comparar el proyecto actual con todos los proyectos")
  
> [!NOTE]
> Project Standard 2013 no puede integrarse directamente con Project Server 2013 a través de complementos de panel de tareas. 
  
Complementos de tarea panel en Project Professional pueden admitir los elementos Web que se crean para Project Server 2013, por lo que los desarrolladores pueden crear una extensión de una vez que se ejecuta con Project Web App y Project Professional. Tarea general panel complementos que se ha desarrollado para otros productos de Office 2013 también pueden usarse con Project Standard 2013 y Project Professional 2013. Para obtener más información, vea [tarea panel complementos para Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Receptores de eventos de Project Server
<a name="pj15_WhatsNew_Events"> </a>

Puede haber varios servidores de Project Web App (también denominados servidores de front-end web o servidores cliente Web) en una granja de servidores de SharePoint que incluye la aplicación de servicio de proyecto de back-end. También se pueden llamar a receptores de eventos de los controladores de eventos. Los controladores de eventos local se pueden implementar con el código de plena confianza e implementados en todos los servidores cliente Web para una instalación local de Project Server. Es posible implementar servicios web en servidores locales o remotos de receptores de eventos remotos y para obtener acceso a varios servidores cliente Web y varias instalaciones de Project Server. Project Online puede usar sólo los receptores de eventos remotos.
  
Controladores de eventos de Project Server se administran mediante SharePoint para cada instancia de Project Web App, en lugar de una página específica de la configuración de Project Web App. En la aplicación de Administración Central de SharePoint, elija **Configuración de aplicación General**, elija **Administrar** en **Configuración de PWA**y, a continuación, elija la instancia en la lista desplegable de **Instancia de Project Web App** en la configuración de PWA página. Para agregar un controlador de eventos local o un receptor de eventos remotos, elija **Controladores de eventos del servidor**.
  
Para una instalación local de Project Server, puede crear un receptor de eventos remotos como una característica de SharePoint que usa la clase [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) en el CSOM y, a continuación, administrar mediante programación la receptor de eventos mediante el uso de métodos en la clase [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) . Para receptores de eventos remotos, eventos anteriores son sincrónicos, eventos posteriores son asincrónicos y hay un tiempo de espera para los casos donde el receptor de eventos remotos no devuelve. 
  
> [!NOTE]
> Administración Central de SharePoint sólo está disponible para instalaciones locales. Para Project Online y SharePoint Online, puede agregar o quitar receptores de eventos remotos mediante un paquete de aplicación basada en CSOM. 
  
En la página de controladores de eventos del servidor, el proceso para agregar un controlador de eventos locales para una instalación de Project Server local es casi el mismo que el proceso descrito en el tema [crear un controlador de eventos de Project Server y registrar un evento](http://msdn.microsoft.com/en-us/library/gg615466.aspx) de Project Server 2010. La diferencia es que la página nuevo controlador de eventos tiene opciones adicionales. Por ejemplo, elija la **Creación de proyectos** en la lista de **eventos** y, a continuación, elija **Nuevo controlador de eventos**. En la página de controlador de eventos de nuevo, los dos únicos necesarias de los campos **nombre** y **orden** (vea la figura 3). Si va a agregar un controlador de eventos de plena confianza local, agregue el campo **Nombre de ensamblado** y el campo **Nombre de la clase** ; Deje la **Dirección Url del extremo** vacía. Si va a agregar un receptor de eventos remotos, agregue la **Dirección Url de extremo**y deje en blanco **El nombre de ensamblado** y el **Nombre de clase** . 
  
> [!CAUTION]
> Si se especifica *tanto* el nombre de clase y nombre del ensamblado y la dirección URL del extremo, Project Server llama la local (local) controlador de eventos. Se omite el receptor de eventos remotos. 
> 
> Si crea dos controladores de eventos para el mismo evento, donde uno es local y el otro remoto, y el valor **Orden** es igual para ambos, Project Server omite el receptor de eventos remotos. 
  
**Ilustración 3. Adición de un controlador de eventos locales o un receptor de eventos remotos**

![Configuración de un controlador de eventos o receptor de eventos] (media/pj15_EventHandlers_NewEventHandler.gif "Configuración de un controlador de eventos o receptor de eventos")
    
Si necesita acceso a los conjuntos de datos PSI para un controlador de eventos local, puede copiar el ensamblado Microsoft.Office.Project.Schema.dll desde la [Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ directorio de 71e9bce111e9429c. 

En lugar de la interfaz PSI, se recomienda que use las clases de eventos en el espacio de nombres **Microsoft.ProjectServer.Client** ; desarrollo con el CSOM no requiere la manipulación de conjuntos de datos. Para desarrollar receptores de eventos remotos para Project Online, debe usar la clase de [evento](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) y la clase [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) en el CSOM. 
  
Antes de implementar un controlador de eventos de Project Server, instalar y probar el controlador de eventos en una instalación de prueba de Project Server. Para una instalación de Project Server local, si el controlador de eventos locales que agregue se convierte en no funciona, el servicio de eventos de Project Server 2013 se produce un error al cargar los otros controladores de evento personalizado válido. En ese caso, debe quitar el controlador de eventos de problema y reinicie el servicio de eventos.
  
> [!NOTE]
> En una instalación local de Project Server, le recomendamos que migre a receptores de eventos remotos usando el CSOM para desarrollar receptores de eventos. Dado que los receptores de eventos remotos no tienen código de terceros en ejecución en Project Server Events Service, son más estables. Los administradores locales se olvidan de la responsabilidad de mantener Project Server Events Service. 
  
Para obtener información general acerca de los eventos, vea [control de eventos en aplicaciones para SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Características desusadas
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Para obtener información sobre las características y las API que están en desuso o se quitó en vista previa de Project Server 2016, vea [¿Qué ha en desuso o eliminado en la vista previa de Project Server 2016](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx). 
  
Características desusadas siguen estando disponibles en Project 2013 para algunas soluciones, pero no se deben usar para el desarrollo de nuevas. La mayoría de las características y las prácticas siguientes no funcionan con Project Online, o con la instalación de Project Server 2013 local predeterminada en el modo de permiso de SharePoint. Las soluciones existentes que utilizan estas características no funcionen para una actualización de Project Server 2010 a Project Server 2013. Aunque en desuso soluciones que usan características pueden continuar trabajando en algunos casos, no son totalmente compatibles para todas las instalaciones de Project 2013.
  
Si las soluciones de usan las características desusadas, debe probarse exhaustivamente antes de la implementación, y se debe modificar para usar admitida características tan pronto como sea práctico. Para obtener información acerca de la configuración de seguridad de Project Server 2013 local para el modo de permiso de Project, vea la sección *Modo de permisos de SharePoint* en [Novedades para los profesionales de TI en Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx).
  
- **Extensiones** [Escenarios de extensión de PSI](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx) están en desuso y no se admite en versiones futuras. Estos escenarios de Project Server 2013 local habían habilitado la integración con servicios de Windows Communication Foundation (WCF) personalizado. 
  
- **Project PSI** La [clase de proyecto](https://docs.microsoft.com/en-us/office/client-developer/project/project-psi-reference-overview) de la PSI está en desuso. Para los nuevos desarrollos, use el [CSOM de Project](client-side-object-model-csom-for-project-2013.md). Project Server 2013 aplicaciones que usan la PSI de Project seguirán funcionando, pero necesitan aplicaciones Project Online reemplazar los métodos PSI de clase de proyecto con sus métodos equivalentes de CSOM.
  
- **PSI de planeamiento de recursos** La [PSI de planeación de recursos](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx) está en desuso. Seguirán siendo compatibles para el desarrollo de Project 2013, pero no se admite en versiones futuras. 
  
- **Interfaz ASMX para la PSI** La PSI incluye interfaces duplicadas para desarrollar extensiones de Project Server local. La interfaz de servicios web ASMX se introdujo con la primera implementación de la PSI en Office Project Server 2007. Project Server 2010 agregó la interfaz de servicios WCF, donde el modelo de objetos, básicamente, duplica los servicios web ASMX. Aunque Project Server 2013 sigue siendo compatible con ASMX y WCF, nuevas soluciones que requieren la PSI deben usar los servicios de WCF. Si es posible, se deben escribir nuevas soluciones con el CSOM. 
  
  Los servicios web ASMX de la PSI están en desuso en Project Server 2013. Para que funcione en futuras versiones de Project Server, se deben volver a escribir soluciones que usan los servicios web ASMX para usar los servicios de WCF o el CSOM. Para obtener más información, vea la sección de *actualización de aplicaciones con la API de Project Server* en la [programación de Project Server](project-server-programmability.md).
  
- **Proveedor de vínculos de objeto (OLP)** En versiones anteriores de Project Server, el servicio **ObjectLinkProvider** en la interfaz PSI (vea [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) ) proporciona una forma de administrar los vínculos de objeto web entre tareas de proyectos de empresa y especializados las listas de SharePoint en el sitio del proyecto para los problemas, riesgos, entregas y documentos. En Project Server 2013, OLP está en desuso. 
  
  Puede usar la clase **[RelatedItemManager](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.client.relateditemmanager.aspx)** en el CSOM de SharePoint para crear, leer y eliminación de vínculos de objeto web entre los elementos de la lista de tareas y las otras listas en un sitio de proyecto. Por ejemplo, para agregar un vínculo de un elemento de tarea a un problema, puede usar el método **[AddSingleLink](http://msdn.microsoft.com/en-us/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** o cualquiera de los dos métodos similares, **AddSingleLinkFromUrl** o **AddSingleLinkToUrl**. La clase **RelatedItemManager** también incluye métodos para eliminar un vínculo de objeto web y la lectura de elementos relacionados. Para la clase equivalente en el JSOM (el modelo de objetos de JavaScript), vea [SP. RelatedItemManager object (sp.js)](http://msdn.microsoft.com/en-us/library/jj838582.aspx).
  
  Se recomienda que use el CSOM de SharePoint para crear aplicaciones de tipo de OLP para una instalación local de Project Server 2013 y Project Online. El espacio de nombres [Microsoft.SharePoint](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.aspx) no incluye un **RelatedItemManager** *** clase. 
  
- **Permisos personalizados** Permisos de seguridad personalizado para tener acceso a características específicas de Project Server o las extensiones se admitían en Office Project Server 2007, donde un artículo en el SDK explica cómo crearlas mediante la modificación directamente de la base de datos publicados. En Project Server 2010, permisos personalizados aún funcionan pero están en desuso. En Project Server 2013, permisos personalizados no funcionan con el modo de permiso de SharePoint predeterminado para instalaciones locales. Para el modo de permiso de Project, se admiten los permisos personalizados. Con Project Online, no es posible el acceso directo de la base de datos. 
  
- **Suplantación** Suplantación en las aplicaciones de PSI-based, donde el usuario de una aplicación puede asumir los permisos de seguridad de un usuario de Project Server diferente, está en desuso en Project Server 2013. Como se ha indicado anteriormente, un valor predeterminado local instalación de Project Server 2013 usa el modo de permiso de SharePoint, que no permite la representación en los grupos de seguridad de Project Server. Para obtener más información, vea [autenticación, autorización y seguridad en SharePoint 2013](http://msdn.microsoft.com/en-us/library/ms457529%28office.15%29.aspx).
  
  Aplicaciones de estado son extensiones típicas que es posible que ha usado la suplantación en versiones anteriores de Project Server. Project Server 2010 presentó el método **ReadStatusForResource** y el método **SubmitStatusForResource** en la interfaz PSI, junto con el permiso global **StatusBrokerPermission** , que elimina la necesidad de suplantación leer y actualizar el estado en nombre de otro usuario. El CSOM en Project Server 2013 usa la PSI subyacente para habilitar extensiones de estado de forma transparente y puede usarse para Project Online o instalaciones locales. 
  
- **Extensiones de la base de datos de informes** Agregar tablas personalizadas y las vistas de la base de datos de informes es una práctica común con versiones anteriores de Project Server. Debido a que Project Server 2013 combina las cuatro bases de datos de versiones anteriores en una base de datos, las actualizaciones no transfieren personalizadas tablas, vistas o procedimientos almacenados para las tablas de informes en la base de datos de Project Server 2013. 
  
  Se recomienda usar SQL Azure o una base de datos de SQL Server independiente para tablas de informes personalizadas y las vistas, donde puede administrar las copias de seguridad de la base de datos y las actualizaciones. Para Project Online, es obligatorio.
  
- **Creación de informes** Las tablas de informes locales y vistas de la base de datos de Project Server y los cubos OLAP, son *no* en desuso y permanecen totalmente compatibles. Sin embargo, las tablas y vistas (la base de datos de informes en las versiones anteriores de Project Server) informes no son accesibles en Project Online. De forma similar, los cubos OLAP sólo están disponibles con instalaciones locales de Project Server 2013. Para informar de las aplicaciones con Project Online, puede usar el servicio **ProjectData** , a través de las consultas REST con el Protocolo OData. 
  
- **Guía de proyectos** La Guía de proyectos es una característica estándar de las aplicaciones de escritorio de Office Project 2007, donde contenido HTML y JavaScript en un panel de tareas proporciona una guía interactiva para crear y administrar proyectos. En Project 2010, la Guía de proyectos no está disponible en una instalación predeterminada, pero se puede habilitar a través de VBA o un complemento de VSTO. La descarga del SDK de Project 2010 incluye los archivos modificados de la Guía de proyectos. 
  
  El modelo de objetos VBA y el modelo de objetos **Microsoft.Office.Interop.MSProject** en Project 2013 aún incluyen a los 22 miembros de la clase de **aplicación** y la clase de **proyecto** que puede administrar a la Guía de proyectos. Sin embargo, Project 2013, aplicaciones de panel de tareas pueden entrar en conflicto con acciones en un panel de tareas de la Guía de proyectos y el contenido de la Guía de proyectos no se puede ser fácilmente distribuida o se venden en la tienda de Office. Se recomienda encarecidamente que desarrolle soluciones de panel de tareas de proyectos con Office Add-ins, contenido de guía de proyectos no personalizado. Para obtener más información acerca de la Guía de proyectos, consulte la [Documentación del SDK de Project 2010](http://msdn.microsoft.com/en-us/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparación de Project Server local con Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Para ayudarle a decidir si va a usar Project Server local o Project Online y qué tipos de extensiones puede desarrollar en cualquier caso, la tabla 2 se comparan las características extensibles de una instalación local de Project Server 2013 con Project Online. Tabla 2 se incluyen las diferencias en la implementación, administración o uso. Para obtener más información acerca de Project Online y Project Server 2013, consulte [Project 2013 para desarrolladores](http://msdn.microsoft.com/en-US/office/fp161502) y [Project Online](https://developer.microsoft.com/en-us/project).
  
**Tabla 2. Extensibilidad de Project Server local y Project Online**

| Característica |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programación ** <br/> |Aplicaciones basadas en el CSOM; modelo de programación coherente  <br/>-. NET, Silverlight, las bibliotecas de cliente de Windows Phone  <br/>-Biblioteca de JavaScript para las páginas personalizadas, elementos Web y las extensiones de la cinta de opciones  <br/>-Protocolos OData y REST<br/><br/> Aplicaciones basadas en PSI; modelo de programación complejo, también puede crear aplicaciones para administración, análisis de cartera, notificaciones, seguridad de modo de Project, sistema de cola y otras áreas<br/><br/>Extensiones de PSI  <br/><br/>Permisos personalizados con la seguridad de modo de Project (desusado)  <br/><br/>Suplantación con la interfaz PSI (desusada)  <br/><br/>Código de plena confianza; extensiones de instalación en la granja de SharePoint  <br/> |Aplicaciones basadas en el CSOM; modelo de programación coherente  <br/>-. NET, Silverlight, las bibliotecas de cliente de Windows Phone<br/>-Biblioteca de JavaScript para las páginas personalizadas, elementos Web y las extensiones de la cinta de opciones<br/>-Protocolos OData y REST<br/><br/>Puede usar la interfaz PSI, pero no es compatible: sin OAuth ni conexiones de servicio a servicio<br/><br/>Sin extensiones de la API del CSOM<br/><br/>Sin permisos personalizados<br/><br/>Sin suplantación<br/><br/>Sin código de plena confianza  <br/> |
|**Bases de datos personalizadas ** <br/> |-SQL Azure  <br/>-SQL Server (modificación de tablas y vistas en el servidor de Project Server no es compatible con la base de datos de informes)  <br/> |-SQL Azure  <br/>-SQL Server (modificación de tablas y vistas en el servidor de Project Server no es compatible con la base de datos de informes)  <br/> |
|**Informes** <br/> |- Servicio de **ProjectData** ; Protocolos de OData y REST  <br/>-Informes de tablas y vistas en la base de datos de Project Server<br/>-Base de datos OLAP  <br/> |- Servicio de **ProjectData** ; Protocolos de OData y REST  <br/> |
|**Controladores de eventos** <br/> |-Receptores de eventos remotos, accesibles a través de los extremos WCF<br/>-Controladores de eventos plena confianza, instalados en la granja de servidores de SharePoint  <br/> | -Receptores de eventos remotos, accesibles a través de los extremos WCF  <br/> |
|**Flujos de trabajo** <br/> |Flujos de trabajo declarativos, creados con SharePoint Designer 2013<br/>-Usar solo en una instancia específica de Project Web App<br/>-Puede importar un diseño de flujo de trabajo desde Visio 2013<br/>-Puede importar y usar acciones personalizadas<br/><br/> Flujos de trabajo declarativos, creados con Visual Studio 2012<br/>-Crear una aplicación que puede incluir los flujos de trabajo<br/>-Crear un paquete de solución de SharePoint (.wsp) que puede incluir los flujos de trabajo<br/>-Crear plantillas de flujo de trabajo para su reutilización<br/>-Crear y usar acciones personalizadas  <br/><br/>Puede usar flujos de trabajo compilados heredados, creados con WF3.5 (actualización recomendada a flujo de trabajo declarativo WF4)  <br/> |Flujos de trabajo declarativos, creados con SharePoint Designer 2013<br/>-Usar solo en una instancia específica de Project Web App<br/>-Puede importar un diseño de flujo de trabajo desde Visio 2013<br/>-Puede importar y usar acciones personalizadas  <br/><br/>Flujos de trabajo declarativos, creados con Visual Studio 2012<br/>-Crear una aplicación que puede incluir los flujos de trabajo  <br/>-Crear un paquete de solución de SharePoint (.wsp) que puede incluir los flujos de trabajo<br/>-Crear plantillas de flujo de trabajo para su reutilización <br/>-Crear y usar acciones personalizadas  <br/> |
|**Distribución ** <br/> |-Office Store (para aplicaciones basadas en CSOM)<br/>-Catálogo de aplicaciones privado en SharePoint<br/>-Recurso compartido de archivos intranet  <br/> |-Tienda de office<br/>-Catálogo de aplicaciones privado en SharePoint  <br/> |

   
## <a name="conclusion"></a>Conclusión
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 proporciona una gran cantidad de nuevas capacidades de desarrollo y escenarios que los asociados y los clientes pueden utilizar para adaptar y extender las capacidades y la utilidad de Project Server en las empresas grandes y en las organizaciones pequeñas. Puede usar la infraestructura para Office 2013 y SharePoint 2013 para ayudar a crear y distribuir aplicaciones para Project 2013 que puede ampliar en gran medida la comerciabilidad y el uso de aplicaciones personalizadas. Algunas características de extensibilidad y prácticas de las versiones anteriores están en desuso en Project 2013, especialmente los servicios de web ASMX de la PSI y las características que implican suplantación o cambios de base de datos directa, lo que no se puede usar con Project Online.
  
La introducción del CSOM habilita el acceso mediante programación a Project Online para una amplia variedad de dispositivos y mediante el uso de JavaScript en aplicaciones web. El CSOM proporciona un modelo de programación más coherente en comparación con la interfaz PSI. Pueden tener acceso a los datos de Project Server en muchas más maneras que en versiones anteriores, incluidos a través del servicio de OData en línea y a través de extremos de REST para datos de informes en la base de datos de Project. Los informes existentes siguen funcionan de la misma manera para su uso local; nuevos informes tienen más flexibilidad.
  
Complementos de Office ofrecen nuevas vías para la venta de soluciones y la integración de Project Standard 2013 con contenido web y otros productos de Office 2013. También puede crear nuevas formas para integrar Project Professional 2013 con datos de Project Server y listas de SharePoint a través de panel de tareas Office Add-ins.
  
Para obtener más información sobre desarrollo de aplicaciones y el uso de las características de programación y el CSOM de SharePoint Server 2013, vea [SharePoint para desarrolladores](http://msdn.microsoft.com/en-US/sharepoint) y [Office para desarrolladores](http://msdn.microsoft.com/en-US/office).
  
## <a name="see-also"></a>Recursos adicionales

- [Project Server 2013 architecture](project-server-2013-architecture.md)  
- [Tareas de programación de Project](project-programming-tasks.md) 
- [Modelo de objetos de cliente (COM) de Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData: referencia del servicio OData de Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)  
- [Complementos de panel de tareas para Project](task-pane-add-ins-for-project.md)   
- [OData: Convenciones URI](http://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint para desarrolladores](http://msdn.microsoft.com/en-US/sharepoint)    
- [Office para desarrolladores](http://msdn.microsoft.com/en-US/office)   
- [Control de eventos en aplicaciones para SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx)   
- [Tienda Office](http://office.microsoft.com/en-us/store/)   
- [Project Online](https://developer.microsoft.com/en-us/project)
    

