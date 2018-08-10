---
title: Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtener la instancia actual de ProjectContext; recuperar y recorrer en iteración la colección de proyectos publicados en el servidor; crear, recuperar, desproteger y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto.
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821299"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="ecac8-103">Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server</span><span class="sxs-lookup"><span data-stu-id="ecac8-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="ecac8-104">En los escenarios de este artículo se muestran cómo obtener la instancia actual de **ProjectContext** ; recuperar y recorrer en iteración la colección de proyectos publicados en el servidor; crear, recuperar, desproteger y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="ecac8-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ecac8-105">Estos escenarios definen código personalizado en el marcado de una página de aplicación de SharePoint pero que no usan el archivo de código subyacente que crea Visual Studio 2012 para la página.</span><span class="sxs-lookup"><span data-stu-id="ecac8-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="ecac8-106">Requisitos previos para trabajar con proyectos de Project Server 2013 en el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="ecac8-107">Para llevar a cabo los escenarios descritos en este artículo, debe instalar y configurar los productos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ecac8-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="ecac8-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecac8-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="ecac8-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecac8-109">Project Server 2013</span></span>
- <span data-ttu-id="ecac8-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="ecac8-110">Visual Studio 2012</span></span>
- <span data-ttu-id="ecac8-111">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="ecac8-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="ecac8-112">También debe tener permisos para implementar la extensión a SharePoint Server 2013 y para contribuir a proyectos.</span><span class="sxs-lookup"><span data-stu-id="ecac8-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ecac8-113">Estas instrucciones suponen que está desarrollando en el equipo que ejecuta Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ecac8-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="ecac8-114">Crear una solución de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ecac8-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="ecac8-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="ecac8-115"></span></span>

<span data-ttu-id="ecac8-116">Los pasos siguientes crean una solución de Visual Studio 2012 que contiene un proyecto de SharePoint y una página de aplicación.</span><span class="sxs-lookup"><span data-stu-id="ecac8-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="ecac8-117">La página contiene la lógica para trabajar con proyectos.</span><span class="sxs-lookup"><span data-stu-id="ecac8-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="ecac8-118">Para crear el proyecto de SharePoint en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ecac8-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="ecac8-119">En el equipo que ejecuta Project Server 2013, ejecute Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="ecac8-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="ecac8-120">En la barra de menús, seleccione **Archivo**, **Nuevo**, **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="ecac8-121">En el cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecac8-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="ecac8-122">En la categoría de plantillas **Office/SharePoint**, seleccione **Soluciones de SharePoint** y seleccione la plantilla **Proyecto de SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="ecac8-123">Nombre del proyecto ProjectsJSOM y, a continuación, elija el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="ecac8-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="ecac8-124">En el cuadro de diálogo **Asistente para la personalización de SharePoint**, elija **Implementar como solución de granja** y luego haga clic en el botón **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="ecac8-125">Edite el valor de la propiedad **Dirección URL del sitio** para el proyecto **ProjectsJSOM** para que coincida con la dirección URL de la instancia de Project Web App (por ejemplo, `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="ecac8-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="ecac8-126">Para crear la página de aplicación en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ecac8-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="ecac8-127">En el **Explorador de soluciones**, abra el menú contextual del proyecto **ProjectsJSOM** y agregue una carpeta asignada "Layouts" de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ecac8-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="ecac8-128">En la carpeta **Layouts** , abra el menú contextual para la carpeta **ProjectsJSOM** y, a continuación, agregue una nueva página de aplicación de SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="ecac8-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="ecac8-129">Abra el menú contextual de la página **ProjectsList.aspx** y elija **Establecer como elemento de inicio**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="ecac8-130">En el marcado de la página **ProjectsList.aspx**, defina los controles de interfaz de usuario dentro de las etiquetas **asp:Content** de "Main", de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="ecac8-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
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
   > <span data-ttu-id="ecac8-p102">Estos controles no se pueden usar en todos los escenarios. Por ejemplo, el escenario "Crear proyecto" no usa los controles **textarea** y **button**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p102">These controls may not be used in every scenario. For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="ecac8-133">Después de la etiqueta **span** de cierre, agregue una etiqueta **SharePoint:ScriptLink**, una etiqueta **SharePoint:FormDigest** y una etiqueta **script**, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="ecac8-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="ecac8-134">La etiqueta **SharePoint: ScriptLink** hace referencia al archivo PS.js, que define el modelo de objetos de JavaScript para Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ecac8-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="ecac8-135">La etiqueta **SharePoint: FormDigest** genera una síntesis del mensaje para la validación de seguridad cuando sea necesario por las operaciones que se actualicen el contenido del servidor.</span><span class="sxs-lookup"><span data-stu-id="ecac8-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="ecac8-136">Reemplace el comentario de marcador de posición con el código de uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="ecac8-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="ecac8-137">Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="ecac8-138">Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="ecac8-139">Eliminar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="ecac8-p104">Para probar la página de aplicación, en la barra de menús, seleccione **Depurar**, **Iniciar depuración**. Si se le pregunta si desea modificar el archivo web.config, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p104">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="ecac8-142">Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="ecac8-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="ecac8-143"></span></span>

<span data-ttu-id="ecac8-144">El procedimiento descrito en esta sección crea proyectos mediante el modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ecac8-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="ecac8-145">El procedimiento incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="ecac8-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="ecac8-146">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="ecac8-p106">Crear un objeto **ProjectCreationInformation** para especificar las propiedades iniciales para el proyecto. Especifique la propiedad **name** necesaria mediante la función **ProjectCreationInformation.set_name**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p106">Create a **ProjectCreationInformation** object to specify initial properties for your project. Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="ecac8-p107">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p107">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function. The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="ecac8-151">Agregar el nuevo proyecto a la colección mediante la función **ProjectCollection.add** y pasar el objeto **ProjectCreationInformation**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="ecac8-p108">Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**. La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**. Esta llamada también publica el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p108">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function. The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**. This call also publishes the project.</span></span>
    
<span data-ttu-id="ecac8-155">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="ecac8-156">Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="ecac8-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="ecac8-157"></span></span>

<span data-ttu-id="ecac8-158">El procedimiento descrito en esta sección, actualiza la propiedad **startDate** de un proyecto mediante el uso del modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ecac8-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="ecac8-159">El procedimiento incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="ecac8-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="ecac8-160">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="ecac8-p110">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p110">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function. The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="ecac8-163">Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="ecac8-164">Recuperar un objeto **PublishedProject** mediante la función **ProjectContext.getById**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="ecac8-p111">Desproteger el proyecto de destino mediante la función **Project.checkOut**. La función **checkOut** devuelve la versión de borrador del proyecto publicado.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p111">Check out the target project by using the **Project.checkOut** function. The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="ecac8-167">Cambiar la fecha de inicio del proyecto mediante la función **DraftProject.set_startDate**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="ecac8-p112">Publicar el proyecto mediante la función **DraftProject.publish** y la función **ProjectContext.waitForQueueAsync**. La función **publish** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p112">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function. The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="ecac8-170">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="ecac8-171">Eliminar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="ecac8-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="ecac8-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="ecac8-172"></span></span>

<span data-ttu-id="ecac8-173">El procedimiento descrito en esta sección, elimina un proyecto mediante el uso del modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ecac8-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="ecac8-174">El procedimiento incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="ecac8-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="ecac8-175">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="ecac8-p114">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**. La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p114">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function. The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="ecac8-178">Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="ecac8-179">Recuperar un objeto **PublishedProject** mediante la función **ProjectCollection.getById**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="ecac8-180">Eliminar el proyecto pasándolo a la función **ProjectCollection.remove**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="ecac8-p115">Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**. La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-p115">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function. The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="ecac8-183">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ecac8-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

<span data-ttu-id="ecac8-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="ecac8-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="ecac8-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecac8-185">See also</span></span>

- [<span data-ttu-id="ecac8-186">Tareas de programación de Project</span><span class="sxs-lookup"><span data-stu-id="ecac8-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="ecac8-187">Modelo de objetos de cliente (COM) de Project 2013</span><span class="sxs-lookup"><span data-stu-id="ecac8-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    
