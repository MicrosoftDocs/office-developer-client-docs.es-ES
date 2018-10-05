---
title: Información general de referencia PSI de Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- servicio de Web, calendario, autenticación, servicio de servicio, ResourcePlan, Web service, StatusReports, Web, Web PSI, espacios de nombres, los controladores de eventos, Project Server, servicio Web, notificaciones, QueueSystem, servicio, Project 2013, plataforma, Web LoginWindows, Web servicio, servicio Web, el estado, el servicio Web, recursos, WinProj, servicio Web de servicio, WssInterop, Web, servicio, Winproj, evento controladores, LookupTable, Web service, PWA, Web servicio Web, Web, seguridad, notificaciones, servicio Web, servicio Web, Parte de horas, Web service, QueueSystem, PSI, servicios Web, servicio Web, eventos, PSI, programación, servicio Web, LookupTable, versión, servicio Web, CustomFields, servicio Web, servicio Web, PWA, PSI, recurso, servicio Web, servicio Web, ResourcePlan, del parte de horas, Web servicio Web, las reglas, PSI, administrado, de servicio de código de servicio de referencia, seguridad, Web, Web la dirección URL del servicio, CustomFields, para la interfaz PSI, referencia, PSI, Web servicio de servicio, WssInterop, Web service, administración, Web, Web CubeAdmin, vista, servicio, calendario, Web servicio Web, Web servicio, vista, administración, servicio Web, LoginForms, Web service, servicio Web, LoginForms, PSI, las direcciones URL, ObjectLinkProvider, servicio, archivo, Web service, CubeAdmin, Web service, reglas, Web servicio Web, servicios Web de autenticación, de servicio, PSI, Project Server Web , eventos, eventos, servicio Web, servicio Web, Project, estado, Web service, servicio Web, ObjectLinkProvider, Project Server Interface, métodos, PSI, Web service, StatusReports, Web servicio Web, archivo, proyecto, Web service, servicio Web, LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: Project Server Interface (PSI) es la API que se usará para desarrollar aplicaciones que se integren con Project Server 2013 local.
ms.openlocfilehash: 58235e16afd208d0d4415e28ad200cc7ff62ac8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390124"
---
# <a name="project-psi-reference-overview"></a>Información general de referencia PSI de Project

Project Server Interface (PSI) es la API que se usará para desarrollar aplicaciones que se integren con Project Server 2013 local.
  
En este artículo es una descripción general de los ensamblados documentados, espacios de nombres y servicios en la PSI. La [referencia de servicio de web y biblioteca de clase de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) en el SDK contiene toda la documentación de código administrado para la PSI y el espacio de nombres [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) en Project Server 2013. Para desarrollar aplicaciones para Project Online, debe usar el espacio de nombres **Microsoft.ProjectServer.Client** en lugar de la PSI. 

La PSI de Project Server 2013 tiene una interfaz dual. La interfaz de ASMX de servicios web se define mediante la detección y los archivos de lenguaje de descripción de servicios Web (disco y WSDL) en el `https://ServerName/ProjectServerName/_vti_bin/psi/` directorio virtual (por ejemplo, Projectdisco.aspx y Projectwsdl.aspx). Puede obtener acceso a la interfaz ASMX sólo a través de la dirección URL de una instalación local de Project Web App (por ejemplo, `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Para mostrar el servicio web en un explorador, debe incluir la `?wsdl` opción de dirección URL. Dado que la interfaz ASMX está integrada con la infraestructura de Windows Communication Foundation (WCF), los archivos .asmx para servicios web de Project Server no existe realmente en el directorio virtual de PSI. 
  
La interfaz de servicios WCF se define mediante archivos de SVC en el back-end `https://ServerName:32843/GUID/PSI/` directorio virtual de la aplicación de servicios Web de SharePoint. Los servicios de la dirección URL de PSI en el directorio virtual de la aplicación de servicio de proyecto (por ejemplo, `https://ServerName:32843/GUID/PSI/project.svc`) incluye los archivos de SVC. Pero no se puede utilizar directamente la dirección URL de back-end para establecer una referencia de servicio WCF. Para desarrollar una aplicación o componente que utiliza los servicios WCF de la PSI, puede usar un archivo de proxy o de un ensamblado de proxy. La descarga del SDK de Project 2013 incluye archivos proxy para los servicios de WCF en Project Server 2013 y secuencias de comandos para obtener archivos actualizados de proxy WCF y para compilar los archivos en un ensamblado de proxy para más reciente de Project Server se basa.
  
El nombre de directorio de aplicación de servicio de proyecto es un valor GUID, que es el mismo que el GUID de la instancia de Project Web App local. En la ventana **Administrador de Internet Information Services (IIS)** , expanda el nodo de **Servicios Web de SharePoint** , elija el nombre del directorio GUID y, a continuación, elija **Configuración avanzada** para copiar el valor de la **Ruta de acceso Virtual** . 
  
> [!IMPORTANT]
> La interfaz de servicio web ASMX de la PSI está en desuso en Project Server 2013, pero todavía se admite. Nuevas aplicaciones deben utilizar la interfaz WCF de PSI o CSOM. Para obtener más información acerca de las características en desuso, vea [actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)
> 
> Nuevas aplicaciones y componentes de software intermedio que se ejecutan sólo en una instalación local de Project Server, deben usar la interfaz WCF, que es la tecnología que se recomienda para las comunicaciones de red. Las aplicaciones heredadas que usan la interfaz ASMX deben usar la dirección URL a través de Project Web App, que comprueba los permisos de Project Server. 
> 
> Para obtener más información acerca de la interfaz ASMX y cómo usar la interfaz WCF, vea [requisitos previos para ejemplos de código basados en ASMX de proyecto](prerequisites-for-asmx-based-code-samples-in-project.md) y [los requisitos previos para ejemplos de código basados en WCF en Project](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Para desarrollar aplicaciones que usan la interfaz WCF, puede usar Visual Studio 2010 o Visual Studio 2012. Para la creación de flujos de trabajo declarativos en Project Server, puede usar SharePoint Designer 2013. Los flujos de trabajo Project Server que requieren acceso a la PSI o CSOM se pueden desarrollar con Visual Studio 2012.
  
### <a name="using-the-psi-reference"></a>Uso de la referencia de la PSI
<a name="pj15_PSIRefOverview_Using"> </a>

El modelo de objetos PSI es grande y muchas clases y miembros son únicamente para uso interno. Como resultado, puede resultar confusa buscar los temas que desee en la [referencia de servicio web y biblioteca de clases de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx). La mayoría de los temas de referencia que va a usar para el desarrollo se encuentran en los siguientes grupos:
  
- **Métodos de la clase principal:** Cada servicio de la PSI incluye una clase principal que se denomina para el nombre del servicio. Por ejemplo, el servicio de **recursos** contiene la clase de [recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) , que se encuentra en el espacio de nombres [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx) . Para ver una lista de los métodos que están disponibles en la clase de **recursos** , expanda el nodo de clase en el panel de contenido y, a continuación, elija el tema de **Métodos de recursos** . 
    
- **Propiedades de DataRow:** Muchos de los métodos de la clase principal usarán o devuelven un **conjunto de datos**. Cada objeto **DataTable** de un **conjunto de datos** contiene datos en uno o más objetos **DataRow** . En la mayoría de los casos, debe ver solo las propiedades de fila, no todos los otros miembros de las clases **DataSet**, **DataTable**o **DataRow** . Por ejemplo, la clase **ResourceAssignmentDataSet** incluye subclases para el **ResourceAssignmentDataTable** y la clase [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx) . Para ver una lista de propiedades que se encuentran en la clase **ResourceAssignmentRow** , expanda el nodo de clase en el panel de contenido y, a continuación, elija el tema de **Las propiedades de ResourceAssignmentDataSet.ResourceAssignmentRow** . 
    
Además de los espacios de nombres de servicio, los vínculos de tema de [referencia de servicio de web y biblioteca de clase de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) a los tres ensamblados de Project Server que se usan en el desarrollo de soluciones de terceros para instalaciones locales. Se proporciona sólo una documentación mínima para estos ensamblados. La referencia de PSI documenta las clases principales y los miembros de los servicios públicos 23. Servicios de PSI seis son únicamente para uso interno y no se documentan. 
  
> [!NOTE]
> Clases en el modelo de objetos de cliente (CSOM) pueden usarse independientemente de los otros ensamblados de Project Server y servicios. Puede usar el espacio de nombres **Microsoft.ProjectServer.Client** en un entorno de desarrollo remoto desde el equipo de Project Server y desarrollar aplicaciones que se integren con Project Online o con una instalación local de Project Server. Sin embargo, el CSOM contiene un subconjunto de la funcionalidad de la PSI completa. El CSOM permite el desarrollo de los escenarios más comunes para la integración de Project Server. Para obtener más información, vea [el CSOM ¿qué hace y no hace](what-the-csom-does-and-does-not-do.md) y [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Para el desarrollo de la mayoría de las aplicaciones que usan la interfaz PSI, no es necesario que desarrollar en un equipo de Project Server, o establecer referencias a ensamblados de Project Server en la memoria caché de ensamblados global. Puede copiar los ensamblados de Project Server es necesarios en el equipo de desarrollo. Project Server 2013 instala los siguientes ensamblados de _[Program Files]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Espacios de nombres para los servicios PSI tienen nombres arbitrarios creados para un ensamblado de proxy PSI, ProjectServerServices.dll, que se genera con el fin de documentación. En la referencia de PSI, cada espacio de nombres de servicio tiene un nombre de marcador de posición (por ejemplo, _[servicio web del proyecto]_) y una referencia web (como `https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Ensamblados y conjuntos de nombres de Project Server
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Muchos de los ensamblados se instalan al instalar Project Server; se documenta sólo cuatro de los ensamblados de Project Server. Normalmente, los programadores de terceros usa sólo algunas clases y miembros en esos ensamblados. Los ensamblados de Project Server sin documentar incluyen espacios de nombres y clases que Project Server usa internamente, como las clases para Project Web App, las entidades empresariales, y el acceso a datos (DAL) de la capa. Cuando se establece una referencia en Visual Studio en uno de los ensamblados documentados de Project Server, puede ver todos los espacios de nombres, clases y miembros en el Examinador de objetos de Visual Studio.
  
> [!NOTE]
> Muchos miembros de los espacios de nombres documentados de Project Server solo se usan internamente y tienen una documentación mínima. 
  
Al desarrollar para Project Online, puede usar sólo el CSOM para tener acceso a funciones de Project Server. No tiene acceso a los servicios de PSI o los otros ensamblados de Project Server.
  
La [referencia de servicio de web y biblioteca de clase de Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) para la PSI incluye espacios de nombres de los siguientes ensamblados: 
  
- **Microsoft.Office.Project.Server.Library.dll** este ensamblado contiene un espacio de nombres documentado y tres espacios de nombres sin documentar, como se indica a continuación: 
    
  - El espacio de nombres [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) incluye muchas enumeraciones y campos de la clase y las propiedades que se usan con frecuencia en las aplicaciones locales para Project Server. Por ejemplo, los desarrolladores suelen utilizar enumeraciones como **CustomField.Type**y las clases **PSClientError**, **PSErrorInfo**y **filtro** . 
    
    El espacio de nombres **Microsoft.Office.Project.Server.Library** también incluye las siete siguientes clases de propiedades, que incluyen más de 3.200 subclases: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    Las clases de propiedad se usan internamente y no se documentan. Las clases de propiedad se usan para la serialización entre 2013 de Project Professional y Project Server. Cuando se trabaja con el espacio de nombres **Microsoft.Office.Project.Server.Library** en Visual Studio, el Examinador de objetos muestra todas las clases de propiedad, lo que es más difícil encontrar las clases que son útiles para el desarrollo de aplicaciones de terceros. Debido a que los programadores de terceros no es necesario usar las clases de propiedad, el SDK de documentos no ellos. 
    
  - **Microsoft.Office.Project.Server.DataServices** las clases y los miembros de este espacio de nombres se usan internamente por el servicio de **OData** en Project Online para tener acceso a las tablas de informes en la base de datos de Project. Las clases de **DataServices** no se documentan. 
    
  - **Microsoft.Office.Project.Server.Administration** la clase y los miembros de este espacio de nombres se usan internamente para registro de diagnóstico y que no se documentan. 
    
  - **Microsoft.Office.Project.Server.Base** las clases y los miembros de este espacio de nombres se usan internamente como clases base y no se documentan. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** este espacio de nombres se usa internamente para generar esquemas de filtro y no está documentada. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** este ensamblado se usa para flujos de trabajo de Project Server 2010 heredados que pueden seguir trabajando en Project Server 2013. Para crear nuevos flujos de trabajo, debe usar SharePoint Designer 2013 o, también puede usar Visual Studio 2012 con la clase [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) . El ensamblado de Microsoft.Office.Project.Server.Workflow.dll incluye los tres espacios de nombres siguientes: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) este espacio de nombres incluye las clases que se usan para las actividades de flujo de trabajo de Project Server. Las actividades incluyen leer, comparar y actualizar las propiedades del proyecto. Otras clases administración flujos de trabajo e incluyen las devoluciones de llamadas de flujo de trabajo cuando se cambian los proyectos. 
    
  - **Microsoft.Office.Project.PWA** este espacio de nombres incluye a un proxy interno para la interfaz PSI, para su uso con Project Web App y con las actividades de flujo de trabajo personalizado; no está documentada. 
    
    Una actividad de flujo de trabajo personalizado requiere una referencia a **Microsoft.Office.Project.PWA** para tener acceso a todas las clases de los servicios de PSI. Por ejemplo, la clase **Microsoft.Office.Project.PWA.PSI** incluye la propiedad **ProjectWebService** , que obtiene a un proxy para el espacio de nombres [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx) . 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** este espacio de nombres incluye las clases de proxy interno para la clase principal en cada servicio de la PSI. Mediante el uso de los permisos elevados del usuario de flujo de trabajo, el flujo de trabajo puede llamar a los métodos PSI a través de las clases de proxy. Las clases de proxy no se documentan. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) es el espacio de nombres sólo en este ensamblado. Incluye receptor de eventos y las clases de argumento de evento para los servicios de PSI y otras clases internas. 
    
  Los programadores escriben gestores de eventos derivados de las clases receptoras de eventos. La mayor parte de las clases primarias de los servicios de PSI tienen una clase receptora de eventos correspondiente. Por ejemplo, la clase **ProjectEventReceiver** contiene métodos receptores anteriores y posteriores al evento que se corresponden con métodos de la clase **Project** en la PSI. El método **OnCreating** y el método **OnCreated** son los métodos receptores anteriores y posteriores al evento para el método **QueueCreateProject**. 
    
  Los programadores normalmente usan las siguientes clases receptoras de eventos:
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  **Las** clases ruleseventreceiver y **StatusReportsEventReceiver** se usan internamente en Project Web App. 
    
- **Microsoft.ProjectServer.Client.dll** este ensamblado contiene el CSOM para el desarrollo con .NET Framework 4. El ensamblado se encuentra en `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Desarrollo de aplicaciones con el espacio de nombres **Microsoft.ProjectServer.Client** es independiente de la API de local Project Server y servicios, aunque las aplicaciones pueden trabajar con un local o instalación en línea de Project Server. Para los ensamblados CSOM relacionados que se pueden usar para Windows Phone 8, Microsoft Silverlight o JavaScript con aplicaciones web, vea [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
    
- **Microsoft.Office.Project.Server.Schema.dll** del SDK de Project 2013 no documenta el espacio de nombres **Microsoft.Office.Project.Server.Schema** , que se encuentra en la `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll` ensamblado. El espacio de nombres contiene las definiciones de todas las clases de **DataRow** , **DataTable**y **conjunto de datos**usadas en la interfaz PSI, además de muchas otras clases similar que Project Server usa internamente. Las clases públicas en cada servicio de la PSI se documentan en la referencia de servicio específica. Por ejemplo, la clase **DriverDataSet.DriverRow** se documenta en el espacio de nombres [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx) . 
    
  > [!NOTE]
  > Las aplicaciones que usan el CSOM, usar controladores de eventos remotos o tener acceso a Project Online no use el espacio de nombres **Microsoft.Office.Project.Server.Schema** . 
  
  En algunas aplicaciones que usan gestores de eventos de plena confianza, en las que los gestores de eventos se instalan en el equipo con Project Server, es necesario definir una referencia al ensamblado Microsoft.Office.Project.Schema.dll. A continuación se muestran dos ejemplos:
    
  - En un gestor de eventos posteriores **OnCreated** de confianza plena para campos personalizados, se puede usar el argumento del evento **e.CustomFieldInformation** con una referencia al espacio de nombres **Microsoft.Office.Project.Server.Schema** para las definiciones de **CustomFieldDataSet** y **CustomFieldsRow**. 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - Una actividad de flujo de trabajo personalizada puede requerir una referencia a **Microsoft.Office.Project.Server.Schema** para definiciones de **DataSet**. 
    
## <a name="psi-services"></a>Servicios de PSI
<a name="pj15_PSIRefOverview_PSI"> </a>

La PSI es un conjunto de servicios de WCF y los servicios web ASMX idénticos para Project Server 2013. Para usar un servicio en un proyecto de Visual Studio, se establece una referencia a la dirección URL de la `.svc` archivo o el `.asmx?wsdl` service mediante el uso de un nombre arbitrario de la nameservice. La utilidad wsdl.exe o la utilidad svcutil.exe, a continuación, genera el código fuente del proxy para ese espacio de nombres, y el compilador crea un ensamblado de proxy de servicio para incluir en la aplicación. 
  
> [!NOTE]
> La referencia de PSI incluye nombres de nameservice de marcador de posición para los servicios PSI como _[servicio web de administración]_, _[servicio web del controlador]_ y _[servicio web del proyecto]_. Cada nameservice PSI incluye una clase principal que contiene los métodos web para dicho servicio. Por ejemplo, si se establece una referencia al servicio de **administración** y asígnele el nombre **WebSvcAdmin**, a continuación, en la aplicación de la **WebSvcAdmin** nameservice incluye la clase principal de **administración** que tiene los métodos web **GetServerCurrency**, **ListInstalledLanguages**, **ReadServerVersion**y así sucesivamente. Vea [actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md) para obtener una lista de servicios PSI en desuso. 
  
De los servicios PSI totales 30, **autenticación**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **PWA**, **vista**y **WinProj** son para uso interno por Project y Project Web App Professional y son no documentan. Aunque se puede crear un ensamblado de proxy que incluye los servicios internos de PSI o archivos de proxy, los servicios internos no son para uso de terceros; la referencia de PSI no documentos esos servicios. En la siguiente figura muestra la ubicación de los servicios PSI back-end en Administrador de Internet Information Services. 
  
**La ubicación de los servicios de PSI en IIS**

![Servicios PSI en el Administrador de IIS] (media/pj15_PSIReference_IIS.gif "Servicios PSI en el Administrador de IIS")
  
Las siguientes son todas las clases que contienen métodos web en los servicios de PSI:
  
1. [Administración](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Incluye métodos que se usan en las páginas de **Administración de Project Server** en Project Web App. Define los años fiscales, administra la configuración de Estados y moneda, informes de períodos, el registro de auditoría y la configuración de Active Directory. 
    
2. [Archivo](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Incluye métodos para administrar la copia de seguridad y restauración de proyectos, las categorías de seguridad, los campos personalizados, recursos, configuración del sistema, las vistas y el proyecto global de empresa. Lee y actualiza la programación de archivado. Archiva todos los proyectos o elimina los proyectos archivados especificados. Guarda los objetos de copia de seguridad en las tablas de base de datos de archivado y restaura cuando se realiza una copia de seguridad de objetos en las tablas de base de datos publicados. 
    
3. **autenticación** Incluye métodos para uso interno solamente por Project Professional y Project Web App. 
    
4. [Calendario](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Administra las excepciones del calendario de empresa. Desprotege y comprueba en calendarios de recursos. Crea, elimina, se enumeran todos los, actualiza o devuelve excepciones de calendario. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Administra la configuración del cubo OLAP. Obtiene la lista de cubos, estado de la base de datos y Analysis Server. Coloca una solicitud de servicio de generación de cubo en la cola. Lee y actualiza las definiciones de miembros calculados y los valores de campo de las dimensiones y medidas del cubo. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Administra campos personalizados de empresa. Incluye la desprotección y proteger métodos y la creación, lectura, actualización y métodos de eliminación (CRUD) para campos personalizados de empresa. 
    
7. [Controlador](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Administra controladores de análisis de cartera de proyectos y priorización de impulsores para creación de proyectos y administración de propuestas. Incluye los métodos CRUD para controladores de proyecto. 
    
8. [Eventos](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Administra las asociaciones de controlador de eventos de Project Server. Incluye los métodos CRUD para asociaciones de controlador de eventos de Project Server para un evento específico, o para todas las asociaciones de controlador de eventos. 
    
9. **ExchangeSync** Esto es un servicio interno de Project Server que controla los eventos de Exchange Server. Project Web App usa **ExchangeSync** para sincronizar las asignaciones entre Project Server y Exchange Server, en lugar de sincronizar directamente con el cliente de Outlook como en Office Project Server 2007. 
    
    El acceso a **ExchangeSync** solo está disponible a través de la dirección URL de **ProjectServiceApplication**. Las clases y miembros de **ExchangeSync** no se admiten para el desarrollo de terceros. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Proporciona los métodos de **Inicio de sesión** y **cierre de sesión** con autenticación basada en formularios. Acceso al servicio **LoginForms** está disponible sólo en un sitio de Project Web App front-end. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Proporciona los métodos de **Inicio de sesión** y **cierre de sesión** que se usan para la autenticación de Windows con aplicaciones basadas en ASMX para autenticación múltiple (notificaciones y basada en formularios) las instalaciones de Project Server 2013. Acceso al servicio **LoginWindows** está disponible sólo en un sitio de Project Web App front-end. 
    
    > [!CAUTION]
    > El servicio **LoginWindows** no se usa en aplicaciones basadas en WCF ni para aplicaciones que se ejecutan en instalaciones de Project Server que solo usan la autenticación de notificaciones o **OAuth**; en estos casos, el método **Login** siempre devuelve **false**. La autentificación de notificaciones gestiona la autenticación de Windows integrada. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Administra las tablas de búsqueda, tablas de búsqueda en varios idiomas y sus máscaras de código correspondiente. Desprotege, protege, lee, crea, elimina y las actualizaciones. 
    
13. [Notificaciones](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Administra las alertas y avisos. Incluye métodos que obtengan, establecerán, registran y anular el registro de los resultados de la alertas. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Administra objetos web y vínculos de documentos y elementos de lista en sitios de SharePoint. Crea, elimina o lee el proyecto, vinculados de proyecto, tarea u objetos web vinculada a la tarea. 
    
    > [!NOTE]
    > El servicio **ObjectLinkProvider** está en desuso en Project Server 2013. Para obtener más información, vea la sección *características ya no se utiliza* en [actualizaciones para programadores de Project 2013](updates-for-developers-in-project-2013.md). 
  
15. **OData** Proporciona la interfaz interna de **OData** para las tablas y vistas de informes. Acceso al servicio de **OData** está disponible sólo a través de la dirección URL **ProjectServiceApplication** de back-end. El servicio de **OData** privado en la interfaz PSI proporciona un método, **ODataClient.ProcessOdataMessage**, que Project Server usa internamente para procesar las solicitudes de datos de informes. Las solicitudes HTTP que se van a través del servicio **ProjectData** front-end. 
    
    Para obtener información sobre el servicio **ProjectData** y el Protocolo OData para leer datos de informes, consulte [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/library/office/jj163015.aspx).
    
16. **P12Upgrade** Proporciona métodos internos para el programa de instalación de Project Server 2013 actualizar una instalación de Office Project Server 2007. Acceso al servicio **P12Upgrade** está disponible sólo a través de la dirección URL de **ProjectServiceApplication** . No se admiten los métodos **P12Upgrade** para el desarrollo de aplicaciones de terceros. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Incluye los métodos CRUD para dependencias del proyecto y las soluciones del optimizador, planeador y análisis. 
    
18. [Proyecto](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Administra los proyectos. Desprotege, protege, crea, elimina, lee o actualiza proyectos en las tablas de borrador de base de datos de Project o tablas publicadas. Coloca un mensaje en la cola para la publicación. 
    
    Crea o elimina las entidades dentro de proyectos (tareas, recursos, asignaciones y así sucesivamente). Obtiene información o actualiza el equipo del proyecto o la dirección del sitio del proyecto. Obtiene el estado del proyecto, una lista de proyectos en las tablas de borrador, todas las tareas de resumen, las tareas que están disponibles para su asignación a un recurso especificado o todos los proyectos donde un recurso tiene asignaciones.
    
    Crea y administra compromisos, crea propuestas de proyectos y proyectos desde listas de tareas de SharePoint y busca relaciones de proyecto/proyecto maestro.
    
19. **psiserviceapp** Se usa internamente en Project Online. No se admiten las clases **psiserviceapp** y miembros para el desarrollo de aplicaciones de terceros. 
    
20. **PWA** Contiene muchos métodos que están optimizados para Project Web App, incluidos los métodos para las reglas de aprobación de actualización de tareas y para la administración de informes de estado. Los métodos de **PWA** a menudo están especializados y algo redundantes en comparación con los métodos equivalentes en otros servicios PSI. Métodos de **PWA** usarán o devuelven muchos de los conjuntos de datos mismo como los otros métodos PSI. 
    
    El acceso al servicio **PWA** solo está disponible a través de la dirección URL **ProjectServiceApplication**. Las clases y miembros de **PWA** no se admiten para desarrollo de terceros. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Administra la cola de Project Server. Obtiene el recuento de trabajos, trabajo y tiempo de espera de grupo de trabajo, estado de todos los trabajos, trabajos especificados, los trabajos que pertenecen a la persona que llama o trabajos para proyectos especificados. Administra la correlación de trabajo y se configura la cola. 
    
22. [Recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Administra los recursos de empresa. Desprotege, protege, actualiza o crea recursos o usuarios de Project Server y su configuración de autorización; Encuentre recursos por nombre o GUID; lee el recurso o datos de usuario y la estructura detallada de recursos (RBS) y la información de seguridad relacionados; Obtiene todas las asignaciones de un recurso; y restablece las contraseñas de usuario. La clase de **recursos** incluye métodos CRUD para delegaciones de usuario. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Administra los planes de recursos. Desprotege, protege, publica e incluye los métodos CRUD para planes de recursos. 
    
24. [Seguridad](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Incluye los métodos CRUD para las plantillas de seguridad, las categorías de seguridad, organizativos y permisos globales y los permisos del grupo. La clase **Security** incluye métodos para categorías de proyectos. 
    
25. [Administración de Estados](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Administra las actualizaciones de estado y las asignaciones. Aplica las actualizaciones de estado o aprobaciones, envía estado actualiza, Establece la información de resumen para las actualizaciones enviadas, elimina las actualizaciones de estado aprobado o historial de aprobación para un usuario especificado o elimina toda la información de estado de un conjunto de proyectos. Crea, obtiene o delega las asignaciones; establece la duración del trabajo de la asignación. Obtiene las asignaciones de nuevo para el usuario actual; Obtiene el historial de transacciones de asignación o una tarea, los datos reales con fases temporales o la jerarquía de la tarea de resumen. 
    
    Previsualiza o importa datos de partes de horas o lee el programa de trabajo y no trabajo de un usuario. Busca actualizaciones de estado pendientes, información de actualizaciones enviadas o un registro de transacciones de los cambios en una actualización enviada. Lee el estado del equipo.
    
26. [Parte de horas](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Administra los partes de horas. Incluye los métodos CRUD para los partes de horas y envía o recuperaciones de partes de horas. Busca los partes de horas que son más tarde o pendiente de aprobación; busca los partes de horas por fecha o período. Obtiene la lista de aprobadores de partes de horas. Carga previamente los datos reales del parte de horas y valida una línea del parte de horas. La clase de **parte de horas** incluye el método **ReadProjectTimesheetLines** y el método **SubmitTimesheetLines** para leer y enviar partes de horas para otro recurso sin necesidad de suplantación. 
    
27. **Vista** El servicio de **vista** está diseñado para su uso únicamente en Project Web App. Métodos en la clase de **vista** administración vistas y ver los informes y los campos en las vistas de lectura. 
    
    El acceso al servicio **View** solo está disponible a través de la dirección URL de **ProjectServiceApplication**. Los métodos **View** no se admiten para el desarrollo de terceros. 
    
28. **WinProj** El servicio de **WinProj** está diseñado para su uso solamente por Project Professional. Los programadores de terceros no deben usar los métodos de **WinProj** para programar con Project Server. 
    
    Algunos métodos de **WinProj** usan conjuntos de datos tales como **ProjectRelationsDataSet** y **ResourceDataSet** que también usan los servicios **Project** y **Resource**, pero que requieren propiedades y funciones específicas en Project Professional. 
    
    El acceso al servicio **WinProj** solo está disponible a través de la dirección URL de **ProjectServiceApplication**. Los métodos **WinProj** o se admiten para el desarrollo de terceros. 
    
29. [Flujo de trabajo](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Incluye los métodos CRUD para tipos de proyecto empresarial y para administrar las fases y las fases de flujo de trabajo. Ejecuta los flujos de trabajo, Establece la información de estado y administra etapas de página (PDP) de todos los detalles del proyecto en flujos de trabajo de administración de propuestas. Para desarrollar flujos de trabajo de Project Server, los programadores pueden usar SharePoint Designer 2013 para flujos de trabajo declarativos o usar Office Developer Tools para Visual Studio 2012 para el desarrollo con .NET Framework 4 y el [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) clase en el CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Administra los sitios de proyecto. Crea y elimina sitios de proyecto. Obtiene información acerca de y actualiza la configuración de SharePoint y los sitios de administración. Sincroniza y actualiza los grupos y las pertenencias a sitios de proyecto. 
    
Cada espacio de nombres de servicio incluye todas las clases de controlador de eventos y el esquema de **conjunto de datos** que usa el servicio. Por ejemplo, `Calendar.svc` (o `Calendar.asmx?wsdl` para el ASMX de servicio web) describe el servicio de **calendario** . Si el nombre de la referencia **WebSvcCalendar**el espacio de nombres de proxy contiene el principal **calendario de** clase con los métodos **CheckInCalendars**, **CheckOutCalendars**y así sucesivamente. El espacio de nombres de proxy **WebSvcCalendar** también incluye la clase **CalendarDataSet** y todas sus subclases. 
  
Algunos de los servicios de la PSI contienen clases **DataSet** duplicadas. Por ejemplo, tanto el servicio **Project** como el servicio **Statusing** incluyen la clase **ProjectDataSet**. Esto se debe a que los métodos de los servicios **Project** y **Statusing** incluyen referencias a **ProjectDataSet**, y los ensamblados de proxy que crea al configurar referencias y compilar una aplicación incluyen los conjuntos de datos relacionados. Los servicios **Project** y **Statusing** pueden solicitar valores para diferentes campos en la clase **ProjectDataSet.ProjectRow**. 
  
Si navega por los espacios de nombres y clases de la referencia de la PSI, por ejemplo, para ver los métodos web para el servicio **Project**, expanda el espacio de nombres **[Servicio web de proyecto]** en la lista **Contenido** y, a continuación, expanda la clase **Project**. 
  
## <a name="see-also"></a>Vea también

- [Project Server 2013 architecture](project-server-2013-architecture.md)
- [Programación de Project Server](project-server-programmability.md)   
- [Lo que hace y no hace PSI](what-the-psi-does-and-does-not-do.md)   
- [Requisitos previos para ejemplos de código basados en ASMX en Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Requisitos previos para ejemplos de código basados en WCF en Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [Centro de programadores de .NET Framework](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

