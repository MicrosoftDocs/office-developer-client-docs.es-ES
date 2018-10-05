---
title: Comenzar con el modelo de objetos de JavaScript de Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: En Project Server 2013, se puede usar el modelo de objetos de JavaScript en Project Online, desarrollo de dispositivos móvil y locales. En este tema se ofrece una breve descripción del modelo de objetos de JavaScript y, a continuación, se describe cómo crear una página de aplicación que recupera e itera a través de proyectos mediante el uso del modelo de objetos de JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388213"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="0671a-104">Comenzar con el modelo de objetos de JavaScript de Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="0671a-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="0671a-105">En Project Server 2013, se puede usar el modelo de objetos de JavaScript en Project Online, desarrollo de dispositivos móvil y locales.</span><span class="sxs-lookup"><span data-stu-id="0671a-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="0671a-106">En este tema se ofrece una breve descripción del modelo de objetos de JavaScript y, a continuación, se describe cómo crear una página de aplicación que recupera e itera a través de proyectos mediante el uso del modelo de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0671a-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="0671a-107">Uso del modelo de objetos de JavaScript de Project Server</span><span class="sxs-lookup"><span data-stu-id="0671a-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="0671a-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-108"></span></span>

<span data-ttu-id="0671a-109">Con el modelo de objetos de JavaScript constituye una excelente manera para crear una aplicación que se ejecuta el cliente (en lugar de código de cliente administrado que se debe ejecutar de forma remota).</span><span class="sxs-lookup"><span data-stu-id="0671a-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="0671a-110">Aplicaciones pueden usar el modelo de objetos de JavaScript para recuperar o cambiar los objetos mediante el envío de llamadas asincrónicas al servidor.</span><span class="sxs-lookup"><span data-stu-id="0671a-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="0671a-111">Aplicaciones que usan el modelo de objetos de JavaScript normalmente se implementan como SharePoint Add-ins, las páginas de aplicación y elementos Web personalizados.</span><span class="sxs-lookup"><span data-stu-id="0671a-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="0671a-112">Para obtener más información, vea "Tipos de componentes de SharePoint que pueden encontrarse en una aplicación de SharePoint" en [webs de Host, agregar en sitios Web y los componentes de SharePoint en SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0671a-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="0671a-113">El modelo de objetos de JavaScript implementa la funcionalidad principal de Project Server 2013, pero el modelo de objetos de JavaScript y el modelo de objetos de servidor no tienen paridad uno a uno.</span><span class="sxs-lookup"><span data-stu-id="0671a-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="0671a-114">El punto de entrada para el modelo de objetos de JavaScript es el objeto de **ProjectContext** , que representa el contexto de cliente para Project Server 2013 y proporciona acceso al contenido del servidor y la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="0671a-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="0671a-115">El modelo de objetos de JavaScript para Project Server 2013 se define en el archivo PS.js, que se encuentra en la ruta de acceso predeterminada `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` en el servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0671a-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="0671a-116">Project Server 2013 también instala el PS. Archivo de Debug.js en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="0671a-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="0671a-117">PS. Debug.js es una versión unminified de PS.js que proporciona la información de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="0671a-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="0671a-118">El modelo de objetos de JavaScript permite la autenticación de formularios, y todas las solicitudes se autentican como el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="0671a-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="0671a-119">Para obtener más información acerca de la seguridad y otras consideraciones de diseño de aplicaciones personalizadas y soluciones, vea [autenticación, autorización y seguridad en SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [aspectos importantes de la arquitectura de SharePoint Add-in y desarrollo horizontal](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)y [los complementos de SharePoint en comparación con las soluciones de SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0671a-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0671a-120">Para obtener acceso a datos desde un sitio de SharePoint forma remota, SharePoint 2013 proporciona una biblioteca entre dominios que le permite realizar llamadas entre dominios del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="0671a-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="0671a-121">Para obtener más información, vea [datos de Access SharePoint 2013 de complementos mediante la biblioteca entre dominios](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0671a-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="0671a-122">Muchos de los conceptos y procesos para usar el modelo de objetos de JavaScript para Project Server 2013 son similares a las de modelos de objetos de cliente relacionados.</span><span class="sxs-lookup"><span data-stu-id="0671a-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="0671a-123">Para obtener más información sobre el modelo de objetos de cliente administrado de Project Server 2013, vea **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="0671a-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="0671a-124">Para obtener más información sobre el modelo de objetos de SharePoint 2013JavaScript y el modelo de objetos de cliente administrado, vea [completar operaciones básicas con código de la biblioteca de JavaScript en SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) y [operaciones básicas completa con el cliente de SharePoint 2013 código de la biblioteca](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0671a-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="0671a-125">Tutorial: creación de una página de aplicación que recupera e itera a través de proyectos</span><span class="sxs-lookup"><span data-stu-id="0671a-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="0671a-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-126"></span></span>

<span data-ttu-id="0671a-127">Aprenda a crear una página de aplicación que muestra el Id., el nombre y la fecha de creación de cada proyecto publicado en un sitio.</span><span class="sxs-lookup"><span data-stu-id="0671a-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="0671a-128">Requisitos previos para crear una página de aplicación que recupera e itera a través de proyectos</span><span class="sxs-lookup"><span data-stu-id="0671a-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="0671a-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-129"></span></span>

<span data-ttu-id="0671a-130">Para desarrollar la página de aplicación que se describe en este tema, debe instalar y configurar los siguientes productos:</span><span class="sxs-lookup"><span data-stu-id="0671a-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="0671a-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="0671a-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="0671a-132">Project Server 2013 con al menos un proyecto publicado</span><span class="sxs-lookup"><span data-stu-id="0671a-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="0671a-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="0671a-133">Visual Studio 2012</span></span>
- <span data-ttu-id="0671a-134">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="0671a-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="0671a-135">También debe tener permisos para implementar la extensión en SharePoint Server 2013 y recuperar proyectos.</span><span class="sxs-lookup"><span data-stu-id="0671a-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0671a-136">Estas instrucciones suponen que está desarrollando en el equipo que ejecuta Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0671a-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="0671a-137">Creación de la página de aplicación en Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="0671a-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="0671a-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-138"></span></span>

<span data-ttu-id="0671a-p108">Los siguientes pasos crean un proyecto de SharePoint y una página de aplicación que contiene una tabla y una etiqueta. La tabla muestra información sobre los proyectos y la etiqueta muestra mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="0671a-p108">The following steps create a SharePoint project and an application page that contains a table and label. The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="0671a-141">En el equipo que ejecuta Project Server 2013, ejecute Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="0671a-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="0671a-142">Crear un proyecto vacío de SharePoint 2013, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="0671a-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="0671a-143">En el cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0671a-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="0671a-144">En la lista de categorías de plantilla, elija la categoría **SharePoint de Office** y, a continuación, elija la plantilla **SharePoint 2013 Project**.</span><span class="sxs-lookup"><span data-stu-id="0671a-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="0671a-145">Nombre del proyecto GetProjectsJSOM y, a continuación, elija el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="0671a-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="0671a-146">En el cuadro de diálogo **Asistente para la personalización de SharePoint**, elija **Implementar como solución de granja** y, a continuación, elija el botón **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="0671a-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="0671a-147">En el Explorador de soluciones, edite el valor de la propiedad **Dirección URL del sitio** para el proyecto **ProjectsJSOM** para que coincida con la dirección URL de la instancia de Project Web App (por ejemplo, `https://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="0671a-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="0671a-148">Abra el menú abreviado del proyecto **GetProjectsJSOM** y, a continuación, agregue una carpeta asignada "Diseños" de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0671a-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="0671a-149">En la carpeta **Layouts** , abra el menú contextual para la carpeta **GetProjectsJSOM** y, a continuación, agregue una nueva página de aplicación de SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="0671a-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="0671a-150">En este ejemplo no utiliza el archivo de código subyacente que crea Visual Studio 2012 para la página de aplicación.</span><span class="sxs-lookup"><span data-stu-id="0671a-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="0671a-151">Abra el menú contextual de la página **ProjectsList.aspx** y elija **Establecer como elemento de inicio**.</span><span class="sxs-lookup"><span data-stu-id="0671a-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="0671a-152">En el fragmento de la página **ProjectsList.aspx**, defina una tabla y un marcador de posición de mensaje dentro de las etiquetas de **asp:Content** "principales", de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="0671a-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="0671a-153">Recuperar la colección de proyectos</span><span class="sxs-lookup"><span data-stu-id="0671a-153">Retrieving the projects collection</span></span>
<span data-ttu-id="0671a-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-154"></span></span>

<span data-ttu-id="0671a-155">Lo siguientes pasos recuperan e inicializan la colección de proyectos.</span><span class="sxs-lookup"><span data-stu-id="0671a-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="0671a-156">Después de la etiqueta de cierre **div**, agregue una etiqueta **SharePoint:ScriptLink** que haga referencia al archivo PS.js, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0671a-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="0671a-157">Debajo de la etiqueta **SharePoint:ScriptLink**, agregue las etiquetas de **script**, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0671a-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="0671a-158">Declare una variable global para almacenar la colección de proyectos, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0671a-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="0671a-159">Llame al método de **SP.SOD.executeOrDelayUntilScriptLoaded** para asegurarse de que el archivo PS.js se carga antes de que se ejecute su código personalizado.</span><span class="sxs-lookup"><span data-stu-id="0671a-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="0671a-160">Agregue una función que conecte con el contexto actual y recupere la colección de proyectos, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0671a-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="0671a-p109">Algunos objetos de cliente que recupera a través del contexto no contienen ningún dato hasta que se hayan inicializado; es decir, no puede obtener acceso a los valores de propiedad del objeto hasta que el objeto se inicialice. Asimismo, para las propiedades de tipo **ValueObject**, debe solicitar explícitamente la propiedad antes de poder obtener acceso a su valor. (Si intenta obtener acceso a una propiedad antes de que se inicialice, recibirá una excepción de **PropertyOrFieldNotInitializedException**).</span><span class="sxs-lookup"><span data-stu-id="0671a-p109">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized. Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value. (If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="0671a-164">Para inicializar un objeto, llame al método de **load** (o el método de **loadQuery**) y, a continuación, al método de **executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="0671a-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="0671a-p110">Al llamar la función **load** o la función **loadQuery** se registra una solicitud de que se desea ejecutar en el servidor. Ingresa un parámetro que representa el objeto que desea recuperar. Si está trabajando con una propiedad de **ValueObject**, entonces también solicita la propiedad en el parámetro.</span><span class="sxs-lookup"><span data-stu-id="0671a-p110">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server. You pass in a parameter that represents the object that you want to retrieve. If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="0671a-p111">Al llamar la función **executeQueryAsync** se envía la solicitud de consulta al servidor de manera asincrónica. Ingresa una función de devolución de llamada satisfactoria y una función de devolución de llamada insatisfactoria para invocar cuándo se recibe la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="0671a-p111">Calling the **executeQueryAsync** function sends the query request to the server asynchronously. You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="0671a-p112">Para reducir el tráfico de red, solicite solamente las propiedades con las que desee trabajar cuando llame la función **load**. Además, si está trabajando con varios objetos, agrupe varias llamadas en la función **load** antes de llamar la función **executeQueryAsync** cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="0671a-p112">To reduce network traffic, request only the properties that you want to work with when you call the **load** function. In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="0671a-172">Iterar a través de la colección de proyectos</span><span class="sxs-lookup"><span data-stu-id="0671a-172">Iterating through the projects collection</span></span>
<span data-ttu-id="0671a-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-173"></span></span>

<span data-ttu-id="0671a-174">Los siguientes pasos iteran a través de la colección de proyectos (si la llamada del servidor es satisfactoria) o entregan un mensaje de error (si hay un error en la llamada).</span><span class="sxs-lookup"><span data-stu-id="0671a-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="0671a-175">Agregue una función de devolución de llamada satisfactoria que itere a través de la colección de proyectos, de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="0671a-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="0671a-176">Agregue una función de devolución de llamada no satisfactoria que entregue un mensaje de error, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0671a-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="0671a-p113">Para probar la página de aplicación, en la barra de menú, elija **Depurar**, **Iniciar depuración**. Si se le solicita modificar el archivo web.config, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0671a-p113">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="0671a-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-179"></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="0671a-180">Ejemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="0671a-180">Complete code example</span></span>

<span data-ttu-id="0671a-181">A continuación se muestra el código completo del archivo ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="0671a-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="0671a-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="0671a-182"></span></span>

## <a name="see-also"></a><span data-ttu-id="0671a-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="0671a-183">See also</span></span>

- [<span data-ttu-id="0671a-184">Crear, recuperar, actualizar y eliminar proyectos mediante el modelo de objetos de JavaScript de Project Server</span><span class="sxs-lookup"><span data-stu-id="0671a-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="0671a-185">Modelo de objetos de cliente (COM) de Project 2013</span><span class="sxs-lookup"><span data-stu-id="0671a-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="0671a-186">Comenzar con CSOM y .NET de Project Server</span><span class="sxs-lookup"><span data-stu-id="0671a-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

