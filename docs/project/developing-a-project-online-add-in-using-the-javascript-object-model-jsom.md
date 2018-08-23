---
title: Desarrollo de un complemento Project Online mediante el modelo de objetos de JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: En este artículo se describe el desarrollo de Microsoft Project Online Add-in para mejorar su experiencia con Project Online. El proyecto de desarrollo se implementa como un tutorial. El complemento utilizado para este artículo lee y muestra los nombres de proyecto y los identificadores de los proyectos publicados desde su cuenta de Project Online y le permite profundizar en las tareas de recuperación asociadas con proyectos individuales.
ms.openlocfilehash: ea5c7e3f3d20aa6bf5b6bb77a18eb87d06f549e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572546"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desarrollo de un complemento Project Online mediante el modelo de objetos de JavaScript (JSOM)

En este artículo se describe el desarrollo de Microsoft Project Online Add-in para mejorar su experiencia con Project Online. El proyecto de desarrollo se implementa como un tutorial. El complemento utilizado para este artículo lee y muestra los nombres de proyecto y los identificadores de los proyectos publicados desde su cuenta de Project Online y le permite profundizar en las tareas de recuperación asociadas con proyectos individuales.
  
En tiempo de ejecución, el listado de agregar tenga un aspecto similar a la siguiente ilustración:
  
![Captura de pantalla que muestra una lista de proyectos JSOM y tareas] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Captura de pantalla que muestra una lista de proyectos JSOM y tareas")
  
El enfoque del ejemplo es la interacción con el proyecto en línea, tomar las consultas y de establecer el contexto de cada solicitud desde el servicio. Elementos de la interfaz (IU) de usuario reciben atención mínima. En su lugar, los listados de origen proporcionan comentarios acerca de la interfaz de usuario.
  
> [!NOTE]
> Los archivos de origen para el complemento de ejemplo, un proyecto de Visual Studio, están disponibles en: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Conservar los archivos de origen útil como una referencia al leer el artículo, cuando cada uno de ellos complementa la otra. Compilación del proyecto de los archivos en Visual Studio y son ejecutables con un mínimo de cambios, sustituyendo la dirección URL para el inquilino de Project Online hacia abajo hasta la carpeta de PWA. 
  
## <a name="background"></a>Fondo

Project Online es un servicio de Office 365 que proporciona a las empresas con una administración de carteras de proyectos (PPM) y la solución de office (PMO) de administración de proyectos para coordinar y administrar proyectos, programas y carteras de proyectos. Project Online es una oferta diferente que las ediciones de escritorio de Project; Sin embargo, Project Online todavía contiene la funcionalidad para mantener y realizar un seguimiento de los detalles del proyecto a lo largo de la vida de un proyecto. Project Online se basa en SharePoint Online.
  
Un complemento de Project Online hospedado consta de los archivos JavaScript y recursos que interactúan con la API de cliente-lado-modelo de objetos. Cuando el usuario visita el complemento, el JavaScript y los recursos se descargan y ejecutan dentro del explorador. El complemento realiza llamadas asincrónicas a Project Online para interactuar con el servicio, si crear, recuperar, actualizar o eliminar datos. 
  
Project Online lleva a cabo una acción más para proteger la información que pertenece a otros inquilinos desde el complemento; es decir, Project Online, se crea un sitio aislado para interactuar con las solicitudes desde el complemento. No hay código personalizado se ejecuta en el host de Project Online. 
  
El programa de instalación de desarrollo para complementos Project Online utiliza el tipo de proyecto de Visual Studio SharePoint Add-in. El complemento está escrito en JavaScript y usa el modelo de objetos de JavaScript de Project (JSOM) para interactuar con el servicio de proyecto en línea. El JSOM de gran parte de su funcionalidad hereda el JSOM de SharePoint.
  
> [!NOTE]
> Complementos pueden publicados y se venden en la tienda Office o implementados en un catálogo de aplicaciones privada en SharePoint. Para obtener más información, vea [implementar y publicar su complemento Office](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/publish).
> 
> El complemento usado en este artículo es un ejemplo para desarrolladores; no está pensada para su uso en un entorno de producción. El propósito principal es mostrar un ejemplo de desarrollo de aplicaciones para Project Online. 
  
## <a name="prerequisites"></a>Requisitos previos

Agregue los siguientes elementos en un entorno de Windows compatible:
  
- **.NET framework 4.0 o posterior**: versiones completas del marco de trabajo de la versión 4.0 son compatibles. El sitio de descarga es https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 o posterior**:  
    
   - La edición professional de 2015 de Visual Studio está lista Ir fuera del cuadro y está disponible en https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - La edición de la Comunidad de 2015 de Visual Studio está disponible en https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. Esta edición requiere la instalación manual de Microsoft Office Developer Tools para Visual Studio.
    
   Están disponibles en Microsoft Office Developer Tools para Visual Studio https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Cuenta A Project Online**: Esto proporciona acceso al servicio de hospedaje. Para obtener más información acerca de cómo obtener una cuenta de Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Asegúrese de que el usuario tiene autorización suficiente para tener acceso a algunos proyectos en el inquilino Project Online. 
    
- **Proyectos en el sitio de hospedaje** que se rellenan con información.
    
> [!NOTE]
> El estándar de .NET Framework es el marco de trabajo correcto para usar. No use ".NET Framework 4 Client Profile". 
  
### <a name="set-up-the-visual-studio-project"></a>Configurar el proyecto de Visual Studio

El programa de instalación de la aplicación consiste en crear un nuevo proyecto, vinculación las bibliotecas adecuadas y declarar los espacios de nombres necesarios. Visual Studio presenta varios tipos de proyectos de desarrollo. La sección es muy básica y breve. El valor que tiene la información es fusionada en un solo lugar.
  
#### <a name="select-a-visual-studio-project"></a>Seleccione un proyecto de Visual Studio

Para crear un proyecto del tipo adecuado para el complemento, debe realizar los siguientes pasos. Palabras clave que se encuentra en la pantalla tienen un atributo **negrita** : 
  
1. En el menú archivo, elija **archivo** > **New** > **Project**. 
    
2. En las plantillas instaladas en el panel izquierdo, seleccione **C#** > **Office/SharePoint** > **Web Add-ins**. 
    
3. En la parte superior del panel central, seleccione **.NET Framework 4** o posterior; la versión actual es 4.6. 
    
4. En los tipos de aplicación en el panel central, elija **Agregar en SharePoint**. 
    
5. En la sección inferior, especifique un nombre y una ubicación para el proyecto y un nombre de la solución. 
    
6. También en la sección inferior, active la casilla **Crear directorio para la solución** . 
    
7. Haga clic en **Aceptar** para crear el proyecto inicial. 
    
El Asistente de Visual Studio realiza preguntas de seguimiento unas acerca del sitio de la configuración de Project Online (denominado configuración de SharePoint en los cuadros de diálogo) en un par de cuadros de diálogo que le siguen. Estas son las preguntas:
  
1. ¿Qué sitio de SharePoint desea usar para depurar el complemento? Especificar la dirección URL del sitio de PWA, tales como https://contoso.sharepoint.com/sites/pwa.
    
2. ¿Cómo desea hospedar su Add in SharePoint? Elija [X] **hospedada en SharePoint**.
    
   Para obtener más información acerca de SharePoint Add-ins, incluidas las opciones de hospedaje, vea [SharePoint Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Haga clic en **Siguiente**. 
    
El segundo cuadro de diálogo adicional en el que se le pide que especifique la versión de SharePoint Online para el complemento: 
  
1. ¿Qué es la versión más antigua de SharePoint que desea que el complemento en el destino? Elija [X] S **SharePoint Online**. 
    
2. Haga clic en **Finalizar**. 
    
Visual Studio crea el proyecto y se tiene acceso al sitio de Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar sideloading en el sitio de Project Online

Sideloading es el mecanismo para probar y depurar los complementos Project Online. Necesita dos secuencias de comandos para sideloading: uno para habilitar sideloading en su sitio Project Online y otro para deshabilitar sideloading una vez que haya terminado de probar y depurar el complemento.
  
Para obtener más información acerca de cómo configurar sideloading, vea [Habilitar SideLoading en su colección de sitios que no sean de desarrollador de la aplicación](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Aplicaciones de Sideloading es una característica de desarrollo o prueba. Es **no previsto para uso de producción**. No no sideload aplicaciones con regularidad, ni mantener sideloading aplicación habilitada para ya se están usando activamente la característica. 
  
## <a name="add-content-to-the-add-in-project"></a>Agregar contenido al proyecto de complemento

Después de crear un proyecto y configurar el mecanismo de depuración, agregar contenido a la aplicación incluye las siguientes tareas:
  
- Definir el ámbito de aplicación
    
- Vinculación de la biblioteca JSOM
    
- Adición de elementos de la interfaz de usuario para el complemento
    
- Inicializar y conectar con el servicio de Project Online
    
- Recuperación de proyectos y detalles o propiedades
    
- Visualización de proyectos
    
- Mostrar las tareas de un proyecto
    
El proyecto de complemento consta de varios archivos. En este ejemplo, debe editar los archivos siguientes: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.CSS - opcional; contiene definiciones de estilo desarrolladas para el complemento
    
Si cambia el inquilino Project Online, como mover de una versión de prueba a un sitio de suscripción, puede actualizar las propiedades del proyecto, incluidas la conexión de servidor y la dirección URL del sitio, utilizando la ventana de propiedades disponibles a través de la **vista** > **Propiedades Ventana** comando. 
  
También puede agregar archivos al proyecto. Si es así, debe actualizar el archivo Elements.xml que se encuentra en el mismo grupo (contenido, imágenes, páginas o secuencias de comandos) para incluir los nuevos archivos. Para obtener más información acerca de los archivos de proyecto, vea [Explorar la estructura de manifiesto de aplicación y el paquete de un complemento de SharePoint](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Ámbito de aplicación de conjunto

El complemento necesita niveles de permiso o ámbito definidos antes de que el servicio devuelve información de resultados de la consulta. Para este complemento, utilice el siguiente ámbito para el proyecto de Visual Studio. Este cambio se realiza en el archivo AppManifest.xml en la ficha permisos:

|Ámbito|Permiso|
|:-----|:-----|
|Varios proyectos (Project Server)  <br/> |Read  <br/> |
   
Guarde el archivo después de establecer el ámbito de la aplicación. De lo contrario, no se devolverá datos desde el servicio. 
  
### <a name="link-the-jsom-library"></a>Vincular la biblioteca JSOM

Las bibliotecas de Project Online en tiempo de ejecución, PS.js y PS.debug.js, se proporcionan por Project Online y son siempre la versión más reciente. Complementos de JavaScript que use JSOM deben vincular con una de estas bibliotecas. Se agregan las definiciones de vinculación en el archivo Default.aspx. Los comandos para utilizar las PS.js o PS.debug.js forman parte del código que se encuentra en el archivo App.js.
  
Agregue el siguiente comando para la definición de PS.js o PS.debug.js en el `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` elemento siguiendo el "SharePoint: ScriptLink" para Object sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Establezca el atributo **OnDemand** para PS.js o PS.debug.js en **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Agregar elementos de la interfaz de usuario para el complemento

El complemento de ejemplo consta de unos pocos componentes. Descripciones de los elementos estáticos se encuentran en el archivo Default.aspx. Las descripciones de elementos dinámicos y código para todos los componentes se encuentran en el archivo App.js. Para comentarios acerca de los componentes, consulte los listados de código de origen. Aquí tiene una lista de los componentes de la interfaz de usuario en el complemento:
  
- Title
    
- Vocabulario introductorio
    
- Botón para quitar las tareas de la tabla
    
- Tabla que muestra el identificador del proyecto y el nombre y la información de la tarea.
    
- Botón (clonado una vez para cada proyecto) que importa los datos de la tarea en la tabla de tareas.
    
Para obtener información detallada de la interfaz de usuario, como el título y la parte de encabezado de la tabla de project, consulte el archivo de proyecto de Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar y conectarse al sistema de host

El archivo App.js contiene el código JavaScript. El complemento PS.js carga en el explorador y, a continuación, llama a la función initializePage. InitializePage recupera un contexto al extremo de Project Online y se inicia la función loadProjects.
  
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

La función loadProjects consulta el servicio para los identificadores y nombres de proyecto. 
  
La aplicación recupera el nombre del proyecto y el proyecto identificador. Otra información sobre el proyecto está disponible y se puede tener acceso mediante la modificación al método load para identificar explícitamente las propiedades para recuperar. Se proporciona un ejemplo en el código como un comentario. 
  
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

La función displayProjects crea una tabla, una fila por cada proyecto y un botón para mostrar las tareas para el proyecto específico. 
  
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
> El bucle while accesos el identificador y las propiedades del nombre. Esto es ligeramente diferente de proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Mostrar las tareas de un proyecto

Las tareas, mientras sea parte del complemento, no forman parte de la carga inicial. Si el usuario está interesado en las tareas asociadas a un proyecto, haciendo clic en el botón "Mostrar tareas" hace que las tareas que se muestra en la lista mediante el controlador de eventos btnLoadTasks. 
  
El controlador de eventos btnLoadTasks, con el identificador de proyecto adecuado, solicita las tareas para el proyecto especificado desde el servidor. Una vez recuperado, btnLoadTasks pasa la lista de tareas a displayTasks para presentar las tareas en la pantalla.
  
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

La función displayTasks muestra las tareas asociadas a un proyecto especificado inmediatamente debajo de la entrada de proyecto.
  
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
> El bucle while accesos el identificador de tarea y las propiedades del nombre. Esto es ligeramente diferente de proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
Sigue la salida de ejemplo para las tareas de un único proyecto.
  
![Captura de pantalla que muestra el resultado de una tarea de proyecto] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Captura de pantalla que muestra el resultado de una tarea de proyecto")
  
## <a name="see-also"></a>Recursos adicionales

Para obtener documentación y ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal del proyecto de desarrollo](https://developer.microsoft.com/en-us/project).
    


