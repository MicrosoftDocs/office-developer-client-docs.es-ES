---
title: Desarrollar un complemento de Project online con el modelo de objetos de JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: En este artículo se describe el desarrollo de complementos de Microsoft Project online para mejorar su experiencia con Project online. El proyecto de desarrollo se implementa como un tutorial. El complemento usado en este artículo Lee y muestra los nombres e identificadores de proyecto de los proyectos publicados de la cuenta de Project online y le permite obtener detalles para recuperar tareas asociadas a proyectos individuales.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322697"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desarrollar un complemento de Project online con el modelo de objetos de JavaScript (JSOM)

En este artículo se describe el desarrollo de complementos de Microsoft Project online para mejorar su experiencia con el proyecto en línea. El proyecto de desarrollo se implementa como un tutorial. El complemento usado en este artículo Lee y muestra los nombres e identificadores de proyecto de los proyectos publicados de la cuenta de Project online y le permite obtener detalles para recuperar tareas asociadas a proyectos individuales.
  
En tiempo de ejecución, la lista de complementos tiene un aspecto similar al de la siguiente ilustración:
  
![Captura de pantalla que muestra una lista de proyectos y tareas de JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Captura de pantalla que muestra una lista de proyectos y tareas de JSOM")
  
El enfoque del ejemplo es la interacción con Project online, que realiza consultas y establece el contexto para cada solicitud del servicio. Los elementos de la interfaz de usuario (UI) reciben una atención mínima. En su lugar, los listados de origen proporcionan comentarios sobre la interfaz de usuario.
  
> [!NOTE]
> Los archivos de origen para el complemento de ejemplo, un proyecto de Visual Studio, están disponibles en https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....:. Mantenga a mano los archivos de origen como referencia mientras lee el artículo, ya que cada uno complementa al otro. Los archivos de la compilación del proyecto de Visual Studio y son ejecutables con cambios mínimos; sustituyendo la dirección URL del inquilino de Project online a la carpeta PWA. 
  
## <a name="background"></a>Fondo

Project online es un servicio de Office 365 que ofrece a las empresas una solución de administración de carteras de proyectos (PPM) y de la oficina de administración de proyectos (PMO) para coordinar y administrar carteras, programas y proyectos. Project online es una oferta diferente de las ediciones de escritorio del proyecto; sin embargo, Project online sigue conteniendo la funcionalidad para mantener y realizar un seguimiento de los detalles del proyecto durante la vida de un proyecto. Project online se basa en SharePoint Online.
  
Un complemento hospedado de Project online consta de JavaScript y archivos de recursos que interactúan con la API del modelo de objetos del lado cliente. Cuando el usuario visita el complemento, el JavaScript y los recursos se descargan y se ejecutan en el explorador. El complemento realiza llamadas asincrónicas a Project online para interactuar con el servicio, ya sea creando, recuperando, actualizando o eliminando datos. 
  
Project online realiza una acción más para proteger la información que pertenece a otros inquilinos del complemento; es decir, Project online crea un sitio aislado para interactuar con las solicitudes del complemento. No se ejecuta ningún código personalizado en el host de Project online. 
  
La configuración de desarrollo para complementos de Project online usa el tipo de proyecto complemento de SharePoint de Visual Studio. El complemento se escribe en JavaScript y usa el modelo de objetos de JavaScript (JSOM) del proyecto para interactuar con el servicio de Project online. JSOM hereda gran parte de su funcionalidad del JSOM de SharePoint.
  
> [!NOTE]
> Los complementos pueden publicarse y venderse en la tienda Office o implementarse en un catálogo de aplicaciones privado de SharePoint. Para obtener más información, vea [deploy and Publish Your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> El complemento usado en este artículo es un ejemplo para desarrolladores; no está pensada para su uso en un entorno de producción. El objetivo principal es mostrar un ejemplo de desarrollo de aplicaciones para Project online. 
  
## <a name="prerequisites"></a>Requisitos previos

Agregue los siguientes elementos a un entorno de Windows admitido:
  
- **.NET Framework 4,0 o posterior**: las versiones completas del marco de trabajo de la versión 4,0 son compatibles. El sitio de descarga es https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 o posterior**:  
    
   - La edición Professional de Visual Studio 2015 está preparada para salirse y está disponible en https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - La edición de la comunidad de Visual Studio 2015 está https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspxdisponible en. Esta edición requiere la instalación manual de Microsoft Office Developer Tools para Visual Studio.
    
   Microsoft Office Developer Tools para Visual Studio está disponible en https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Una cuenta de Project online**: proporciona acceso al servicio de hospedaje. Para obtener más información acerca de cómo obtener una cuenta de Project Online, vea https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Asegúrese de que el usuario del complemento tenga la autorización suficiente para obtener acceso a algunos proyectos del espacio empresarial de Project online. 
    
- **Proyectos en el sitio de hospedaje** que se rellenan con información.
    
> [!NOTE]
> .NET Framework estándar es el marco correcto que se debe usar. No use el perfil de cliente de .NET Framework 4. 
  
### <a name="set-up-the-visual-studio-project"></a>Configuración del proyecto de Visual Studio

El programa de instalación de la aplicación consiste en crear un nuevo proyecto, vincular las bibliotecas apropiadas y declarar los espacios de nombres necesarios. Visual Studio presenta varios tipos de proyectos de desarrollo. La sección es breve y muy básica. El valor tiene la información que se combina en un único punto.
  
#### <a name="select-a-visual-studio-project"></a>Seleccionar un proyecto de Visual Studio

Para crear un proyecto del tipo adecuado para el complemento, debe realizar los siguientes pasos. Las palabras clave que se encuentran en la pantalla tienen un atributo en **negrita** : 
  
1. En el menú Archivo, elija **archivo** > **nuevo** > **proyecto**. 
    
2. En las plantillas instaladas, en el panel izquierdo, seleccione**Complementos Web de** **C#** > **Office/SharePoint** > . 
    
3. En la parte superior del panel central, seleccione **.NET Framework 4** o posterior; la versión actual es 4,6. 
    
4. En los tipos de aplicación del panel central, elija **complemento de SharePoint**. 
    
5. En la sección inferior, especifique un nombre y una ubicación para el proyecto, así como un nombre de la solución. 
    
6. También en la sección inferior, active la casilla **Crear directorio para la solución**. 
    
7. Haga clic en **Aceptar** para crear un proyecto inicial. 
    
El Asistente de Visual Studio hace algunas preguntas de seguimiento sobre el sitio de configuración de Project online (denominado configuración de SharePoint en los cuadros de diálogo) en un par de cuadros de diálogo que siguen. Estas son las preguntas:
  
1. ¿Qué sitio de SharePoint desea usar para depurar el complemento? Especifique la dirección URL del sitio de PWA, como https://contoso.sharepoint.com/sites/pwa.
    
2. ¿Cómo desea hospedar el complemento de SharePoint? Elija [X] **hospedado en SharePoint**.
    
   Para obtener más información sobre los complementos de SharePoint, incluidas las opciones de hospedaje, consulte [Complementos de SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Haga clic en **Siguiente**. 
    
El segundo cuadro de diálogo adicional le pide que especifique la versión de SharePoint Online para el complemento: 
  
1. ¿Cuál es la versión más antigua de SharePoint a la que desea dirigir el complemento? Elija [X] S **harePoint-online**. 
    
2. Haga clic en **Finalizar**. 
    
Visual Studio crea el proyecto y obtiene acceso al sitio de Project online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar la transferencia local en el sitio de Project online

La transferencia local es un mecanismo para probar y depurar complementos de Project online. Necesita dos scripts para la transferencia local: uno para habilitar la transferencia local en el sitio de Project online y otro para deshabilitar la transferencia local cuando haya terminado de probar y depurar el complemento.
  
Para obtener más información sobre cómo configurar la instalación de prueba, vea [Habilitar la transferencia local de aplicaciones en la colección de sitios no para desarrolladores](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Las aplicaciones de transferencia local es una característica de desarrollo y prueba. No está **pensada para su uso en producción**. No transfiera localmente aplicaciones de forma regular o mantenga la instalación de prueba de aplicaciones habilitada durante más tiempo del que usa la característica de forma activa. 
  
## <a name="add-content-to-the-add-in-project"></a>Agregar contenido al proyecto del complemento

Después de crear un proyecto y de configurar el mecanismo de depuración, agregar contenido a la aplicación incluye las siguientes tareas:
  
- Configuración del ámbito de la aplicación
    
- Vinculación de la biblioteca JSOM
    
- Adición de elementos de la interfaz de usuario al complemento
    
- Inicialización y conexión al servicio de Project online
    
- Recuperación de proyectos y detalles/propiedades
    
- Mostrar proyectos
    
- Mostrar tareas para un proyecto
    
El proyecto de complemento consta de muchos archivos. En este ejemplo, necesitará editar los siguientes archivos: 
  
- AppManifest. XML
    
- Default. aspx
    
- App. js
    
- App. CSS: opcional; contiene las definiciones de estilo desarrolladas para el complemento.
    
Si el espacio empresarial de Project online cambia, como cambiar de una prueba a un sitio de suscripción, puede actualizar las propiedades del proyecto, incluidas la conexión del servidor y la dirección URL del sitio, mediante la ventana Propiedades disponible a través de las propiedades de la **vista** > .** Comando ventana** . 
  
También puede Agregar archivos al proyecto. Si es así, deberá actualizar el archivo Elements. XML ubicado en el mismo grupo (contenido, imágenes, páginas o scripts) para incluir los nuevos archivos. Para obtener más información sobre los archivos de proyecto, vea [explorar la estructura del manifiesto de la aplicación y el paquete de un complemento de SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Establecer el ámbito de la aplicación

El complemento necesita niveles de permisos o de ámbito definidos antes de que el servicio devuelva información en los resultados de la consulta. Para este complemento, use el siguiente ámbito para el proyecto de Visual Studio. Este cambio se realiza en el archivo AppManifest. XML en la pestaña permisos:

|Ámbito|Permiso|
|:-----|:-----|
|Varios proyectos (Project Server)  <br/> |Lectura  <br/> |
   
Guarde el archivo después de establecer el ámbito de la aplicación. De lo contrario, no se devolverá ningún dato del servicio. 
  
### <a name="link-the-jsom-library"></a>Vincular la biblioteca JSOM

Project online proporciona las bibliotecas de Project online de tiempo de ejecución, PS. js y PS. Debug. js, y siempre son las versiones más recientes. Los complementos de JavaScript que usan JSOM deben vincularse con una de estas bibliotecas. Las definiciones de vínculos se agregan en el archivo default. aspx. Los comandos para usar PS. js y/o PS. Debug. js forman parte del código ubicado en el archivo app. js.
  
Agregue el siguiente comando para la definición de PS. js o PS. Debug. js `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` en el elemento que sigue a "SharePoint: ScriptLink" para SP. js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> El atributo **OnDemand** de PS. js o PS. Debug. js establecido en **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Agregar elementos de la interfaz de usuario al complemento

El complemento de ejemplo consta de algunos componentes. Las descripciones de elementos estáticos se encuentran en el archivo default. aspx. Las descripciones de elementos dinámicos y el código de todos los componentes se encuentran en el archivo app. js. Para obtener comentarios sobre los componentes, consulte los listados de código fuente. A continuación, se muestra una lista de los componentes de la interfaz de usuario del complemento:
  
- Title
    
- Introducción texto
    
- Botón para quitar tareas de la tabla
    
- Tabla que enumera el identificador y el nombre del proyecto, así como la información de la tarea.
    
- Botón tareas (clonado una vez para cada proyecto) que importa datos de tareas a la tabla.
    
Para obtener información detallada sobre la interfaz de usuario, como el título y la parte de encabezado de la tabla de Project, vea el archivo de proyecto default. aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar y conectarse al sistema host

El archivo app. js contiene el código JavaScript. El complemento carga PS. js en el explorador y, a continuación, llama a la función initializePage. InitializePage recupera un contexto en el punto de conexión de Project online e inicia la función loadProjects.
  
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

La función loadProjects consulta el servicio en busca de los nombres e identificadores de proyecto. 
  
La aplicación recupera el nombre del proyecto y el identificador del proyecto. Otra información sobre el proyecto está disponible y se puede tener acceso a ella modificando el método Load para identificar explícitamente las propiedades que se van a recuperar. En el código se proporciona un ejemplo como comentario. 
  
Si la consulta se realiza correctamente, el complemento sigue llamando a displayProjects. 
  
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
> El bucle while tiene acceso a las propiedades ID y Name. Esto es ligeramente diferente al proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Mostrar las tareas de un proyecto

Las tareas, mientras que parte del complemento, no forman parte de la carga inicial. Si el usuario está interesado en las tareas asociadas a un proyecto, al hacer clic en el botón "Mostrar tareas" las tareas se muestran en la lista mediante el controlador de eventos btnLoadTasks. 
  
El controlador de eventos btnLoadTasks, con el identificador de proyecto adecuado, solicita las tareas para el proyecto especificado desde el servidor. Una vez recuperada, btnLoadTasks pasa la lista de tareas a displayTasks para mostrar las tareas en la pantalla.
  
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
> El bucle while tiene acceso a las propiedades ID de tarea y nombre. Esto es ligeramente diferente al proyecto de código fuente que llama a una función que, a su vez, tiene acceso a las mismas propiedades. 
  
A continuación se muestra un ejemplo de resultado para las tareas de un único proyecto.
  
![Captura de pantalla que muestra el resultado de una tarea de proyecto] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Captura de pantalla que muestra el resultado de una tarea de proyecto")
  
## <a name="see-also"></a>Vea también

Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).
    


