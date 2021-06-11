---
title: Obtener el identificador del proyecto en una parte del complemento en una página de detalles de Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Los elementos de complemento se hospedan en elementos iframe que están totalmente aislados de la página de hospedaje. Para obtener información sobre el proyecto actual desde un elemento de complemento en la página de detalles de Project (PDP), puede usar el método window.postMessage, un agente de escucha de eventos y un controlador de eventos que analiza el identificador del proyecto del mensaje.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322599"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="a6be2-104">Obtener el identificador del proyecto en una parte del complemento en una página de detalles de Project</span><span class="sxs-lookup"><span data-stu-id="a6be2-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="a6be2-105">Los elementos de complemento se hospedan en elementos **iframe** que están totalmente aislados de la página de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="a6be2-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="a6be2-106">Para obtener información sobre el proyecto actual desde un elemento de complemento en la página de detalles (PDP) de Project, puede usar el método **window.postMessage,** un agente de escucha de eventos y un controlador de eventos que analiza el identificador del proyecto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6be2-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="a6be2-107">Requisitos previos para crear un SharePoint complemento hospedado por el usuario que obtiene el identificador del proyecto</span><span class="sxs-lookup"><span data-stu-id="a6be2-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="a6be2-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="a6be2-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="a6be2-109">Para usar el ejemplo de código de este artículo, necesitará una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="a6be2-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="a6be2-110">SharePoint 2013 y Project Server 2013, configurados para el aislamiento de complementos.</span><span class="sxs-lookup"><span data-stu-id="a6be2-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="a6be2-111">Si está desarrollando de forma remota, el servidor debe admitir la instalación local de complementos o debe instalar el complemento en un sitio para desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="a6be2-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="a6be2-112">SharePoint En línea y Project Online</span><span class="sxs-lookup"><span data-stu-id="a6be2-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="a6be2-113">Visual Studio 2013, Visual Studio 2012 con Office Developer Tools for Visual Studio 2013, o Napa</span><span class="sxs-lookup"><span data-stu-id="a6be2-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="a6be2-114">Permisos suficientes para el usuario que ha iniciado la sesión:</span><span class="sxs-lookup"><span data-stu-id="a6be2-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="a6be2-115">Permisos de administrador local en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a6be2-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="a6be2-116">Leer el acceso a al menos un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a6be2-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="a6be2-117">Permiso para editar páginas en el sitio Project Web App.</span><span class="sxs-lookup"><span data-stu-id="a6be2-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="a6be2-118">Debe iniciar sesión como un usuario distinto de la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a6be2-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="a6be2-119">La cuenta del sistema no tiene permiso para instalar un complemento.</span><span class="sxs-lookup"><span data-stu-id="a6be2-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="a6be2-120">Consulte [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obtener más información acerca de los complementos para Project.</span><span class="sxs-lookup"><span data-stu-id="a6be2-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="a6be2-121">Consulte [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obtener instrucciones sobre la configuración local (incluida cómo deshabilitar la comprobación de bucle atrás, si es necesario).</span><span class="sxs-lookup"><span data-stu-id="a6be2-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="a6be2-122">Si estás desarrollando de forma remota, consulta Desarrollo de aplicaciones [para SharePoint en un sistema remoto.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="a6be2-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="a6be2-123">Crear el complemento SharePoint hospedado por el cliente y el elemento web cliente</span><span class="sxs-lookup"><span data-stu-id="a6be2-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="a6be2-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="a6be2-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="a6be2-125">Abra Visual Studio y elija **Archivo**  >  **nuevo**  >  **Project**.</span><span class="sxs-lookup"><span data-stu-id="a6be2-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="a6be2-126">En el cuadro de diálogo **Nuevo proyecto**, elija **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a6be2-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="a6be2-127">En la **lista** Plantillas, elija **Visual C#** Office/SharePoint Complementos para SharePoint  >    >    >  **2013**.</span><span class="sxs-lookup"><span data-stu-id="a6be2-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="a6be2-128">Asigne al complemento el nombre GetProjectIdAddinPart y, a continuación, elija el **botón** Aceptar.</span><span class="sxs-lookup"><span data-stu-id="a6be2-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="a6be2-129">En el cuadro de diálogo Nuevo complemento **para SharePoint,** escriba la dirección URL del sitio PWA que desea usar para la depuración (por ejemplo: _https://contoso.com/sites/pwasite/_ ).</span><span class="sxs-lookup"><span data-stu-id="a6be2-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="a6be2-130">Elija la **SharePoint hospedada** para hospedar el complemento y, a continuación, elija el **botón** Finalizar.</span><span class="sxs-lookup"><span data-stu-id="a6be2-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="a6be2-131">En **el Explorador de** soluciones, abra el menú contextual del proyecto GetProjectIdAddinPart y, a continuación, elija **Agregar**  >  **nuevo elemento**.</span><span class="sxs-lookup"><span data-stu-id="a6be2-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="a6be2-132">En el cuadro de diálogo Agregar nuevo **elemento,** elija Elemento web cliente **(Host Web),** asigne el nombre GetProjectId al elemento web y, a continuación, elija el **botón** Agregar.</span><span class="sxs-lookup"><span data-stu-id="a6be2-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="a6be2-133">En el **cuadro de diálogo** Crear elemento web cliente, elija la opción Crear un nuevo elemento web cliente y, **a** continuación, elija el **botón** Finalizar.</span><span class="sxs-lookup"><span data-stu-id="a6be2-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="a6be2-134">Obtener el identificador del proyecto en el elemento de complemento</span><span class="sxs-lookup"><span data-stu-id="a6be2-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="a6be2-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="a6be2-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="a6be2-136">El elemento de complemento GetProjectId define su código personalizado en la página GetProjectId.aspx del elemento web cliente.</span><span class="sxs-lookup"><span data-stu-id="a6be2-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="a6be2-137">La lógica que recibe y controla el mensaje se define en el elemento **head** de la página y los controles de página se definen en el elemento **body** de la página.</span><span class="sxs-lookup"><span data-stu-id="a6be2-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="a6be2-138">Abra la página del elemento web GetProjectId.aspx (en la **carpeta** Pages).</span><span class="sxs-lookup"><span data-stu-id="a6be2-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="a6be2-139">En el **elemento head** de la página, reemplace el código entre las etiquetas **de script** por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a6be2-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. <span data-ttu-id="a6be2-140">Agregue el siguiente código en el **elemento body** de la página.</span><span class="sxs-lookup"><span data-stu-id="a6be2-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="a6be2-141">El código define un control span que muestra el identificador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a6be2-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="a6be2-142">En el Elements.xml, cambie opcionalmente el nombre, el título, la descripción y el tamaño predeterminado del elemento de complemento.</span><span class="sxs-lookup"><span data-stu-id="a6be2-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="a6be2-143">En este ejemplo se usan los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="a6be2-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="a6be2-144">Para probar el elemento de complemento, en la barra de menús, elija **Depurar**, **Iniciar depuración**.</span><span class="sxs-lookup"><span data-stu-id="a6be2-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="a6be2-145">Si se le pide que modifique el archivo web.config, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a6be2-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="a6be2-146">Para depurar el elemento de complemento, establezca los puntos de interrupción adecuados en el script que agregó.</span><span class="sxs-lookup"><span data-stu-id="a6be2-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="a6be2-147">Vaya a una página PDP y elija **Editar página** en el menú Herramientas (icono de engranaje).</span><span class="sxs-lookup"><span data-stu-id="a6be2-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="a6be2-148">Agregue el **elemento GetProjectId Title** a un elemento web de la página.</span><span class="sxs-lookup"><span data-stu-id="a6be2-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="a6be2-149">El identificador del proyecto se muestra en el control **span** de la página del elemento web.</span><span class="sxs-lookup"><span data-stu-id="a6be2-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="a6be2-150">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="a6be2-150">Next steps</span></span>
<span data-ttu-id="a6be2-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a6be2-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="a6be2-152">El elemento de complemento de este ejemplo no tiene acceso a Project de servidor ni a SharePoint datos.</span><span class="sxs-lookup"><span data-stu-id="a6be2-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="a6be2-153">Puede usar el identificador del producto para obtener información sobre el proyecto actual mediante una API de cliente, como el modelo de objetos de JavaScript o el servicio REST.</span><span class="sxs-lookup"><span data-stu-id="a6be2-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="a6be2-154">En el AppManifest.xml, especifique los permisos que el complemento necesita para tener acceso a Project de servidor o SharePoint datos.</span><span class="sxs-lookup"><span data-stu-id="a6be2-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="a6be2-155">Consulte [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para obtener información sobre cómo establecer propiedades personalizadas para un elemento de complemento.</span><span class="sxs-lookup"><span data-stu-id="a6be2-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="a6be2-156">Ejemplo: Obtener el identificador del proyecto en un elemento de complemento en una página PDP</span><span class="sxs-lookup"><span data-stu-id="a6be2-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="a6be2-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="a6be2-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="a6be2-158">El siguiente ejemplo es el código completo de la página GetProjectID.aspx del elemento web cliente.</span><span class="sxs-lookup"><span data-stu-id="a6be2-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="a6be2-159">El código registra un agente de escucha de eventos y un controlador de eventos que recibe y analiza un mensaje que contiene el identificador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a6be2-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a><span data-ttu-id="a6be2-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6be2-160">See also</span></span>

- [<span data-ttu-id="a6be2-161">Tareas de programación de Project</span><span class="sxs-lookup"><span data-stu-id="a6be2-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="a6be2-162">Crear un complemento de Project Server hospedado por SharePoint</span><span class="sxs-lookup"><span data-stu-id="a6be2-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="a6be2-163">Crear elementos de complemento para instalarlos con el complemento de SharePoint</span><span class="sxs-lookup"><span data-stu-id="a6be2-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

