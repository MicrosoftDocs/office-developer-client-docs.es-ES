---
title: Comenzar con el modelo de objetos de JavaScript de Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: En Project Server 2013, el modelo de objetos de JavaScript se puede usar en proyectos de Project online, móviles y en desarrollo local. En este tema se proporciona una breve introducción al modelo de objetos de JavaScript y, a continuación, se describe cómo crear una página de aplicación que recupera e itera a través de proyectos mediante el modelo de objetos de JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360476"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Comenzar con el modelo de objetos de JavaScript de Project Server 2013

En Project Server 2013, el modelo de objetos de JavaScript se puede usar en proyectos de Project online, móviles y en desarrollo local. En este tema se proporciona una breve introducción al modelo de objetos de JavaScript y, a continuación, se describe cómo crear una página de aplicación que recupera e itera a través de proyectos mediante el modelo de objetos de JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Uso del modelo de objetos de JavaScript de Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Usar el modelo de objetos de JavaScript es una excelente manera de crear una aplicación que se ejecuta en el lado cliente (frente al código de cliente administrado que debe ejecutarse de forma remota). Las aplicaciones pueden usar el modelo de objetos de JavaScript para recuperar o cambiar objetos mediante el envío de llamadas asincrónicas al servidor. Las aplicaciones que usan el modelo de objetos de JavaScript se suelen implementar como complementos de SharePoint, páginas de aplicación y elementos Web personalizados. Para obtener más información, vea "tipos de componentes de SharePoint que pueden estar en una aplicación para SharePoint" en [webs de host, webs de complemento y componentes de SharePoint en sharepoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
El modelo de objetos de JavaScript implementa la funcionalidad principal de Project Server 2013, pero el modelo de objetos de JavaScript y el modelo de objetos de servidor no tienen paridad uno a uno. El punto de entrada al modelo de objetos de JavaScript es el objeto **ProjectContext** , que representa el contexto de cliente de Project Server 2013 y proporciona acceso al contenido y a la funcionalidad del servidor. El modelo de objetos de JavaScript para Project Server 2013 se define en el archivo PS. js, que se encuentra en la `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` ruta de acceso predeterminada en el servidor de aplicaciones. Project Server 2013 también instala el PS. Archivo debug. js en la misma ubicación. PS.Debug.js es una versión no reducida de PS.js que proporciona información de IntelliSense. 
  
El modelo de objetos de JavaScript permite la autenticación de formularios y todas las solicitudes se autentican como el usuario actual. Para obtener más información sobre seguridad y otras consideraciones sobre el diseño de aplicaciones y soluciones personalizadas, vea [autenticación, autorización y seguridad en SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [aspectos importantes de la arquitectura y el desarrollo de complementos de SharePoint horizontal](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)y complementos de [SharePoint en comparación con las soluciones de SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Para obtener acceso a los datos de un sitio de SharePoint de forma remota, SharePoint 2013 proporciona una biblioteca entre dominios que permite realizar llamadas entre dominios del lado cliente. Para obtener más información, vea [acceso a datos de SharePoint 2013 desde complementos con la biblioteca entre dominios](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Muchos conceptos y procesos para usar el modelo de objetos de JavaScript para Project Server 2013 son similares a los de los modelos de objetos de cliente relacionados. Para obtener más información sobre el modelo de objetos de cliente administrado de Project Server 2013, vea **Microsoft. ProjectServer. Client**. Para obtener más información sobre el modelo de objetos de SharePoint 2013JavaScript y el modelo de objetos de cliente administrado, vea [completar operaciones básicas con código de biblioteca de JavaScript en SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) y [completar operaciones básicas con el cliente de SharePoint 2013 código de biblioteca](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Tutorial: creación de una página de aplicación que recupera e itera a través de proyectos
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Aprenda a crear una página de aplicación que muestra el Id., el nombre y la fecha de creación de cada proyecto publicado en un sitio.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Requisitos previos para crear una página de aplicación que recupera e itera a través de proyectos
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Para desarrollar la página de aplicación que se describe en este tema, debe instalar y configurar los siguientes productos:
  
- SharePoint Server 2013
- Project Server 2013 con al menos un proyecto publicado
- Visual Studio 2012
- Office Developer Tools para Visual Studio 2012
    
También debe tener permisos para implementar la extensión en SharePoint Server 2013 y para recuperar proyectos.
  
> [!NOTE]
> En estas instrucciones se da por supuesto que está desarrollando en el equipo que ejecuta Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Creación de la página de aplicación en Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Los siguientes pasos crean un proyecto de SharePoint y una página de aplicación que contiene una tabla y una etiqueta. La tabla muestra información sobre los proyectos y la etiqueta muestra mensajes de error.
  
1. En el equipo que ejecuta Project Server 2013, ejecute Visual Studio 2012 como administrador.
    
2. Cree un proyecto de SharePoint 2013 vacío, como se indica a continuación:
    
    1. En el cuadro de diálogo **Nuevo proyecto**, elija **.NET Framework 4.5** de la lista desplegable en la parte superior del cuadro de diálogo. 
        
    2. En la lista de categorías de plantilla, elija la categoría **SharePoint de Office** y, a continuación, elija la plantilla **SharePoint 2013 Project**. 
        
    3. Asigne al proyecto el nombre GetProjectsJSOM y, a continuación, elija el botón **Aceptar** . 
        
    4. En el cuadro de diálogo **Asistente para la personalización de SharePoint**, elija **Implementar como solución de granja** y, a continuación, elija el botón **Finalizar**. 
    
3. En el explorador de soluciones, edite el valor de la propiedad **dirección URL del sitio** para el proyecto **ProjectsJSOM** de manera que se corresponda con la dirección `https://ServerName/PWA`URL de la instancia de Project Web App (por ejemplo,).
    
4. Abra el menú abreviado del proyecto **GetProjectsJSOM** y, a continuación, agregue una carpeta asignada "Diseños" de SharePoint. 
    
5. En la **** carpeta Layouts, abra el menú contextual de la carpeta **GetProjectsJSOM** y, a continuación, agregue una nueva página de aplicación de SharePoint denominada ProjectsList. aspx.
    
   > [!NOTE]
   > Este ejemplo no usa el archivo de código subyacente que crea Visual Studio 2012 para la página de aplicación. 
  
6. Abra el menú abreviado de la página **ProjectsList.aspx** y elija **Definir como elemento de inicio**.
    
7. En el fragmento de la página **ProjectsList.aspx**, defina una tabla y un marcador de posición de mensaje dentro de las etiquetas de **asp:Content** "principales", de la manera siguiente. 
    
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

### <a name="retrieving-the-projects-collection"></a>Recuperar la colección de proyectos
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Lo siguientes pasos recuperan e inicializan la colección de proyectos.
  
1. Después de la etiqueta de cierre **div**, agregue una etiqueta **SharePoint:ScriptLink** que haga referencia al archivo PS.js, de la siguiente manera. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Debajo de la etiqueta **SharePoint:ScriptLink**, agregue las etiquetas de **script**, de la siguiente manera. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Declare una variable global para almacenar la colección de proyectos, de la siguiente manera.
    
   ```js
   var projects;
   ```

4. Llame al método de **SP.SOD.executeOrDelayUntilScriptLoaded** para asegurarse de que el archivo PS.js se carga antes de que se ejecute su código personalizado. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Agregue una función que conecte con el contexto actual y recupere la colección de proyectos, de la siguiente manera.
    
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

   Algunos objetos de cliente que recupera a través del contexto no contienen ningún dato hasta que se hayan inicializado; es decir, no puede obtener acceso a los valores de propiedad del objeto hasta que el objeto se inicialice. Asimismo, para las propiedades de tipo **ValueObject**, debe solicitar explícitamente la propiedad antes de poder obtener acceso a su valor. (Si intenta tener acceso a una propiedad antes de que se inicialice, recibirá una excepción **excepción propertyorfieldnotinitializedexception** ). 
    
   Para inicializar un objeto, llame al método de **load** (o el método de **loadQuery**) y, a continuación, al método de **executeQueryAsync**. 
    
   - Al llamar la función **load** o la función **loadQuery** se registra una solicitud de que se desea ejecutar en el servidor. Ingresa un parámetro que representa el objeto que desea recuperar. Si está trabajando con una propiedad de **ValueObject**, entonces también solicita la propiedad en el parámetro. 
    
   - Al llamar la función **executeQueryAsync** se envía la solicitud de consulta al servidor de manera asincrónica. Ingresa una función de devolución de llamada satisfactoria y una función de devolución de llamada insatisfactoria para invocar cuándo se recibe la respuesta del servidor. 
    
   Para reducir el tráfico de red, solicite solamente las propiedades con las que desee trabajar cuando llame la función **load**. Además, si está trabajando con varios objetos, agrupe varias llamadas en la función **load** antes de llamar la función **executeQueryAsync** cuando sea posible. 
    
### <a name="iterating-through-the-projects-collection"></a>Iterar a través de la colección de proyectos
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Los siguientes pasos iteran a través de la colección de proyectos (si la llamada del servidor es satisfactoria) o entregan un mensaje de error (si hay un error en la llamada).
  
1. Agregue una función de devolución de llamada satisfactoria que itere a través de la colección de proyectos, de la manera siguiente.
    
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

2. Agregue una función de devolución de llamada no satisfactoria que entregue un mensaje de error, de la siguiente manera.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Para probar la página de aplicación, en la barra de menú, elija **Depurar**, **Iniciar depuración**. Si se le solicita modificar el archivo web.config, elija **Aceptar**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Ejemplo de código completo

A continuación se muestra el código completo del archivo ProjectsList.aspx.
  
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

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>Vea también

- [Crear, recuperar, actualizar y eliminar proyectos con el modelo de objetos de JavaScript de Project Server](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Modelo de objeto del cliente (CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Introducción a .NET y CSOM de Project Server](getting-started-with-the-project-server-csom-and-net.md)
    

