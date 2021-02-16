---
title: Desarrollo de un complemento de Project Online con el modelo de objetos de JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: En este artículo se describe el desarrollo de complementos de Microsoft Project Online para mejorar su experiencia con Project Online. El proyecto de desarrollo se implementa como un tutorial. El complemento que se usa para este artículo lee y muestra los nombres de proyecto e IDs de los proyectos publicados desde su cuenta de Project Online y le permite explorar en profundidad para recuperar tareas asociadas a proyectos individuales.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322697"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desarrollo de un complemento de Project Online con el modelo de objetos de JavaScript (JSOM)

En este artículo se describe el desarrollo de complementos de Microsoft Project Online para mejorar su experiencia con Project Online. El proyecto de desarrollo se implementa como un tutorial. El complemento que se usa para este artículo lee y muestra los nombres de proyecto e IDs de los proyectos publicados desde su cuenta de Project Online y le permite explorar en profundidad para recuperar tareas asociadas a proyectos individuales.
  
En tiempo de ejecución, la descripción del complemento es similar a la siguiente ilustración:
  
![Captura de pantalla que muestra una lista de proyectos y]tareas de JSOM Captura de pantalla que muestra una lista de proyectos y tareas de(media/766e5914-f048-48f4-9282-291f55e6e90d.png "JSOM")
  
El foco del ejemplo es la interacción con Project Online, realizar consultas y establecer el contexto para cada solicitud del servicio. Los elementos de la interfaz de usuario reciben una atención mínima. En su lugar, las listas de origen proporcionan comentarios sobre la interfaz de usuario.
  
> [!NOTE]
> Los archivos de origen del complemento de ejemplo, un Visual Studio proyecto, están disponibles en: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . Mantenga los archivos de origen a mano como referencia mientras lee el artículo, ya que cada uno complementa al otro. Los archivos de la Visual Studio compilación del proyecto y son ejecutables con cambios mínimos, sustituyendo la dirección URL del inquilino de Project Online a la carpeta de PWA. 
  
## <a name="background"></a>Información previa

Project Online es un servicio de Office 365 que proporciona a las empresas una solución de administración de carteras de proyectos (PPM) y una oficina de administración de proyectos (PMO) para coordinar y administrar carteras, programas y proyectos. Project Online es una oferta diferente de las ediciones de escritorio de Project; sin embargo, Project Online aún contiene la funcionalidad para mantener y realizar un seguimiento de los detalles del proyecto a lo largo de la vida de un proyecto. Project Online se basa en SharePoint Online.
  
Un complemento hospedado de Project Online consta de JavaScript y archivos de recursos que interactúan con la API del modelo de objetos del lado cliente. Cuando el usuario visita el complemento, el JavaScript y los recursos se descargan y ejecutan en el explorador. El complemento realiza llamadas asincrónicas a Project Online para interactuar con el servicio, ya sea creando, recuperando, actualizando o eliminando datos. 
  
Project Online realiza una acción más para proteger la información que pertenece a otros inquilinos del complemento; es decir, Project Online crea un sitio aislado para interactuar con las solicitudes del complemento. No se ejecuta ningún código personalizado en el host de Project Online. 
  
La configuración de desarrollo para complementos de Project Online usa el Visual Studio proyecto de complemento de SharePoint. El complemento está escrito en JavaScript y usa el modelo de objetos de JavaScript (JSOM) de Project para interactuar con el servicio de Project Online. JSOM hereda gran parte de su funcionalidad del JSOM de SharePoint.
  
> [!NOTE]
> Los complementos se pueden publicar y vender en la Tienda Office o implementarse en un catálogo de aplicaciones privado en SharePoint. Para obtener más información, vea [Implementar y publicar el complemento de Office.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)
> 
> El complemento que se usa en este artículo es un ejemplo para desarrolladores; no está pensado para su uso en un entorno de producción. El propósito principal es mostrar un ejemplo de desarrollo de aplicaciones para Project Online. 
  
## <a name="prerequisites"></a>Requisitos previos

Agrega los siguientes elementos a un entorno de Windows compatible:
  
- **.NET Framework 4.0 o** posterior: las versiones completas del marco de la versión 4.0 son compatibles. El sitio de descarga es https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 o posterior:**  
    
   - La edición profesional de Visual Studio 2015 está lista para usarse y está disponible en https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx .
    
   - La edición de la Visual Studio 2015 está disponible en https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx . Esta edición requiere la instalación manual de Microsoft Office Developer Tools para Visual Studio.
    
   Las Microsoft Office Developer Tools para Visual Studio están disponibles en https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .
    
- **Una cuenta de Project Online:** proporciona acceso al servicio de hospedaje. Para obtener más información acerca de cómo obtener una cuenta de Project Online, vea https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Asegúrese de que el usuario del complemento tiene autorización suficiente para tener acceso a algunos proyectos en el inquilino de Project Online. 
    
- **Proyectos en el sitio de hospedaje** que se rellenan con información.
    
> [!NOTE]
> .NET Framework estándar es el marco correcto para usar. No use el "perfil de cliente de .NET Framework 4". 
  
### <a name="set-up-the-visual-studio-project"></a>Configuración del proyecto de Visual Studio

La configuración de la aplicación consiste en crear un nuevo proyecto, vincular las bibliotecas adecuadas y declarar los espacios de nombres necesarios. Visual Studio presenta varios tipos de proyectos de desarrollo. La sección es breve y muy básica. El valor es que la información se une en un solo lugar.
  
#### <a name="select-a-visual-studio-project"></a>Seleccionar un proyecto de Visual Studio

Para crear un proyecto del tipo adecuado para el complemento, debe realizar los siguientes pasos. Las palabras clave encontradas en la pantalla tienen un atributo **de** negrita: 
  
1. En el menú Archivo, elija **Archivo**  >  **nuevo**  >  **proyecto.** 
    
2. En las plantillas instaladas en el panel izquierdo, seleccione **Complementos web** de  >  **Office/SharePoint**  >  **de** C#. 
    
3. En la parte superior del panel central, seleccione **.NET Framework 4** o posterior; la versión actual es 4.6. 
    
4. En los tipos de aplicación del panel central, elija **Complemento de SharePoint.** 
    
5. En la sección inferior, especifique un nombre y una ubicación para el proyecto, así como un nombre de la solución. 
    
6. También en la sección inferior, active la casilla **Crear directorio para la solución**. 
    
7. Haga clic en **Aceptar** para crear un proyecto inicial. 
    
El asistente Visual Studio hace algunas preguntas de seguimiento sobre el sitio de configuración de Project Online (denominado configuración de SharePoint en los cuadros de diálogo) en un par de cuadros de diálogo que se abren a continuación. Estas son las preguntas:
  
1. ¿Qué sitio de SharePoint desea usar para depurar el complemento? Especifique la dirección URL del sitio de PWA, como https://contoso.sharepoint.com/sites/pwa .
    
2. ¿Cómo desea hospedar el complemento de SharePoint? Elija [X] **hospedado en SharePoint.**
    
   Para obtener más información acerca de los complementos de SharePoint, incluidas las opciones de hospedaje, vea [Complementos de SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Haga clic en **Siguiente**. 
    
El segundo cuadro de diálogo adicional le pide que especifique la versión de SharePoint Online para el complemento: 
  
1. ¿Cuál es la versión más antigua de SharePoint a la que quiere que se dirigirá el complemento? Elija [X] S **harePoint-Online**. 
    
2. Haga clic en **Finalizar**. 
    
Visual Studio crea el proyecto y accede al sitio de Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar la instalación de instalación local en el sitio de Project Online

La instalación de prueba es el mecanismo para probar y depurar complementos de Project Online. Necesita dos scripts para la instalación de prueba: uno para habilitar la instalación de prueba en el sitio de Project Online y otro para deshabilitar la instalación de prueba una vez que termine de probar y depurar el complemento.
  
Para obtener más información acerca de la configuración de la instalación de instalación de local, vea Habilitar la instalación de instalación local de aplicaciones en la colección de sitios para no [desarrolladores.](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)
  
> [!NOTE]
> La instalación de prueba de aplicaciones es una característica para desarrolladores y pruebas. No está **pensado para uso de producción.** No realices la instalación de prueba de aplicaciones periódicamente o mantén habilitada la instalación de prueba de la aplicación durante más tiempo del que usas activamente la característica. 
  
## <a name="add-content-to-the-add-in-project"></a>Agregar contenido al proyecto de complemento

Después de crear un proyecto y configurar el mecanismo de depuración, agregar contenido a la aplicación incluye las siguientes tareas:
  
- Establecer el ámbito de la aplicación
    
- Vincular la biblioteca JSOM
    
- Agregar elementos de la interfaz de usuario al complemento
    
- Inicialización y conexión al servicio de Project Online
    
- Recuperación de proyectos y detalles/propiedades
    
- Mostrar proyectos
    
- Mostrar tareas para un proyecto
    
El proyecto de complemento consta de muchos archivos. En este ejemplo, tendrá que editar los archivos siguientes: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css: opcional; contiene definiciones de estilo desarrolladas para el complemento
    
Si el inquilino de Project Online cambia, como pasar de una versión de prueba a un sitio de suscripción, puede actualizar las propiedades del proyecto, incluida la conexión del servidor y la dirección URL del sitio, mediante la ventana Propiedades disponible a través del comando Ver ventana  >   propiedades. 
  
También puede agregar archivos al proyecto. Si es así, deberá actualizar el archivo Elements.xml ubicado en el mismo grupo (contenido, imágenes, páginas o scripts) para incluir los nuevos archivos. Para obtener más información acerca de los archivos de proyecto, vea Explorar la estructura del manifiesto de la aplicación y [el paquete de un complemento de SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Establecer ámbito de aplicación

El complemento necesita niveles de ámbito o permisos definidos antes de que el servicio devuelva información en los resultados de la consulta. Para este complemento, use el siguiente ámbito para el Visual Studio proyecto. Este cambio se realiza en el archivo AppManifest.xml en la pestaña Permisos:

|Ámbito|Permiso|
|:-----|:-----|
|Varios proyectos (Project Server)  <br/> |Lectura  <br/> |
   
Guarde el archivo después de establecer el ámbito de la aplicación. De lo contrario, no se devolverán datos del servicio. 
  
### <a name="link-the-jsom-library"></a>Vincular la biblioteca JSOM

Las bibliotecas de Project Online en tiempo de ejecución, PS.js y PS.debug.js, las proporciona Project Online y son siempre la versión más reciente. Los complementos de JavaScript que usan JSOM deben vincularse con una de estas bibliotecas. Las definiciones de vinculación se agregan en el archivo Default.aspx. Los comandos para usar el PS.js y/o PS.debug.js forman parte del código que se encuentra en el App.js archivo.
  
Agregue el siguiente comando para PS.js o PS.debug.js definición en el elemento que sigue a  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` "SharePoint:ScriptLink" para sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> El **atributo OnDemand** para PS.js o PS.debug.js establecido en **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Agregar elementos de la interfaz de usuario al complemento

El complemento de ejemplo consta de algunos componentes. Las descripciones de elementos estáticos se encuentran en el archivo Default.aspx. Las descripciones de elementos dinámicos y el código de todos los componentes se encuentran en el App.js archivo. Para obtener comentarios sobre los componentes, consulte las listas de código fuente. Esta es una lista de los componentes de la interfaz de usuario en el complemento:
  
- El título
    
- Verbiage introductorio
    
- Botón para quitar tareas de la tabla
    
- Tabla que enumera el identificador y el nombre del proyecto, así como la información de la tarea.
    
- Botón Tareas (clonado una vez para cada proyecto) que importa datos de tareas en la tabla.
    
Para obtener detalles de la interfaz de usuario, como el título y la parte de encabezado de la tabla del proyecto, vea el archivo de proyecto Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar y conectarse al sistema host

El App.js contiene el código JavaScript. El complemento carga los PS.js en el explorador y, a continuación, llama a la función initializePage. InitializePage recupera un contexto para el extremo de Project Online e inicia la función loadProjects.
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a>Recuperar los proyectos

La función loadProjects consulta al servicio los nombres de proyecto e IDs. 
  
La aplicación recupera el nombre del proyecto y el identificador del proyecto. Otra información sobre el proyecto está disponible y se puede obtener acceso modificando el método de carga para identificar explícitamente las propiedades que se recuperarán. En el código se proporciona un ejemplo como comentario. 
  
Si la consulta se realiza correctamente, el complemento continúa llamando a displayProjects. 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a>Mostrar los proyectos

La función displayProjects crea una tabla, una fila por proyecto y un botón para mostrar las tareas del proyecto específico. 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> El bucle while tiene acceso a las propiedades id. y name. Esto es ligeramente diferente al proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Mostrar las tareas de un proyecto

Las tareas, aunque forman parte del complemento, no forman parte de la carga inicial. Si el usuario está interesado en las tareas asociadas a un proyecto, al hacer clic en el botón "Mostrar tareas", las tareas se mostrarán en la lista mediante el controlador de eventos btnLoadTasks. 
  
El controlador de eventos btnLoadTasks, con el identificador de proyecto adecuado, solicita las tareas para el proyecto especificado del servidor. Una vez recuperado, btnLoadTasks pasa la lista de tareas a displayTasks para presentar las tareas en pantalla.
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

La función displayTasks muestra las tareas asociadas a un proyecto especificado inmediatamente debajo de la entrada del proyecto.
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> El bucle while tiene acceso a las propiedades id. y nombre de tarea. Esto es ligeramente diferente al proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
A continuación se muestra el resultado de ejemplo de las tareas de un único proyecto.
  
![Captura de pantalla que muestra el resultado de una captura de pantalla de tarea]de proyecto que muestra la salida de una tarea de(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "proyecto")
  
## <a name="see-also"></a>Vea también

Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).
    


