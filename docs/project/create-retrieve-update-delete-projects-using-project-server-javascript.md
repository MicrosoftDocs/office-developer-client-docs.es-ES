---
title: Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtener la instancia actual de ProjectContext; recuperar e iterar en la colección de proyectos publicados en el servidor; crear, recuperar, des extraer y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322669"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="c2347-103">Crear, recuperar, actualizar y eliminar proyectos con JavaScript de Project Server</span><span class="sxs-lookup"><span data-stu-id="c2347-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="c2347-104">Los escenarios de este artículo muestran cómo obtener la instancia actual de **ProjectContext;** recuperar e iterar en la colección de proyectos publicados en el servidor; crear, recuperar, des extraer y eliminar un proyecto mediante el modelo de objetos de JavaScript de Project Server; y cambiar las propiedades de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="c2347-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c2347-105">Estos escenarios definen código personalizado en el marcado de una página de aplicación de SharePoint, pero no usan el archivo de código subyacente que Visual Studio 2012 crea para la página.</span><span class="sxs-lookup"><span data-stu-id="c2347-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="c2347-106">Requisitos previos para trabajar con proyectos de Project Server 2013 en el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="c2347-107">Para llevar a cabo los escenarios descritos en este artículo, debe instalar y configurar los productos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2347-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="c2347-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2347-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="c2347-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2347-109">Project Server 2013</span></span>
- <span data-ttu-id="c2347-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="c2347-110">Visual Studio 2012</span></span>
- <span data-ttu-id="c2347-111">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="c2347-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="c2347-112">También debe tener permisos para implementar la extensión en SharePoint Server 2013 y contribuir a proyectos.</span><span class="sxs-lookup"><span data-stu-id="c2347-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c2347-113">En estas instrucciones se supone que está desarrollando en el equipo que ejecuta Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2347-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="c2347-114">Crear la solución de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c2347-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="c2347-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="c2347-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span></span>

<span data-ttu-id="c2347-116">Los siguientes pasos crean una Visual Studio de 2012 que contiene un proyecto de SharePoint y una página de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2347-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="c2347-117">La página contiene la lógica para trabajar con proyectos.</span><span class="sxs-lookup"><span data-stu-id="c2347-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="c2347-118">Para crear el proyecto de SharePoint en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c2347-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="c2347-119">En el equipo que ejecuta Project Server 2013, ejecute Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="c2347-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="c2347-120">En la barra de menús, seleccione **Archivo**, **Nuevo**, **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c2347-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="c2347-121">En el cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c2347-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="c2347-122">En la categoría de plantillas **Office/SharePoint**, seleccione **Soluciones de SharePoint** y seleccione la plantilla **Proyecto de SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="c2347-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="c2347-123">Asigne al proyecto el nombre ProjectsJSOM y, a continuación, elija el **botón** Aceptar.</span><span class="sxs-lookup"><span data-stu-id="c2347-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="c2347-124">En el cuadro de diálogo **Asistente para la personalización de SharePoint**, elija **Implementar como solución de granja** y luego haga clic en el botón **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="c2347-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="c2347-125">Edite el valor de la propiedad **Url** del sitio para el **proyecto ProjectsJSOM** para que coincida con la dirección URL de la instancia de Project Web App (por ejemplo,  `https://ServerName/PWA` ).</span><span class="sxs-lookup"><span data-stu-id="c2347-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="c2347-126">Para crear la página de aplicación en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c2347-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="c2347-127">En el **Explorador de soluciones**, abra el menú contextual del proyecto **ProjectsJSOM** y agregue una carpeta asignada "Layouts" de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c2347-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="c2347-128">En la **carpeta Layouts,** abra el menú contextual de la carpeta **ProjectsJSOM** y, a continuación, agregue una nueva página de aplicación de SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="c2347-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="c2347-129">Abra el menú abreviado de la página **ProjectsList.aspx** y elija **Definir como elemento de inicio**.</span><span class="sxs-lookup"><span data-stu-id="c2347-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="c2347-130">En el marcado de la página **ProjectsList.aspx**, defina los controles de interfaz de usuario dentro de las etiquetas **asp:Content** de "Main", de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="c2347-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
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
   > <span data-ttu-id="c2347-131">[!NOTA] Es posible que estos controles no se usen en cada escenario.</span><span class="sxs-lookup"><span data-stu-id="c2347-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="c2347-132">Por ejemplo, el escenario "Crear proyecto" no usa los controles **textarea** y **button**.</span><span class="sxs-lookup"><span data-stu-id="c2347-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="c2347-133">Después de la etiqueta **span** de cierre, agregue una etiqueta **SharePoint:ScriptLink**, una etiqueta **SharePoint:FormDigest** y una etiqueta **script**, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="c2347-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="c2347-134">La **etiqueta SharePoint:ScriptLink** hace referencia al archivo PS.js, que define el modelo de objetos de JavaScript para Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2347-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="c2347-135">La etiqueta **SharePoint:FormDigest** genera una síntesis del mensaje para validación de seguridad cuando lo necesitan las operaciones que actualizan contenido del servidor.</span><span class="sxs-lookup"><span data-stu-id="c2347-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="c2347-136">Reemplace el comentario de marcador de posición con el código de uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="c2347-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="c2347-137">Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="c2347-138">Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="c2347-139">Eliminación de proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="c2347-p104">Para probar la página de aplicación, en la barra de menú, elija **Depurar**, **Iniciar depuración**. Si se le solicita modificar el archivo web.config, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c2347-p104">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c2347-142">Crear proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c2347-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c2347-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span></span>

<span data-ttu-id="c2347-144">El procedimiento de esta sección crea proyectos mediante el modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c2347-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="c2347-145">El procedimiento incluye los siguientes pasos generales:</span><span class="sxs-lookup"><span data-stu-id="c2347-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="c2347-146">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="c2347-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c2347-147">Crear un objeto **ProjectCreationInformation** para especificar las propiedades iniciales para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c2347-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="c2347-148">Especifique la propiedad **name** necesaria mediante la función **ProjectCreationInformation.set_name**.</span><span class="sxs-lookup"><span data-stu-id="c2347-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="c2347-149">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="c2347-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c2347-150">La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="c2347-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="c2347-151">Agregar el nuevo proyecto a la colección mediante la función **ProjectCollection.add** y pasar el objeto **ProjectCreationInformation**.</span><span class="sxs-lookup"><span data-stu-id="c2347-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="c2347-152">Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c2347-153">La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="c2347-154">Esta llamada también publica el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c2347-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="c2347-155">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="c2347-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c2347-156">Actualizar proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c2347-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c2347-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span></span>

<span data-ttu-id="c2347-158">El procedimiento de esta sección actualiza la **propiedad startDate** de un proyecto mediante el modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c2347-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="c2347-159">El procedimiento incluye los siguientes pasos generales:</span><span class="sxs-lookup"><span data-stu-id="c2347-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="c2347-160">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="c2347-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c2347-161">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="c2347-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c2347-162">La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="c2347-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="c2347-163">Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="c2347-164">Recuperar un objeto **PublishedProject** mediante la función **ProjectContext.getById**.</span><span class="sxs-lookup"><span data-stu-id="c2347-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="c2347-165">Desproteger el proyecto de destino mediante la función **Project.checkOut**.</span><span class="sxs-lookup"><span data-stu-id="c2347-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="c2347-166">La función **checkOut** devuelve la versión de borrador del proyecto publicado.</span><span class="sxs-lookup"><span data-stu-id="c2347-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="c2347-167">Cambiar la fecha de inicio del proyecto mediante la función **DraftProject.set_startDate**.</span><span class="sxs-lookup"><span data-stu-id="c2347-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="c2347-168">Publicar el proyecto mediante la función **DraftProject.publish** y la función **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c2347-169">La función **publish** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="c2347-170">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="c2347-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c2347-171">Eliminación de proyectos de Project Server 2013 mediante el modelo de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c2347-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c2347-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c2347-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span></span>

<span data-ttu-id="c2347-173">El procedimiento de esta sección elimina un proyecto mediante el modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c2347-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="c2347-174">El procedimiento incluye los siguientes pasos generales:</span><span class="sxs-lookup"><span data-stu-id="c2347-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="c2347-175">Obtener la instancia actual de **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="c2347-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c2347-176">Recuperar los proyectos publicados del servidor mediante la función **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="c2347-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c2347-177">La función **get_projects** devuelve un objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="c2347-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="c2347-178">Ejecutar la solicitud en el servidor mediante la función **ProjectContext.load** y la función **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="c2347-179">Recuperar un objeto **PublishedProject** mediante la función **ProjectCollection.getById**.</span><span class="sxs-lookup"><span data-stu-id="c2347-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="c2347-180">Eliminar el proyecto pasándolo a la función **ProjectCollection.remove**.</span><span class="sxs-lookup"><span data-stu-id="c2347-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="c2347-181">Actualizar la colección mediante la función **ProjectCollection.update** y la función **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c2347-182">La función **update** devuelve un objeto **QueueJob** que se pasa a **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="c2347-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="c2347-183">Pegar el código siguiente entre las etiquetas **script** que ha agregado en el procedimiento **Para crear la página de aplicación en Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="c2347-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
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

<span data-ttu-id="c2347-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="c2347-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="c2347-185">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2347-185">See also</span></span>

- [<span data-ttu-id="c2347-186">Tareas de programación de Project</span><span class="sxs-lookup"><span data-stu-id="c2347-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="c2347-187">Modelo de objetos de cliente (CSOM) para Project 2013</span><span class="sxs-lookup"><span data-stu-id="c2347-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

