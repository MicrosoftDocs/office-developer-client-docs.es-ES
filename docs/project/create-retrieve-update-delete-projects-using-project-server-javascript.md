---
title: Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtener la instancia actual de ProjectContext; recuperar y recorrer en iteración la colección de proyectos publicados en el servidor; crear, recuperar, desproteger y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382914"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server

En los escenarios de este artículo se muestran cómo obtener la instancia actual de **ProjectContext** ; recuperar y recorrer en iteración la colección de proyectos publicados en el servidor; crear, recuperar, desproteger y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto. 
  
> [!NOTE]
> Estos escenarios definen código personalizado en el marcado de una página de aplicación de SharePoint pero que no usan el archivo de código subyacente que crea Visual Studio 2012 para la página. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Requisitos previos para trabajar con proyectos de Project Server 2013 en el modelo de objetos de JavaScript

Para llevar a cabo los escenarios descritos en este artículo, debe instalar y configurar los productos siguientes:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools para Visual Studio 2012
    
También debe tener permisos para implementar la extensión a SharePoint Server 2013 y para contribuir a proyectos.
  
> [!NOTE]
> Estas instrucciones suponen que está desarrollando en el equipo que ejecuta Project Server 2013. 
  
## <a name="create-the-visual-studio-solution"></a>Crear una solución de Visual Studio
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

Los pasos siguientes crean una solución de Visual Studio 2012 que contiene un proyecto de SharePoint y una página de aplicación. La página contiene la lógica para trabajar con proyectos.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Para crear el proyecto de SharePoint en Visual Studio

1. En el equipo que ejecuta Project Server 2013, ejecute Visual Studio 2012 como administrador.
    
2. En la barra de menús, seleccione **Archivo**, **Nuevo**, **Proyecto**.
    
3. En el cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo. 
    
4. En la categoría de plantillas **Office/SharePoint**, seleccione **Soluciones de SharePoint** y seleccione la plantilla **Proyecto de SharePoint 2013**. 
    
5. Nombre del proyecto ProjectsJSOM y, a continuación, elija el botón **Aceptar** . 
    
6. En el cuadro de diálogo **Asistente para la personalización de SharePoint**, elija **Implementar como solución de granja** y luego haga clic en el botón **Finalizar**. 
    
7. Edite el valor de la propiedad **Dirección URL del sitio** para el proyecto **ProjectsJSOM** para que coincida con la dirección URL de la instancia de Project Web App (por ejemplo, `https://ServerName/PWA`).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Para crear la página de aplicación en Visual Studio

1. En el **Explorador de soluciones**, abra el menú contextual del proyecto **ProjectsJSOM** y agregue una carpeta asignada "Layouts" de SharePoint. 
    
2. En la carpeta **Layouts** , abra el menú contextual para la carpeta **ProjectsJSOM** y, a continuación, agregue una nueva página de aplicación de SharePoint denominada ProjectsList.aspx.
    
3. Abra el menú contextual de la página **ProjectsList.aspx** y elija **Establecer como elemento de inicio**.
    
4. En el marcado de la página **ProjectsList.aspx**, defina los controles de interfaz de usuario dentro de las etiquetas **asp:Content** de "Main", de la siguiente manera. 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > Estos controles no se pueden usar en todos los escenarios. Por ejemplo, el escenario "Crear proyecto" no usa los controles **textarea** y **button**. 
  
5. Después de la etiqueta **span** de cierre, agregue una etiqueta **SharePoint:ScriptLink**, una etiqueta **SharePoint:FormDigest** y una etiqueta **script**, de la siguiente manera. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   La etiqueta **SharePoint: ScriptLink** hace referencia al archivo PS.js, que define el modelo de objetos de JavaScript para Project Server 2013. La etiqueta **SharePoint: FormDigest** genera una síntesis del mensaje para la validación de seguridad cuando sea necesario por las operaciones que se actualicen el contenido del servidor. 
    
6. Reemplace el comentario de marcador de posición con el código de uno de los siguientes procedimientos:
    
   - [Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Eliminar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Para probar la página de aplicación, en la barra de menús, seleccione **Depurar**, **Iniciar depuración**. Si se le pregunta si desea modificar el archivo web.config, seleccione **Aceptar**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

El procedimiento descrito en esta sección crea proyectos mediante el modelo de objetos de JavaScript. El procedimiento incluye los siguientes pasos de alto nivel:
  
1. Obtener la instancia actual de **ProjectContext**. 
    
2. Crear un objeto **ProjectCreationInformation** para especificar las propiedades iniciales para el proyecto. Especifique la propiedad **name** necesaria mediante la función **ProjectCreationInformation.set_name**. 
    
3. Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**. 
    
4. Agregar el nuevo proyecto a la colección mediante la función **ProjectCollection.add** y pasar el objeto **ProjectCreationInformation**. 
    
5. Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**. La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**. Esta llamada también publica el proyecto.
    
Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**. 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

El procedimiento descrito en esta sección, actualiza la propiedad **startDate** de un proyecto mediante el uso del modelo de objetos de JavaScript. El procedimiento incluye los siguientes pasos de alto nivel: 
  
1. Obtener la instancia actual de **ProjectContext**. 
    
2. Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**. 
    
3. Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**. 
    
4. Recuperar un objeto **PublishedProject** mediante la función **ProjectContext.getById**. 
    
5. Desproteger el proyecto de destino mediante la función **Project.checkOut**. La función **checkOut** devuelve la versión de borrador del proyecto publicado. 
    
6. Cambiar la fecha de inicio del proyecto mediante la función **DraftProject.set_startDate**. 
    
7. Publicar el proyecto mediante la función **DraftProject.publish** y la función **ProjectContext.waitForQueueAsync**. La función **publish** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.
    
Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**. 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Eliminar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

El procedimiento descrito en esta sección, elimina un proyecto mediante el uso del modelo de objetos de JavaScript. El procedimiento incluye los siguientes pasos de alto nivel:
  
1. Obtener la instancia actual de **ProjectContext**. 
    
2. Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**. 
    
3. Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**. 
    
4. Recuperar un objeto **PublishedProject** mediante la función **ProjectCollection.getById**. 
    
5. Eliminar el proyecto pasándolo a la función **ProjectCollection.remove**. 
    
6. Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**. La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.
    
Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**. 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>Vea también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Modelo de objetos de cliente (COM) de Project 2013](client-side-object-model-csom-for-project-2013.md)
    

