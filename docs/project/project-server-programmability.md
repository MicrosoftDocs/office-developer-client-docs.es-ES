---
title: Programación de Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- events
- PDS
- PDS compatibility
- Project Server databases
- Project Server events
- Project Server Interface
- Project Server workflow
- Project workflow
- PSI
- PSI limitations
- PSI uses
- SharePoint Services
- WF
- workflow
- Workflow Foundation
- WSS
keywords:
- Project 2013, las versiones de programación, PSI, proyectos y arquitectura, programación, Project Server, PSI, las limitaciones, Project Server Interface, admitidas genérico de compatibilidad, Project Server Interface, de las características, Project Server Interface, PDS, Project Server, project proyectos de versiones, las versiones, Project Server, las bases de datos, Project 2013, plataforma, Project Server Interface, usar los eventos de escenarios, Project Server, Project Server, el servicio de datos de Project, la compatibilidad con PSI, Project Server Interfaz
localization_priority: Normal
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Obtenga información sobre las características principales de programación de Project Server 2013. En este artículo se incluye información acerca de trasladar las aplicaciones que han sido creadas para versiones anteriores de Project Server.
ms.openlocfilehash: c2c03da1e0b7c010d4cad8801f98c0c0cf0b1883
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821441"
---
# <a name="project-server-programmability"></a>Programación de Project Server

Obtenga información sobre las características principales de programación de Project Server 2013. En este artículo se incluye información acerca de trasladar las aplicaciones que han sido creadas para versiones anteriores de Project Server.

Project Server 2013 está diseñado para admitir la mayoría de las aplicaciones que se desarrollaron para Project Server 2010 y nuevas soluciones para varias plataformas, donde aplicaciones pueden tener acceso a ambos en línea y las instalaciones de Project Server local. Aplicaciones y extensiones que se desarrollaron para Project Server 2003 o anterior deben volver a diseñarse para usar el modelo de objetos de cliente (COM) o Project Server Interface (PSI). Las aplicaciones que se desarrollaron para Office Project Server 2007 o Project Server 2010 pueden requerir algunos cambios y volver a compilar para usar la interfaz PSI; Para usar el CSOM, las aplicaciones requieren un cambio de diseño.
  
La plataforma de Project Server permite altos niveles de productividad de los programadores mediante la creación en SharePoint Server 2013, .NET Framework 4 y el Protocolo OData con el CSOM. Los desarrolladores pueden ampliar Project Web App con aplicaciones, los elementos de aplicación y los elementos Web, definir flujos de trabajo mediante el uso de SharePoint Designer 2013 y exigir la aplicación de reglas de negocio mediante el uso de receptores de eventos remotos para los eventos de Project Server.
  
## <a name="project-server-and-sharepoint-server"></a>Project Server y SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App se basa en SharePoint Server 2013 y usa páginas maestras y elementos Web para que sea más fácil crear aplicaciones personalizadas y soluciones de Project Web App. Project Server 2013 se integra profundamente con SharePoint Server 2013 como la plataforma de colaboración de project, reporting, administración de sitios, seguridad y administración de flujo de trabajo.
  
Los sitios del proyecto incluyen más información y opciones de colaboración para los miembros del equipo, donde puede agregar aplicaciones predeterminadas que incluyen un proyecto de las listas de SharePoint de resumen, especializado para las tareas con una escala de tiempo, el seguimiento de problemas, riesgos, entregas, del proyecto y el calendario de equipo, junto con las discusiones de equipo y de biblioteca de documentos. Aplicaciones personalizadas para Project Server 2013 proporcionan extensiones y flexibilidad para la colaboración en equipo. También puede agregar elementos de la aplicación para personalizar una aplicación, mediante el mismo mecanismo para agregar y editar elementos Web cuando se edita una página. Puede encontrar los sitios del proyecto en cualquier lugar dentro de la granja de servidores de SharePoint donde está instalado el servidor de Project Server. Para usar otros servicios principales de SharePoint Server 2013, como servicios de Excel y de búsqueda Enterprise Search, un administrador puede habilitar y configurar los servicios. 
  
Al instalar Project Server 2013, aprovisionar la aplicación de servicio de proyecto en el sitio de SharePoint Web Services. La aplicación de servicio de proyecto incluye los servicios locales de Windows Communication Foundation (WCF) y servicios web de ASMX para la PSI. Otras aplicaciones de servicio ejemplos de búsqueda de SharePoint y administración de documentos de SharePoint. Para obtener más información, vea la documentación para desarrolladores de SharePoint Server 2013.
  
La aplicación de servicio de proyecto es un proveedor de servicio lógico que puede administrar varias instancias de Project Web App. Aprovisionamiento de Project Server, crea un sitio de Project Web App específico dentro de una aplicación web de SharePoint. La página principal de Project Web App contiene vínculos a la página Centro de proyectos, página del centro de recursos y la página del centro de inteligencia empresarial para informes, además de una página que contiene una lista de aplicaciones estándares adicionales. La figura 1 muestra el comando **Editar página** en la lista desplegable de **configuración** en la página principal de Project Web App, que permite agregar o editar elementos Web. 
  
> [!NOTE]
> Algunas páginas administrativas en Project Web App, como la página Configuración de PWA, no son editables y no mostrar el comando **Editar página** . Project Web App no permite editar páginas mediante SharePoint Designer 2013. Puede editar las páginas del sitio de proyecto con SharePoint Designer 2013. 
  
**En la figura 1. Mediante el menú Editar página de Project Web App**

![Edición de la página principal de Project Web Access] (media/pj15_Programmability_PWAHome.gif "Edición de la página principal de Project Web Access")
  
Para obtener acceso a la página Configuración del sitio de Project Web App, elija el icono de **configuración** en la esquina superior derecha de la página. La página Configuración del sitio ( `http://ServerName/ProjectServerName/_layouts/15/settings.aspx`) permite cambiar la apariencia y el tema del sitio, agregar elementos Web personalizados y modificar o crear páginas maestras de los sitios de proyecto.
  
Personalización del código en las páginas ASPX o personalización de las páginas maestras de Project Web App con SharePoint Designer 2013, no se admite. Personalización del código en las páginas de Project Web App puede causar problemas con los service packs y actualizaciones de Project Server. 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>Personalización de Project Web App con paquetes de SharePoint
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Debido a que Project Web App es una aplicación de SharePoint y los sitios de proyecto son sitios de SharePoint, puede agregar aplicaciones personalizadas, elementos Web, controladores de eventos, campos personalizados y otras características mediante el uso de paquetes de SharePoint (archivos .wsp) o aplicaciones de SharePoint (archivos .spapp). Un paquete de SharePoint o un paquete de aplicación puede incluir varias entidades de Project Server, donde se especifican las definiciones de entidad en un archivo elements.xml dentro del paquete.
  
Para Project Online, puede agregar botones a la cinta de opciones de Project Web App, pero no se puede quitar o cambiar el nombre de los botones de producto existente y no se puede crear nuevas fichas de la cinta de opciones. Para obtener más información, vea [crear acciones personalizadas para implementarlas con aplicaciones para SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx).
  
> [!CAUTION]
> Al instalar un paquete o un paquete de aplicación de SharePoint, los tipos de entidades de Project Server deben aparecer en el orden especificado por el esquema PSEntityProvision.xsd o se producirá un error en la validación del esquema del paquete y la instalación no se realizará. 
  
El archivo de esquema PSEntityProvision.xsd está disponible en la descarga del SDK de Project 2013, en la `Documentation\Schemas\AppProvisioning` subdirectorio. La figura 2 muestra la vista del explorador de esquema de XML en Visual Studio del esquema **PSEntityProvision** , donde se expande la secuencia **LookupTable** . 
  
**La figura 2. Vista de la entidad de Project Server aprovisionamiento de esquema de Visual Studio**

![Vista del esquema de entidad de Project Server] (media/pj15_Programmability_EntitySchema.gif "Vista del esquema de entidad de Project Server")
  
Paquetes de SharePoint que instalación las características de Project Server pueden contener uno o varios archivos de elements.xml que siguen el esquema de **PSEntityProvision** . Las entidades de Project Server en un único archivo XML deben aparecer en el orden siguiente: 
  
1. Fases de flujo de trabajo
    
2. Tablas de búsqueda
    
3. Campos personalizados
    
4. Fases de flujo de trabajo
    
5. Tipos de proyecto empresarial
    
6. Controladores de eventos
    
Al crear un paquete de SharePoint que contiene entidades de Project Server, es posible colocar las definiciones de entidad en varios archivos elements.xml. Cada archivo XML podría pasar la validación de esquema, pero las entidades de todo el paquete podrían no estar en el orden correcto. Por ejemplo, una entidad de campo personalizado del primer archivo XML podría referirse a una tabla de búsqueda del segundo archivo XML. Durante la instalación, no se podría crear el campo personalizado porque la tabla de búsqueda aún no se habría creado.
  
Si se produce un error en la instalación de un paquete, los objetos que se han creado permanecen en Project Web App, pero el paquete no se instala completamente. Puede volver a instalar el paquete de trabajo, pero no es una buena experiencia para los clientes. Cuando las definiciones de entidad abarcan varios archivos elements.xml, organizar las entidades de Project Server en todo el paquete de SharePoint para asegurarse de que la instalación sigue el orden correcto. Con el esquema de PSEntityProvision.xsd en la descarga del SDK de Project 2013, es posible desarrollar una herramienta que comprueba el orden indicado de las entidades en los archivos XML.
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Actualización de aplicaciones con las API de Project Server
<a name="pj15_Programmability_APIs"> </a>

Cuando se actualiza una aplicación que se ha desarrollado para una versión anterior de Project Server, puede usar el CSOM o la PSI para una interfaz de programación que incluye métodos para crear, leer, actualizar y eliminar entidades de proyecto (las operaciones CRUD). Aunque el CSOM llama internamente a la PSI, no sustituye completamente todos los métodos PSI. Para escenarios y las limitaciones de la PSI y del CSOM, consulte [What the PSI does and no hace](what-the-psi-does-and-does-not-do.md) y [el CSOM ¿qué hace y no hace](what-the-csom-does-and-does-not-do.md).
  
> [!NOTE]
> Si el CSOM incluye la funcionalidad que necesita, se recomienda actualizar aplicaciones para usar el CSOM. El CSOM permite que las aplicaciones que se usará para local y las instalaciones en línea de Project Server 2013. 
  
Si la aplicación lee principalmente datos de Project Server, puede usar las tablas y vistas de informes en la base de datos de Project Server para un escenario local. Si piensa usar la aplicación con Project Online, puede usar el Protocolo OData para el servicio **ProjectData** , que proporciona acceso en línea a los datos de informes y local. Para obtener más información, vea [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)
  
### <a name="using-the-psi"></a>Empleo de PSI
<a name="pj15_Programmability_PSI"> </a>

PSI permite a las aplicaciones cliente de plena confianza, incluidas las aplicaciones de LOB, Project Web App y Project Professional 2013, para tener acceso a datos de Project Server dentro de una granja de servidores de SharePoint. La PSI se genera y se utiliza con .NET Framework 4 y ofrece ventajas como un entorno de desarrollo conocidas con seguridad integrada, tratamiento de errores y colección de elementos no utilizados.
  
La PSI se tiene acceso a través de los servicios de WCF o servicios web de ASMX. La interfaz ASMX se basa en WCF. Normalmente, cada servicio de la PSI contiene una clase base con los métodos CRUD para los elementos dentro de esa clase. Los elementos se especifican mediante las clases de **conjunto de datos** relacionadas. Por ejemplo, el servicio de **CustomFields** contiene la clase **CustomFields** con métodos como [CreateCustomFields2](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.CreateCustomFields2.aspx) . Datos para uno o más campos personalizados de empresa se especifican en la **CustomFieldDataSet**.
  
> [!NOTE]
> La interfaz de servicios web ASMX de la PSI está en desuso en Project Server 2013. Aunque la interfaz ASMX sigue estando disponible, nuevas aplicaciones que usan la PSI deben usar la interfaz WCF o, si es posible, las nuevas aplicaciones deben utilizar el CSOM en lugar de la PSI. Las futuras versiones de Project Server requerirá una actualización de aplicaciones de basadas en ASMX existentes para utilizar la interfaz WCF de la PSI o para usar el CSOM. 
  
Hay 22 público, documentado servicios PSI, que se duplican en la interfaz WCF y la interfaz ASMX. PSI también incluye ocho servicios no están documentados, privados. Project Web App y Project Professional usan los servicios de PSI pública y los servicios PSI privados. Por lo general se divide la PSI para que coincidan con los objetos de negocios. Es decir, cada método PSI está asociado con un objeto de negocio como **calendario** o un **recurso**. La PSI es la interfaz principal para los objetos de negocios. Debido a que la capa de negocios proporciona componentes de lógica empresarial reutilizables, diferentes aplicaciones que interactúan con datos de Project Server usan la misma lógica de negocios.
  
Métodos PSI que interactúan de forma asincrónica con Project Server tienen nombres que comienzan con la **cola**. Cada método PSI se implementa con una interfaz independiente que usa inflexible de datos. Por ejemplo, el método **QueueCreateProject** en el servicio de **proyecto** acepta el parámetro de _conjunto de datos_ del tipo de **ProjectDataSet**. La clase **ProjectDataSet** se deriva el tipo de **conjunto de datos** . Escriba la comprobación de la finalización de IntelliSense y de .NET Framework en la Ayuda de Visual Studio para reducir los errores en el desarrollo con la PSI. Para obtener una introducción a la referencia detallada para PSI espacios de nombres, clases, métodos, propiedades, eventos y ensamblados relacionados, vea [Descripción general de referencia de PSI de Project](project-psi-reference-overview.md).
  
Project Server 2013 usa el control de excepciones de .NET Framework. Todos los errores se registran en el servidor, en la parte superior de la pila de PSI. Algunos errores de envían un informe sencillo para el cliente, como un objeto **SoapException** para la interfaz ASMX o un objeto **FaultException** para la interfaz WCF. Excepciones que se pueden registrar en el registro de eventos de aplicación, y algunos errores también registran un informe detallado en el servidor en los registros de seguimiento del servicio de registro unificado (ULS). 
  
En las aplicaciones locales de plena confianza, PSI además es extensible. Es posible agregar un ensamblado de .NET con un servicio que proporciona nuevas características, usa la misma infraestructura de seguridad de Project Server y llama a otros métodos de PSI o hereda de clases de PSI. Una extensión de PSI también puede proporcionar la lógica empresarial y el acceso de base de datos necesarios para la nueva funcionalidad.
  
### <a name="using-the-csom"></a>Empleo del CSOM
<a name="pj15_Programmability_CSOM"> </a>

Con el CSOM, puede desarrollar aplicaciones que tienen acceso a Project Online o una instalación de Project Server 2013 local. En un almacén de Office pública o un catálogo de aplicaciones privada se pueden distribuir aplicaciones. El CSOM está diseñado para ser una API fácil de usar que consume directamente o proporciona datos por su nombre con las consultas LINQ, en lugar de pasar los conjuntos de datos y construcción _changeXml_ parámetros o parámetros de _filtro_ XML. El CSOM implementa la funcionalidad principal de Project Server Interface (PSI) para las entidades principales como **proyecto**, **tarea**, **EnterpriseResource**y **asignación**. El CSOM incluye muchas entidades de adicionales como **CustomField**, **LookupTable**, **WorkflowActivities**, **EventHandler**y **QueueJob**, que admite otras funciones de Project Server comunes.
  
El CSOM se puede usar copiando los siguientes recursos en el equipo de desarrollo local:
  
- Para el desarrollo de .NET Framework 4, copie el `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll` ensamblado. 
    
  Para obtener documentación sobre las clases CSOM y miembros, vea el espacio de nombres [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . Para una aplicación de ejemplo, vea [Getting started with el CSOM y. NET](getting-started-with-the-project-server-csom-and-net.md).
    
- Para el desarrollo de Microsoft Silverlight, copie la `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll` ensamblado. 
    
- Para desarrollar aplicaciones para Windows Phone 8, copie la `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll` ensamblado. 
    
- Para utilizar JavaScript para el desarrollo de aplicaciones web y aplicaciones para otros dispositivos, copie la `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` archivo y la `PS.debug.js` archivo. Para una aplicación web de ejemplo, vea [Getting started with el modelo de objetos de JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md).
    
El CSOM llama internamente a la PSI; por lo tanto, si la interfaz PSI no puede hacer un trabajo, puede ni el CSOM. Para conocer las limitaciones del CSOM, consulte [el CSOM ¿qué hace y no hace](what-the-csom-does-and-does-not-do.md) y [What the PSI hace y no hace](what-the-psi-does-and-does-not-do.md). Para obtener más información sobre el desarrollo con el CSOM, vea [actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md) y [modelo de objetos de cliente (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="porting-applications-built-for-project-server-2003"></a>Aplicaciones de migración compiladas para Project Server 2003
<a name="pj15_Programmability_Porting2003"> </a>

En Project Server 2003, muchos datos y funciones solo están disponibles con Project Professional 2003 o mediante acceso directo de base de datos. PSI, introducida en Project Server 2007, elimina en gran medida esa restricción. A diferencia de Project Data Service (PDS) de Project Server 2003, PSI y el CSOM proporcionan interfaces generales para objetos empresariales de Project Server.
  
Las aplicaciones desarrolladas para PDS no son compatibles con versiones posteriores de Project Server. El CSOM y PSI proporcionan paridad funcional para PDS, pero no coinciden con los métodos o parámetros de PDS.
  
> [!NOTE]
> Debido a que las aplicaciones de PDS deben deben rediseñarse por completo para Project Server 2013, se recomienda que use el CSOM. 
  
Para obtener más información acerca de la compatibilidad de PDS y directrices para las extensiones PDS a la PSI, consulte [PDS Parity in PSI Web Services](http://msdn.microsoft.com/library/61a0b0c7-9b74-46d1-87ed-66ffdd8017f8%28Office.15%29.aspx).
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Aplicaciones de migración compiladas para Project Server 2007 y Project Server 2010
<a name="pj15_Programmability_Porting2007"> </a>

La PSI de Project Server 2013 es un superconjunto del modelo de objetos PSI en Office Project Server 2007 y Project Server 2010. Muchas aplicaciones creadas para las dos versiones anteriores de Project Server seguirán funcionando en instalaciones locales de local de plena confianza, de Project Server 2013. Sin embargo, los siguientes tipos de aplicaciones requieren actualizaciones o cambio de diseño:
  
- Use CSOM para aplicaciones adaptadas para su uso con Project Online.
    
- Use el CSOM para aplicaciones adaptadas para su empleo en dispositivos móviles y tabletas.
    
- Use CSOM para aplicaciones que están disponibles como aplicaciones en la tienda de Office o en un catálogo de aplicaciones privada.
    
- Para las aplicaciones que modifican la programación de proyectos, use el CSOM o cambie la aplicación para que utilice el método PSI [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) . 
    
- Local o aplicaciones web que inicie sesión en instancias diferentes de Project Web App a los usuarios deben usar valores mediante programación para los extremos WCF de CSOM o la PSI. Los métodos están en desuso. Aplicaciones deben usar la autenticación de OAuth en lugar de la autenticación de formularios y para su uso con Project Online. Para obtener más información, vea [autorización y autenticación para aplicaciones en SharePoint 2013](http://msdn.microsoft.com/en-us/library/fp142384%28office.15%29.aspx#FileName_uniquekeyword1).
    
- Aplicaciones que se basan en una configuración concreta de seguridad de Project Server o la modifican.
    
  > [!NOTE]
  > Una instalación local de predeterminada de Project Server 2013 usa el modo de permiso de SharePoint, donde la configuración de seguridad de Project Server no es accesibles a través de la PSI. Para cambiar al modo de permiso de Project, vea la sección *Modo de permisos de SharePoint* en [Novedades para los profesionales de TI en Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx#section13). 
  
- Para muchos Project Server flujos de trabajo personalizados, puede usar SharePoint Designer 2013 para crear flujos de trabajo declarativos. Para flujos de trabajo personalizados que requieren programación adicional, debería usar *no* directamente clases o miembros en el espacio de nombres **Microsoft.Office.Project.Server.Workflow** . En su lugar, use la clase [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) en el CSOM. 
    
- En general, deben volver a escribir aplicaciones que usan la suplantación para usar la interfaz WCF de la PSI. Las aplicaciones que implican las actualizaciones de estado simple para otros usuarios no requiere suplantación. Puede usar el método [StatusAssignment.SubmitStatusUpdates](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.StatusAssignment.SubmitStatusUpdates.aspx) en el CSOM o el método [Statusing.SubmitStatusForResource](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.SubmitStatusForResource.aspx) en la interfaz PSI. 
    
- Componentes de software intermedio que se ejecutan en el equipo de Project Server pueden instalarse solo para uso local y deben usar la interfaz WCF de la PSI. Por ejemplo, un componente de software intermedio que usa el ASMX de la interfaz para intercambiar datos entre local de Project Web App y una aplicación de partes de horas externos tendría que volver a escribir para usar la interfaz WCF de la PSI. Para trabajar con Project Online, el componente tendría que se ha diseñado como una aplicación y usar el CSOM.
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>Migración y compatibilidad de soluciones personalizadas
<a name="pj15_Programmability_CustomSolutions"> </a>

Clases y miembros en las interfaces ASMX y WCF públicas de la PSI son idénticos. Pero el número de columnas y el tamaño de tablas de datos que usan o devuelto por los métodos PSI pueden ser diferentes entre Project Server 2013 y las dos versiones anteriores de Project Server. También existen diferencias en las tablas y vistas, en comparación con la base de datos de informes en las versiones anteriores de informes.
  
> [!IMPORTANT]
> Se recomienda encarecidamente probar a fondo las soluciones en una instalación que no sea de producción de Project Server 2013 antes de implementarlas en un servidor de producción. 
  
Al migrar una solución a Project Server 2013, o si una solución no funciona como se esperaba, debería como mínimo hacer lo siguiente:
  
- Actualice la solución, puede abrirlo en Visual Studio 2012. Algunas soluciones también pueden usar Visual Studio 2010.
    
- Cambie el destino a .NET Framework 4.
    
- Cambiar las referencias de ensamblado para usar los ensamblados de Project Server 2013, como Microsoft.Office.Project.Server.Library.dll y Microsoft.Office.Project.Server.Events.Receivers.dll.
    
- Hacer una lista de las referencias web ASMX o las referencias del servicio WCF y los espacios de nombres y, a continuación, eliminar las referencias de Project Server.
    
- Agregue el ensamblado de proxy ProjectServerServices.dll que puede crear a partir de los archivos de origen del proxy WCF en la descarga del SDK de Project 2013, o agregar los archivos de origen de proxy para los servicios WCF necesarios. Para los servicios ASMX, agregue las referencias de servicio web de ASMX front-end de nuevo, mediante el uso de los mismos nombres de espacio de nombres; o bien, agregue el ensamblado de proxy ProjectServerServices.dll que se puede generar desde los orígenes de WSDL en la descarga del SDK de Project 2013.
    
  > [!NOTE]
  > En la descarga del SDK de Project 2013, los espacios de nombres en el origen de proxy los archivos de todos los inicio con *Svc* . Por ejemplo, el espacio de nombres del servicio de **recursos** en el archivo de proxy WCF y en el archivo de proxy ASMX es **SvcResource**. > Si la aplicación utiliza los nombres de espacio de nombres diferente, puede volver a compilar el ensamblado de proxy para usar los espacios de nombres, o cambiar los espacios de nombres PSI en la aplicación. Por ejemplo, puede modificar la secuencia de comandos CompileWCFProxyAssembly.cmd y volver a compilar ProjectServerServices.dll desde los archivos de origen de proxy en la descarga del SDK. 
  
- Si cambia de uso de la interfaz ASMX de la PSI para la interfaz WCF, se pueden inicializar las clases de cliente mediante programación o mediante el uso de los extremos WCF en app.config. Use la inicialización mediante programación cuando tenga que cambiar rápidamente a distintas instancias de Project Web App, o cuando está desarrollando un elemento web que usa la interfaz PSI.
    
- Existen varios métodos nuevo y conjuntos de datos en los servicios de PSI de Project Server 2013 y algunas clases **DataRow** contienen nuevas propiedades. Por ejemplo, el método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) en la interfaz PSI usa el servidor Project Server motor de programación para volver a programar un proyecto actualizado sin tener que abrir el proyecto en Project Professional 2013 y también permite agregar o eliminar entidades de proyecto en la misma llamada. 
    
- Compilar y probar la solución.
    
## <a name="project-scheduling-on-the-server"></a>Programación de proyectos en el servidor
<a name="pj15_Programmability_Scheduling"> </a>

Project Server 2013 tiene dos motores de programación. El motor de programación más reciente es el mismo que el motor de programación de Project Professional 2013. Cuando realice los cambios de programación y publique los cambios mediante el elemento web de programación (página de detalles del proyecto) en Project Web App o un sitio de proyecto, o con el CSOM, el cálculo de las fechas, los costos, duración, trabajo restante, las líneas de base y otros cambios relacionados con a la programación son los mismos como si se realizan los cambios y publica el proyecto mediante Project Professional 2013. Sin embargo, excepto el método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) , los métodos PSI usan el motor de programación más antiguos que se ha migrado de Project Server 2010. La razón es para asegurarse de que las aplicaciones heredadas comportan del mismo en Project Server 2013 tal como lo hacían anteriormente. 
  
> [!NOTE]
> Para usar el motor de programación actualizado en Project Server 2013, las aplicaciones pueden usar el CSOM. 
  
Tanto los motores de programación más antiguos como los más modernos tienen las siguientes limitaciones:
  
- **Único proyecto solo de programación** Programación afecta sólo en el proyecto actual, cuando se realizan cambios a través de las actualizaciones de estado de tareas con la PSI o CSOM, o con Project Web App. Si el proyecto actual tiene vínculos a otros proyectos, subproyectos o proyectos principales, no se cambiarán los proyectos vinculados. 
    
- **Tareas de resumen** Las tareas de resumen son normalmente de sólo lectura en Project Server. Por ejemplo, no se puede crear las asignaciones de tareas de resumen y no se puede modificar el porcentaje de finalización. Sin embargo, Project Server admite la edición las fechas y la duración de las tareas de resumen programadas manualmente. 
    
    Los datos reales no se agregan automáticamente a una asignación de tarea de resumen en Project Server, porque eso omitiría el proceso de aprobación de Project Server. En Project Professional, al agregar datos reales a una subtarea, también se agregan para una asignación de la tarea de resumen. La diferencia de comportamiento puede ser confusa para un usuario.
    
    Project Server elimina los datos reales de una asignación de tarea de resumen si la duración de la subtarea se acorta o se modifica la fecha de finalización.
    
    > [!CAUTION]
    > Aunque Project Professional puede hacerlo, le recomendamos que no haga asignaciones en tareas de resumen. 
  
A continuación se enumeran los problemas y las limitaciones de la programación de PSI con el motor de programación más antiguo de Project Server:
  
- **Cambio del estado activo de una tarea** El motor de programación de Project Server más antiguos puede mostrar incoherente inicio o de finalización veces cuando utilice el método [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) para cambiar el estado activo de una tarea, si hay varios cambios en el objeto **ProjectDataSet** para el _ conjunto de datos_ parámetro. Si la propiedad **TASK_IS_ACTIVE** es el único cambio en el parámetro de _conjunto de datos_ de **QueueUpdateProject**, puede actualizar el proyecto.
    
    Para obtener más información acerca de las tareas inactivas y el motor de programación más antiguos, consulte el blog de artículos de [Introducción de las tareas inactivas en Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx) y [Project Server 2010: programación en el web, la PSI y Project Professional](http://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0). Para obtener una comparación de programación en Project Professional 2010 y Project Web App en Project Server 2010, consulte [comparación de administración de programación basada en Web](http://www.microsoft.com/project/en/us/project-server-2010-editions.aspx).
    
- **No calcula el valor acumulado** El motor de programación más antiguos no calcula los campos de valor acumulado: CRTR, CPF, CPTR, CPTP, IRC, VC, VC %, CEF, SPI, VP, VP %, IRPC, VAF, variación de duración, variación de comienzo, variación de fin, variación de costo y variación de trabajo. Si un proyecto tiene los valores de estos campos y el proyecto se actualiza mediante el método **QueueUpdateProject** , no cambie los valores de campo. Para evitar el problema, use el método **QueueUpdateProject2** . 
    
Puede controlar las limitaciones de la programación de PSI de varias formas:
  
- Si el CSOM tiene los métodos que necesita la aplicación, utilícelo en lugar de PSI.
    
- Abra los proyectos en Project Professional y vuelva a guardarlos en Project Server.
    
- En los informes, no incluya campos que PSI no actualice.
    
- Agregue una nota en los informes que indique que los datos pueden estar obsoletos.
    
En las tablas de informes y los cubos hay marcas que ayudan a detectar si algunos datos de un proyecto no están actualizados. Los datos de informes de la tabla MSP_EpmProject de MSP_EpmProject_UserView incluyen los siguientes campos: 
  
-  _ProjectWbsIsStale_ &ndash; Indica si la estructura de descomposición del trabajo (jerarquía del esquema de tareas) es obsoleta. 
    
-  _ProjectEarnedValueIsStale_ &ndash; Indica los campos de valor acumulado están obsoletos. 
    
-  _ProjectRollupsAreStale_ &ndash; Indica que un subproyecto se actualiza en la base de datos de borrador, pero no se actualiza el proyecto principal. Los valores del subproyecto están obsoletos. 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; El proyecto principal no está sincronizado con sus elementos secundarios. Esto sucede cuando los proyectos secundarios se publican explícitamente, no como parte de la publicación del proyecto principal. 
    
-  _ProjectCalculationsAreStale_ &ndash; Project Professional ha guardado un proyecto sin calcular el programa (es decir, el modo de cálculo se establece en **Manual** en la ficha **programación** en el cuadro de diálogo **Opciones de proyecto** ). 
    
-  _ProjectGhostTaskAreStale_ &ndash; Es Similar a _ProjectHierarchyNotSynchronized_, pero le advierte en datos de vínculos entre proyectos. Es posible que no existe ningún proyecto maestro, pero los datos del proyecto en un lado del vínculo están más recientes que en el otro lado.
    
## <a name="about-accessing-the-project-server-database"></a>Acerca del acceso a la base de datos de Project Server
<a name="pj15_Programmability_Databases"> </a>

Si tiene permisos en Microsoft SQL Server para tener acceso a la base de datos de Project Server, puede leer las tablas y vistas de informes. Si tiene los permisos necesarios de Project Server, puede leer los datos de las tablas de informes mediante el uso de consultas OData. Los desarrolladores se recomienda encarecidamente no tengan acceso directamente a la borrador, publicado, o archivar tablas a través de consultas de SQL Server en la base de datos de Project Server. Realizar cambios directos en cualquiera de las tablas de la base de datos de Project Server puede dañar la integridad referencial e interferir con acceso de base de datos a través del servicio de puesta en cola de Project Server.
  
> [!IMPORTANT]
> No hay nada que le impida activamente usar el acceso de base de datos directo mediante programación para actualizar datos. Debería tener en cuenta de que la caché de Project Professional, las tablas de publicados y las tablas de informes dependen de un protocolo de sincronización de la caché que se puede alterar por la edición directa de datos. Si daña la base de datos de Project Server o las cachés de cliente de Project Professional mediante el acceso directo para cambiar datos, sepa que el servicio de soporte del producto no podrá prestarle ayuda. 
  
Las aplicaciones que tienen acceso directamente a la borrador, publicados o archivar las tablas y vistas también son dependientes de los esquemas de base de datos, que pueden cambiar en el service Pack o versiones posteriores de Project Server 2013. Las aplicaciones que tienen acceso directamente a las bases de datos también pierden la seguridad integrada en Project Server, lógica de negocios comunes, seguimiento, las auditorías, comprobación de errores, informes, flujo de trabajo y otras características. Es probable que tendría que volver a escribir una aplicación de este tipo después de las actualizaciones de Project Server 2013. 
  
Para todos estos motivos, Project Professional y Project Web App no realizan llamadas directas a la borrador, publicado, o archivar tablas; tampoco deberían cualquier otra aplicación que se integra con Project Server.
  
Los esquemas del borrador, publicado, y tablas de archivo no se documentan. Puede usar las tablas de informes para ayudar a generar informes y se documenta el esquema de las tablas y vistas de informes en la descarga del SDK de Project 2013. Para el esquema de OData de los datos de informes, consulte [ProjectData: referencia de servicio OData de Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
## <a name="see-also"></a>Ver también

- [Actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md)    
- [Arquitectura de Project Server 2013](project-server-2013-architecture.md)    
- [Lo que hace y no hace la PSI](what-the-psi-does-and-does-not-do.md)   
- [Lo que hace y no hace el CSOM](what-the-csom-does-and-does-not-do.md)    
- [Modelo de objetos de cliente (COM) de Project 2013](client-side-object-model-csom-for-project-2013.md)    
- [Comenzar desarrollar flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md)    
- [Referencias de programación de Project 2013](project-2013-programming-references.md)    
- [Información general de referencia PSI de Project](project-psi-reference-overview.md)    
- [Crear acciones personalizadas para implementarlas con aplicaciones para SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx)    
- [Introducción a las tareas inactivas en Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010: Programación en el Web, la PSI y Project Professional](http://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0)
- [Comparación de la administración de programación basada en Web](http://www.microsoft.com/project/en/us/project-server-2010-editions.aspx)
    

