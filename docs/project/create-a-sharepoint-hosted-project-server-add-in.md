---
title: Crear un complemento de Project Server hospedado por SharePoint
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: De los tres tipos de aplicaciones que se pueden crear para Project online (autohospedado, hospedado por el proveedor y hospedado en SharePoint), la aplicación hospedada por SharePoint es la más sencilla de crear e implementar.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773760"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a><span data-ttu-id="f5a24-103">Crear un complemento de Project Server hospedado por SharePoint</span><span class="sxs-lookup"><span data-stu-id="f5a24-103">Create a SharePoint-hosted Project Server add-in</span></span>

<span data-ttu-id="f5a24-104">De los tres tipos de aplicaciones que se pueden crear para Project online (autohospedado, hospedado por el proveedor y hospedado en SharePoint), la aplicación hospedada por SharePoint es la más sencilla de crear e implementar.</span><span class="sxs-lookup"><span data-stu-id="f5a24-104">Of the three types of apps that you can create for Project Online (autohosted, provider-hosted, and SharePoint-hosted), the SharePoint-hosted app is the simplest to create and deploy.</span></span> <span data-ttu-id="f5a24-105">Una aplicación hospedada en SharePoint no requiere autenticación de OAuth y no usa Azure o requiere el mantenimiento de un sitio local para los recursos hospedados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5a24-105">A SharePoint-hosted app does not require OAuth authentication, and does not use Azure or require maintenance of a local site for the provider-hosted resources.</span></span> <span data-ttu-id="f5a24-106">La plantilla de **aplicación para SharePoint 2013** en Visual Studio es un marco práctico para desarrollar aplicaciones que se pueden publicar y vender en la tienda Office o implementar en un catálogo de aplicaciones privado en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f5a24-106">The **App for SharePoint 2013** template in Visual Studio is a convenient framework for developing apps that can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> 
  
<span data-ttu-id="f5a24-107">En Project, statusing es un proceso en el que un integrante del grupo puede usar la página tareas en Project Web App para enviar el estado de una tarea asignada, como el número de horas que han trabajado cada día de la semana en trabajar en la tarea.</span><span class="sxs-lookup"><span data-stu-id="f5a24-107">In Project, statusing is a process where a team member can use the Tasks page in Project Web App to submit the status of an assigned task, such as the number of hours worked each day of a week spent working on the task.</span></span> <span data-ttu-id="f5a24-108">El propietario de la asignación (normalmente el jefe de proyecto) puede aprobar o rechazar el estado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-108">The assignment owner (usually the project manager) can approve or reject the status.</span></span> <span data-ttu-id="f5a24-109">Si se aprueba el estado, Project vuelve a calcular la programación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-109">When the status is approved, Project recalculates the schedule.</span></span> <span data-ttu-id="f5a24-110">La aplicación **QuickStatus** muestra tareas asignadas, donde el usuario puede actualizar rápidamente el porcentaje completado y enviar el estado de las asignaciones seleccionadas para su aprobación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-110">The **QuickStatus** app displays assigned tasks, where the user can quickly update percent complete and submit status of the selected assignments for approval.</span></span> <span data-ttu-id="f5a24-111">Aunque la página tareas de Project Web App tiene mucha más funcionalidad, la aplicación **QuickStatus** es un ejemplo que proporciona una interfaz simplificada.</span><span class="sxs-lookup"><span data-stu-id="f5a24-111">Although the Tasks page in Project Web App has much more functionality, the **QuickStatus** app is an example that provides a simplified interface.</span></span> 
  
<span data-ttu-id="f5a24-112">La aplicación **QuickStatus** es un ejemplo para desarrolladores; no está destinada a usarse en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f5a24-112">The **QuickStatus** app is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="f5a24-113">El objetivo principal es mostrar un ejemplo de desarrollo de aplicaciones para Project online, no crear una aplicación de statusing de estado completamente funcional.</span><span class="sxs-lookup"><span data-stu-id="f5a24-113">The primary purpose is to show an example of app development for Project Online, not to create a fully functional statusing app.</span></span> <span data-ttu-id="f5a24-114">Para obtener un mejor enfoque de los estados, consulte la recomendación de [Siguientes pasos](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="f5a24-114">For a better approach to statusing, see the recommendation in [Next steps](#pj15_StatusingApp_NextSteps).</span></span>
  
<span data-ttu-id="f5a24-115">Para obtener información general sobre el estado, vea progreso de la [tarea](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span><span class="sxs-lookup"><span data-stu-id="f5a24-115">For general information about statusing, see [Task progress](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span></span> <span data-ttu-id="f5a24-116">Para obtener más información sobre el desarrollo de complementos para SharePoint y Project Server, vea [Complementos de SharePoint](https://msdn.microsoft.com/library/jj163230.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-116">For more information about developing add-ins for SharePoint and Project Server, see [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).</span></span>

<span data-ttu-id="f5a24-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span></span>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a><span data-ttu-id="f5a24-118">Requisitos previos para crear una aplicación para Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5a24-118">Prerequisites for creating an app for Project Server 2013</span></span>

<span data-ttu-id="f5a24-119">Para desarrollar aplicaciones relativamente sencillas que se puedan implementar en Project online o en una instalación local de Project Server 2013, puede usar Napa, que proporciona un entorno de desarrollo en línea.</span><span class="sxs-lookup"><span data-stu-id="f5a24-119">To develop relatively simple apps that can be deployed to Project Online or to an on-premises installation of Project Server 2013, you can use the Napa, which provide an online development environment.</span></span> <span data-ttu-id="f5a24-120">Para las aplicaciones más complejas, la modificación de la cinta de Project Web App y la depuración más sencilla durante el desarrollo, puede usar Visual Studio 2012 o Visual Studio 2013.</span><span class="sxs-lookup"><span data-stu-id="f5a24-120">For more complex apps, modifying the Project Web App ribbon, and easier debugging during development, you can use Visual Studio 2012 or Visual Studio 2013.</span></span> <span data-ttu-id="f5a24-121">Por ejemplo, con una instalación local, puede comprobar de forma manual las bases de datos de borrador para ver los cambios de la base de datos de Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-121">For example, with an on-premises installation, you can manually check the Drafts datatables for changes in the Project Server database.</span></span> <span data-ttu-id="f5a24-122">En este artículo se muestra cómo realizar el desarrollo de aplicaciones con Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5a24-122">This article shows how to do app development with Visual Studio.</span></span>
  
<span data-ttu-id="f5a24-123">El desarrollo de aplicaciones de Project Server con Visual Studio exige lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f5a24-123">Development of Project Server apps with Visual Studio requires the following:</span></span>
  
- <span data-ttu-id="f5a24-p106">Asegúrese de haber instalado los Service Pack y las actualizaciones de Windows más recientes en el equipo de desarrollo local. El sistema operativo puede ser Windows 7, Windows 8, Windows Server 2008 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p106">Ensure that you have installed the most recent service packs and Windows updates on your local development computer. The operating system can be Windows 7, Windows 8, Windows Server 2008, or Windows Server 2012.</span></span>
    
- <span data-ttu-id="f5a24-126">Debe tener un equipo que tenga instalado SharePoint Server 2013 y Project Server 2013, donde el equipo está configurado para el aislamiento de aplicaciones y la instalación de prueba de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-126">You must have a computer that has SharePoint Server 2013 and Project Server 2013 installed, where the computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="f5a24-127">La instalación de prueba permite a Visual Studio instalar de forma temporal la aplicación para su depuración.</span><span class="sxs-lookup"><span data-stu-id="f5a24-127">Sideloading enables Visual Studio to temporarily install the app for debugging.</span></span> <span data-ttu-id="f5a24-128">Puede usar la instalación local de SharePoint y Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-128">You can use an on-premises installation of SharePoint and Project Server.</span></span> <span data-ttu-id="f5a24-129">Para obtener más información, vea [set up an on-premises Development Environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-129">For more information, see [Set up an on-premises development environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-130">Para una instalación local, configure un dominio de aplicación aislado *antes* de crear un catálogo de aplicaciones corporativo.</span><span class="sxs-lookup"><span data-stu-id="f5a24-130">For an on-premises installation, configure an isolated app domain  *before*  you create a corporate app catalog.</span></span> 
  
- <span data-ttu-id="f5a24-131">El equipo de desarrollo puede ser un equipo remoto que tenga instalado Office Developer Tools para Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f5a24-131">The development computer can be a remote computer that has Office Developer Tools for Visual Studio 2012 installed.</span></span> <span data-ttu-id="f5a24-132">Asegúrese de que ha instalado la versión más reciente; Vea la sección *herramientas* de [descargas de aplicaciones para Office y SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-132">Ensure that you have installed the most recent version; see the  *Tools*  section of the [Apps for Office and SharePoint downloads](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span></span>
    
- <span data-ttu-id="f5a24-133">Compruebe que la instancia de Project Web App que va a usar para el desarrollo y las pruebas es accesible en el explorador.</span><span class="sxs-lookup"><span data-stu-id="f5a24-133">Verify that the Project Web App instance you will be using for development and testing is accessible in the browser.</span></span>
    
<span data-ttu-id="f5a24-134">Para obtener información sobre el uso de las herramientas en línea, vea [configurar un entorno para el desarrollo de aplicaciones para SharePoint en Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-134">For information about using the online tools, see [Set up an environment for developing apps for SharePoint on Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span></span> <span data-ttu-id="f5a24-135">Para ver un tutorial sobre cómo crear una aplicación sencilla para Project Server que use las herramientas en línea, consulte la serie de blogs de EPMSource, [crear su primera aplicación de Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span><span class="sxs-lookup"><span data-stu-id="f5a24-135">For a walkthrough of building a simple app for Project Server that uses the online tools, see the EPMSource blog series, [Building your first Project Server app](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span></span>

<span data-ttu-id="f5a24-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span></span>

## <a name="using-visual-studio-to-create-a-project-server-app"></a><span data-ttu-id="f5a24-137">Empleo de Visual Studio para crear una aplicación de Project Server</span><span class="sxs-lookup"><span data-stu-id="f5a24-137">Using Visual Studio to create a Project Server app</span></span>

<span data-ttu-id="f5a24-138">Office Developer Tools para Visual Studio 2012 incluye una plantilla para aplicaciones de SharePoint que se puede usar con Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f5a24-138">Office Developer Tools for Visual Studio 2012 includes a template for SharePoint apps that can be used with Project Server 2013.</span></span> <span data-ttu-id="f5a24-139">Al crear una solución de aplicación, esta incluye los siguientes archivos para el código personalizado:</span><span class="sxs-lookup"><span data-stu-id="f5a24-139">When you create an app solution, the solution includes the following files for your custom code:</span></span>
  
- <span data-ttu-id="f5a24-p111">**AppManifest.xml** incluye la configuración del título de la aplicación, el ámbito de solicitud de permisos y otras propiedades. El procedimiento 1 incluye los pasos para establecer las propiedades mediante el diseñador de manifiestos.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p111">**AppManifest.xml** includes settings for the app title, permission request scope, and other properties. Procedure 1 includes steps to set the properties by using the Manifest Designer.</span></span> 
    
- <span data-ttu-id="f5a24-142">**Default.aspx** en la carpeta Páginas de la página principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-142">**Default.aspx** in the Pages folder is the main page of the app.</span></span> <span data-ttu-id="f5a24-143">El procedimiento 2 muestra cómo agregar contenido HTML5 para la aplicación **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-143">Procedure 2 shows how to add HTML5 content for the **QuickStatus** app.</span></span> 
    
- <span data-ttu-id="f5a24-144">**App. js** en la carpeta scripts es el archivo principal para el código JavaScript personalizado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-144">**App.js** in the Scripts folder is the primary file for the custom JavaScript code.</span></span> <span data-ttu-id="f5a24-145">En el procedimiento 3 se explica el código JavaScript para la aplicación **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="f5a24-145">Procedure 3 explains the JavaScript code for the **QuickStatus** app.</span></span> 
    
   <span data-ttu-id="f5a24-146">Si agrega controles comerciales como una cuadrícula o un selector de fecha basados en jQuery, puede Agregar referencias a archivos JavaScript adicionales en el archivo default. aspx.</span><span class="sxs-lookup"><span data-stu-id="f5a24-146">If you add commercial controls such as a jQuery-based grid or date picker, you can add references to additional JavaScript files in the Default.aspx file.</span></span>
    
- <span data-ttu-id="f5a24-147">**App.css** en la carpeta Contenido es el archivo principal de los estilos CSS3 personalizados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-147">**App.css** in the Content folder is the primary file for custom CSS3 styles.</span></span> <span data-ttu-id="f5a24-148">Los procedimientos 2 y 3 incluyen información sobre los estilos de las hojas de estilos en cascada (CSS) de la aplicación **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-148">Procedure 2 and Procedure 3 include information about cascading style sheets (CSS) styles for the **QuickStatus** app.</span></span> <span data-ttu-id="f5a24-149">Puede agregar referencias a archivos CSS adicionales en el archivo Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="f5a24-149">You can add references to additional CSS files in the Default.aspx file.</span></span> 
    
- <span data-ttu-id="f5a24-150">**AppIcon. png** en la carpeta Images es el icono de 96 x 96 que la aplicación muestra en la tienda Office o en el catálogo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-150">**AppIcon.png** in the Images folder is the 96 x 96 icon that the app displays in the Office Store or the app catalog.</span></span> 
    
<span data-ttu-id="f5a24-151">Para modificar la cinta de Project Web App, puede Agregar una acción personalizada de la cinta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-151">To modify the Project Web App ribbon, you can add a ribbon custom action.</span></span> <span data-ttu-id="f5a24-152">La sección [Código de ejemplo de la aplicación QuickStatus](#pj15_StatusingApp_Example) incluye el código completo de los archivos Default.aspx, App.js, App.css, Elements.xml y AppManifest.xml modificados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-152">The [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section includes the complete code for the modified Default.aspx, App.js, App.css, Elements.xml, and AppManifest.xml files.</span></span> 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a><span data-ttu-id="f5a24-153">Procedimiento 1.</span><span class="sxs-lookup"><span data-stu-id="f5a24-153">Procedure 1.</span></span> <span data-ttu-id="f5a24-154">Crear un proyecto de aplicación en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5a24-154">To create an app project in Visual Studio</span></span>

1. <span data-ttu-id="f5a24-155">Ejecute Visual Studio 2012 como administrador y, a continuación, seleccione **nuevo proyecto** en la página inicio.</span><span class="sxs-lookup"><span data-stu-id="f5a24-155">Run Visual Studio 2012 as an administrator, and then select **New Project** on the Start page.</span></span> 
    
2. <span data-ttu-id="f5a24-p117">En el cuadro de diálogo **Nuevo proyecto**, expanda los nodos **Plantillas**, **Visual C#** y **Office o SharePoint** y seleccione **Aplicaciones**. Use **.NET Framework 4.5** predeterminado en la lista desplegable del marco de destino en la parte superior del panel central y, a continuación, seleccione **Aplicación de SharePoint 2013** (ilustración 1).</span><span class="sxs-lookup"><span data-stu-id="f5a24-p117">In the **New Project** dialog box, expand the **Templates**, **Visual C#**, and **Office/SharePoint** nodes, and then select **Apps**. Use the default **.NET Framework 4.5** in the target framework drop-down list at the top of the center pane, and then select **App for SharePoint 2013** (see Figure 1).</span></span> 
    
3. <span data-ttu-id="f5a24-158">En el campo **nombre** , escriba QuickStatus, vaya a la ubicación donde desea guardar la aplicación y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-158">In the **Name** field, type QuickStatus, browse to the location where you want to save the app, and then choose **OK**.</span></span>
    
   <span data-ttu-id="f5a24-159">**Ilustración 1. Creación de una aplicación de Project Server en Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="f5a24-159">**Figure 1. Creating a Project Server app in Visual Studio**</span></span>

   <span data-ttu-id="f5a24-160">![Creación de una aplicación de Project Server en Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creación de una aplicación de Project Server en Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="f5a24-160">![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")</span></span>
  
4. <span data-ttu-id="f5a24-161">En el cuadro de diálogo **Nueva aplicación para SharePoint**, rellene los tres campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5a24-161">In the **New app for SharePoint** dialog box, fill in the following three fields:</span></span> 
    
   - <span data-ttu-id="f5a24-162">En el cuadro de texto superior, escriba el nombre que desea que la aplicación muestre en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-162">In the top text box, type the name that you want the app to display in Project Web App.</span></span> <span data-ttu-id="f5a24-163">Por ejemplo, escriba Actualización de estado rápida.</span><span class="sxs-lookup"><span data-stu-id="f5a24-163">For example, type Quick Status Update.</span></span>
    
   - <span data-ttu-id="f5a24-164">Para que el sitio se use para la depuración, escriba la dirección URL de la instancia de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-164">For the site to use for debugging, type the URL of the Project Web App instance.</span></span> <span data-ttu-id="f5a24-165">Por ejemplo, escriba `https://ServerName/ProjectServerName` (reemplazando _ServerName_ y _ProjectServerName_ con sus propios valores) y, a continuación, elija **validar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-165">For example, type  `https://ServerName/ProjectServerName` (replacing  _ServerName_ and  _ProjectServerName_ with your own values), and then choose **Validate**.</span></span> <span data-ttu-id="f5a24-166">Si todo va bien, Visual Studio muestra **Conexión correcta**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-166">If all goes well, Visual Studio shows **Connection successful**.</span></span> <span data-ttu-id="f5a24-167">Si recibe un mensaje de error, asegúrese de que la dirección URL de Project Web App es correcta y de que el equipo de Project Server está configurado para el aislamiento de aplicaciones y la transferencia local de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-167">If you get an error message, ensure that the Project Web App URL is correct and that the Project Server computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="f5a24-168">Para obtener más información, vea la sección [requisitos previos para crear una aplicación para Project Server 2013](#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="f5a24-168">For more information, see the [Prerequisites for creating an app for Project Server 2013](#pj15_StatusingApp_Prerequisites) section.</span></span> 
    
   - <span data-ttu-id="f5a24-169">En la lista desplegable **¿Cómo desea hospedar la aplicación para SharePoint?**, seleccione **Hospedada por SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-169">In the **How do you want to host your app for SharePoint** drop-down list, choose **SharePoint-hosted**.</span></span>
    
   > [!CAUTION]
   > <span data-ttu-id="f5a24-170">Si por error selecciona el tipo de proyecto predeterminado **Hospedada por el proveedor**, Visual Studio crea dos proyectos en la solución: un proyecto **QuickStatus** y un proyecto **QuickStatusWeb**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-170">If you choose the default **Provider-hosted** project type by mistake, Visual Studio creates two projects in the solution: a **QuickStatus** project and a **QuickStatusWeb** project.</span></span> <span data-ttu-id="f5a24-171">Si ve dos proyectos, elimine esa solución y vuelva a empezar.</span><span class="sxs-lookup"><span data-stu-id="f5a24-171">If you see two projects, delete that solution and start again.</span></span> 
  
5. <span data-ttu-id="f5a24-172">Seleccione **Aceptar** para crear la solución **QuickStatus**, el proyecto **QuickStatus** y los archivos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-172">Choose **OK** to create the **QuickStatus** solution, **QuickStatus** project, and default files.</span></span> 
    
6. <span data-ttu-id="f5a24-p121">Abra la vista del diseñador de manifiestos (por ejemplo, haga doble clic en el archivo AppManifest.xml). En la pestaña **General**, el cuadro de texto **Título** debería mostrar el nombre de la aplicación que escribió en el paso 4. Seleccione la pestaña **Permisos** para agregar las siguientes solicitudes de permisos para la aplicación (ilustración 2):</span><span class="sxs-lookup"><span data-stu-id="f5a24-p121">Open the Manifest Designer view (for example, double-click the AppManifest.xml file). On the **General** tab, the **Title** text box should show the app name that you typed in step 4. Choose the **Permissions** tab to add the following permission requests for the app (see Figure 2):</span></span> 
    
   - <span data-ttu-id="f5a24-p122">En la primera fila de la lista **Solicitudes de permiso**, en la columna **Ámbito**, seleccione **Estado** en la lista desplegable. En la columna **Permiso**, seleccione **SubmitStatus**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p122">In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list. In the **Permission** column, choose **SubmitStatus**.</span></span>
    
   - <span data-ttu-id="f5a24-178">Agregue una fila si **Ámbito** es **Varios proyectos** y **Permiso** es **Read**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-178">Add a row where the **Scope** is **Multiple Projects** and the **Permission** is **Read**.</span></span>
    
   <span data-ttu-id="f5a24-179">**Ilustración 2. Establecimiento del ámbito de permisos de una aplicación de estado**</span><span class="sxs-lookup"><span data-stu-id="f5a24-179">**Figure 2. Setting the permission scope for a statusing app**</span></span>

   <span data-ttu-id="f5a24-180">![Definición del ámbito de permisos de una aplicación de estado](media/pj15_CreateStatusingApp_PermissionScope.gif "Definición del ámbito de permisos de una aplicación de estado")</span><span class="sxs-lookup"><span data-stu-id="f5a24-180">![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")</span></span>
  
<span data-ttu-id="f5a24-181">La aplicación **QuickStatus** permite a un usuario de Project Web App leer asignaciones para ese usuario desde varios proyectos, cambiar el porcentaje completado de asignación y enviar la actualización.</span><span class="sxs-lookup"><span data-stu-id="f5a24-181">The **QuickStatus** app enables a Project Web App user to read assignments for that user from multiple projects, change the assignment percent complete, and submit the update.</span></span> <span data-ttu-id="f5a24-182">Los demás ámbitos de solicitud de permisos mostrados en la lista desplegable de la ilustración 2 no son necesarios para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-182">The other permission request scopes shown in the drop-down list in Figure 2 are not required for this app.</span></span> <span data-ttu-id="f5a24-183">Los ámbitos de solicitud de permisos son los permisos que la aplicación solicita en nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="f5a24-183">The permission request scopes are the permissions that the app requests on behalf of the user.</span></span> <span data-ttu-id="f5a24-184">Si el usuario no tiene esos permisos en Project Web App, la aplicación no se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-184">If the user does not have those permissions in Project Web App, the app does not run.</span></span> <span data-ttu-id="f5a24-185">Una aplicación puede tener varios ámbitos de solicitud de permisos, incluidos aquellos para otros permisos de SharePoint, pero debería tener el mínimo necesario para la funcionalidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-185">An app can have multiple permission request scopes, including those for other SharePoint permissions, but should have only the minimum necessary for the app functionality.</span></span> <span data-ttu-id="f5a24-186">Estos son los ámbitos de solicitud de permisos relacionados con Project Server:</span><span class="sxs-lookup"><span data-stu-id="f5a24-186">Following are the permission request scopes that are related to Project Server:</span></span> 

- <span data-ttu-id="f5a24-187">**Recursos de empresa**: permisos de administrador de recursos para leer o escribir información sobre otros usuarios de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-187">**Enterprise Resources**: Resource manager permissions, to read or write information about other Project Web App users.</span></span>
    
- <span data-ttu-id="f5a24-188">**Varios proyectos**: leer o escribir en más de un proyecto donde el usuario tiene los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-188">**Multiple Projects**: Read or write to more than one project, where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="f5a24-189">**Project Server**: requiere que el usuario de la aplicación tenga permisos de administrador para Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-189">**Project Server**: Requires the app user to have administrator permissions for Project Web App.</span></span>
    
- <span data-ttu-id="f5a24-190">**Informes**: Lea el servicio OData de **ProjectData** para Project Web App (solo requiere el permiso de inicio de sesión de Project Web App).</span><span class="sxs-lookup"><span data-stu-id="f5a24-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span></span> 
    
- <span data-ttu-id="f5a24-191">**Proyecto único**: leer o escribir en un proyecto donde el usuario tiene los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-191">**Single Project**: Read or write to a project where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="f5a24-192">**Estado**: enviar actualizaciones de los estados de las asignaciones, como horas trabajadas, porcentaje completado y nuevas asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-192">**Statusing**: Submit updates for status of assignments, such as times worked, percent complete, and new assignments.</span></span>
    
- <span data-ttu-id="f5a24-193">**Flujo de trabajo**: si el usuario tiene permiso para ejecutar flujos de trabajo de Project Server, la aplicación se ejecuta con permisos elevados para el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f5a24-193">**Workflow**: If the user has permission to run Project Server workflows, the app then runs with elevated permissions for the workflow.</span></span>
    
<span data-ttu-id="f5a24-194">Para obtener más información sobre los ámbitos de solicitud de permisos para Project Server 2013, vea la sección *aplicaciones de Project* en [actualizaciones para desarrolladores de Project 2013](updates-for-developers-in-project-2013.md) y [permisos de aplicaciones en SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-194">For more information about permission request scopes for Project Server 2013, see the  *Project apps*  section in [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) and [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span></span>


<span data-ttu-id="f5a24-195"><a name="pj15_StatusingApp_HTML"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-195"><a name="pj15_StatusingApp_HTML"> </a></span></span>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a><span data-ttu-id="f5a24-196">Creación de contenido HTML para la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-196">Creating the HTML content for the QuickStatus app</span></span>

<span data-ttu-id="f5a24-197">Antes de empezar a codificar el contenido HTML, diseñe la interfaz de usuario y la experiencia de usuario de la aplicación QuickStatus (la ilustración 3 muestra un ejemplo de la página completada).</span><span class="sxs-lookup"><span data-stu-id="f5a24-197">Before you start coding the HTML content, design the user interface and user experience for the QuickStatus app (Figure 3 shows an example of the completed page).</span></span> <span data-ttu-id="f5a24-198">Un diseño también puede incluir un esquema de las funciones de JavaScript que interactúan con el código HTML.</span><span class="sxs-lookup"><span data-stu-id="f5a24-198">A design can also include an outline of the JavaScript functions that interact with the HTML code.</span></span> <span data-ttu-id="f5a24-199">Para obtener información general, vea diseño de la [experiencia del usuario para aplicaciones en SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-199">For general information, see [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span></span>
  
<span data-ttu-id="f5a24-200">**Ilustración 3. Diseño de la página de la aplicación QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="f5a24-200">**Figure 3. Design of the QuickStatus app page**</span></span>

<span data-ttu-id="f5a24-201">![Diseño de la página de la aplicación QuickStatus](media/pj15_CreateStatusingApp_AfterRefresh.gif "Diseño de la página de la aplicación QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="f5a24-201">![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")</span></span>
  
<span data-ttu-id="f5a24-202">La aplicación muestra el nombre para mostrar en la parte superior, que es el valor del elemento **Title** de AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="f5a24-202">The app shows the display name at the top, which is the value of the **Title** element in AppManifest.xml.</span></span> 
  
<span data-ttu-id="f5a24-203">De forma predeterminada, la página emplea HTML5.</span><span class="sxs-lookup"><span data-stu-id="f5a24-203">By default, the page uses HTML5.</span></span> <span data-ttu-id="f5a24-204">A continuación se enumeran los elementos HTML estándar de los objetos principales de la IU que la aplicación **QuickStatus** contiene en el cuerpo de la página:</span><span class="sxs-lookup"><span data-stu-id="f5a24-204">Following are the standard HTML elements for the main UI objects that the **QuickStatus** app contains in the body of the page:</span></span> 
  
- <span data-ttu-id="f5a24-205">Un elemento **form** contiene todos los demás elementos de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f5a24-205">A **form** element contains all of the other UI elements.</span></span> 
    
- <span data-ttu-id="f5a24-206">Un elemento **fieldset** crea un contenedor y un borde para la tabla de asignaciones; el elemento secundario **legend** proporciona una etiqueta para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="f5a24-206">A **fieldset** element creates a container and border for the table of assignments; the child **legend** element provides a label for the container.</span></span> 
    
- <span data-ttu-id="f5a24-207">Un elemento **table** incluye un título y solo un encabezado de tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-207">A **table** element includes a caption and only a table header.</span></span> <span data-ttu-id="f5a24-208">Las funciones de JavaScript cambian el título de la tabla y agregan filas para las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-208">JavaScript functions change the table caption and add rows for the assignments.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-209">Para paginar y ordenar fácilmente, una aplicación de producción probablemente emplearía un control de cuadrícula comercial basado en jQuery en lugar de una tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-209">To easily add paging and sorting, a production app would probably use a commercial jQuery-based grid control instead of a table.</span></span> 
  
   <span data-ttu-id="f5a24-210">La tabla incluye columnas para el nombre del proyecto, el nombre de las tareas con una casilla de verificación, el trabajo real, el porcentaje completado, el trabajo restante y la fecha de finalización de la asignación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-210">The table includes columns for the project name, task name with a check box, actual work, percent complete, remaining work, and the assignment finish date.</span></span> <span data-ttu-id="f5a24-211">Las funciones de JavaScript crean la casilla de verificación y el campo de entrada de texto para el porcentaje completado de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="f5a24-211">JavaScript functions create the check box and the text input field for the percent complete of each task.</span></span>
    
- <span data-ttu-id="f5a24-212">Un elemento **input** para que un cuadro de texto establezca el porcentaje completado de todas las asignaciones seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f5a24-212">An **input** element for a text box sets percent complete for all selected assignments.</span></span> 
    
- <span data-ttu-id="f5a24-213">Un elemento **button** envía los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-213">A **button** element submits the status changes.</span></span> 
    
- <span data-ttu-id="f5a24-214">Un elemento **button** actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="f5a24-214">A **button** element refreshes the page.</span></span> 
    
- <span data-ttu-id="f5a24-215">Un elemento **Button** sale de la aplicación y vuelve a la página tareas en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-215">A **button** element exits the app and returns to the Tasks page in Project Web App.</span></span> 
    
<span data-ttu-id="f5a24-216">Los elementos de cuadro de texto y botón inferiores están en elementos **div**, de modo que CSS pueda administrar con facilidad la posición y el aspecto de los objetos de la IU.</span><span class="sxs-lookup"><span data-stu-id="f5a24-216">The bottom text box and button elements are within **div** elements, so that CSS can easily manage the position and appearance of the UI objects.</span></span> <span data-ttu-id="f5a24-217">Una función de JavaScript agrega un párrafo en la parte inferior de la página que contiene los resultados correctos o erróneos de la actualización del estado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-217">A JavaScript function adds a paragraph at the bottom of the page that contains results for success or failure of the status update.</span></span> 
  
### <a name="procedure-2-to-create-the-html-content"></a><span data-ttu-id="f5a24-218">Procedimiento 2.</span><span class="sxs-lookup"><span data-stu-id="f5a24-218">Procedure 2.</span></span> <span data-ttu-id="f5a24-219">Crear el contenido HTML</span><span class="sxs-lookup"><span data-stu-id="f5a24-219">To create the HTML content</span></span>

1. <span data-ttu-id="f5a24-220">En Visual Studio, abra el archivo default. aspx.</span><span class="sxs-lookup"><span data-stu-id="f5a24-220">In Visual Studio, open the Default.aspx file.</span></span>
    
   <span data-ttu-id="f5a24-221">El archivo incluye dos elementos **asp: Content** : el elemento con el `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` atributo se agrega en el encabezado de la página y el elemento con `ContentPlaceHolderID="PlaceHolderMain"` el atributo se coloca dentro del elemento de **cuerpo** de la página.</span><span class="sxs-lookup"><span data-stu-id="f5a24-221">The file includes two **asp:Content** elements: The element with the  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribute is added within the page header, and the element with the  `ContentPlaceHolderID="PlaceHolderMain"` attribute is placed within the page **body** element.</span></span> 
    
2. <span data-ttu-id="f5a24-222">En el `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control del encabezado de página, agregue una referencia al archivo PS. js en el equipo de Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-222">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control for the page header, add a reference to the PS.js file on the Project Server computer.</span></span> <span data-ttu-id="f5a24-223">Para las pruebas y la depuración puede usar PS.debug.js.</span><span class="sxs-lookup"><span data-stu-id="f5a24-223">For testing and debugging, you can use PS.debug.js.</span></span> 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   <span data-ttu-id="f5a24-224">La infraestructura de la aplicación `/_layouts/15/` usa el directorio virtual para el sitio de SharePoint en IIS.</span><span class="sxs-lookup"><span data-stu-id="f5a24-224">The app infrastructure uses the `/_layouts/15/` virtual directory for the SharePoint site in IIS.</span></span> <span data-ttu-id="f5a24-225">El archivo físico es `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span><span class="sxs-lookup"><span data-stu-id="f5a24-225">The physical file is  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-226">Antes de implementar la aplicación para uso de producción, `.debug` Quite de las referencias del script para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f5a24-226">Before you deploy the app for production use, remove  `.debug` from the script references to improve performance.</span></span> 
  
3. <span data-ttu-id="f5a24-227">En el `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control del cuerpo de la página, elimine el elemento **div** generado y, a continuación, agregue el código HTML para los objetos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f5a24-227">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control for the page body, delete the generated **div** element, and then add the HTML code for the UI objects.</span></span> <span data-ttu-id="f5a24-228">El elemento **table** solo contiene una fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-228">The **table** element contains only a header row.</span></span> <span data-ttu-id="f5a24-229">La columna **Nombre de tarea** incluye un control de entrada de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-229">The **Task name** column includes a check box input control.</span></span> <span data-ttu-id="f5a24-230">El texto del elemento **caption** se sustituye por la devolución de llamada **onGetUserNameSuccess** de la función **getUserInfo** del archivo App.js.</span><span class="sxs-lookup"><span data-stu-id="f5a24-230">Text for the **caption** element is replaced by the **onGetUserNameSuccess** callback for the **getUserInfo** function in the App.js file.</span></span> 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. <span data-ttu-id="f5a24-231">En el archivo App.css, agregue el código CSS para la posición y el aspecto de los elementos de la IU.</span><span class="sxs-lookup"><span data-stu-id="f5a24-231">In the App.css file, add CSS code for the position and appearance of the UI elements.</span></span> <span data-ttu-id="f5a24-232">Para ver el código CSS completo de la aplicación **QuickStatus**, consulte la sección [Código de ejemplo de la aplicación QuickStatus](#pj15_StatusingApp_Example).</span><span class="sxs-lookup"><span data-stu-id="f5a24-232">For the complete CSS code of the **QuickStatus** app, see the [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section.</span></span> 
    
<span data-ttu-id="f5a24-233">El procedimiento 3 agrega las funciones de JavaScript para leer las asignaciones y crear las filas de la tabla, así como para cambiar y actualizar el porcentaje completado de la asignación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-233">Procedure 3 adds the JavaScript functions to read the assignments and create the table rows, and to change and update the assignment percent complete.</span></span> <span data-ttu-id="f5a24-234">Los pasos reales son más iterativos en el desarrollo de una aplicación, donde se crean de forma alternativa parte del código HTML, se agregan y se prueban los estilos y las funciones de JavaScript relacionados, se modifica o agrega más código HTML y, a continuación, se repite el proceso.</span><span class="sxs-lookup"><span data-stu-id="f5a24-234">The actual steps are more iterative in developing an app, where you alternately create some of the HTML code, add and test related styles and JavaScript functions, modify or add more HTML code, and then repeat the process.</span></span>

<span data-ttu-id="f5a24-235"><a name="pj15_StatusingApp_JavaScript"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-235"><a name="pj15_StatusingApp_JavaScript"> </a></span></span>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a><span data-ttu-id="f5a24-236">Creación de las funciones JavaScript para la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-236">Creating the JavaScript functions for the QuickStatus app</span></span>

<span data-ttu-id="f5a24-237">La plantilla de Visual Studio de una aplicación de SharePoint incluye el archivo App.js, que contiene el código de inicialización predeterminado que obtiene el contexto de cliente de SharePoint y demuestra las acciones básicas get y set de la página de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-237">The Visual Studio template for a SharePoint app includes the App.js file, which contains default initialization code that gets the SharePoint client context and demonstrates basic get and set actions for the app page.</span></span> <span data-ttu-id="f5a24-238">El espacio de nombres de JavaScript para la biblioteca SP. js del lado cliente de SharePoint es **SP**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-238">The JavaScript namespace for the SharePoint client-side SP.js library is **SP**.</span></span> <span data-ttu-id="f5a24-239">Dado que una aplicación de Project Server usa la biblioteca PS.js, la aplicación emplea el espacio de nombres **PS** para obtener el contexto de cliente y obtener acceso al JSOM de Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-239">Because a Project Server app uses the PS.js library, the app uses the **PS** namespace to get the client context and access the JSOM for Project Server.</span></span> 
  
<span data-ttu-id="f5a24-240">Las funciones de JavaScript en la aplicación **QuickStatus** incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f5a24-240">JavaScript functions in the **QuickStatus** app include the following:</span></span> 
  
- <span data-ttu-id="f5a24-241">El controlador de eventos **ready** del documento se ejecuta al instanciar el modelo de objetos del documento (DOM).</span><span class="sxs-lookup"><span data-stu-id="f5a24-241">The document **ready** event handler runs when the document object model (DOM) is instantiated.</span></span> <span data-ttu-id="f5a24-242">El controlador de eventos **ready** realiza los siguientes cuatro pasos:</span><span class="sxs-lookup"><span data-stu-id="f5a24-242">The **ready** event handler does the following four steps:</span></span> 
    
    1. <span data-ttu-id="f5a24-243">Inicializa la variable global **projContext** con el contexto de cliente del JSOM de Project Server y la variable global **pwaWeb**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-243">Initializes the **projContext** global variable with the client context for the Project Server JSOM and the **pwaWeb** global variable.</span></span> 
        
    2. <span data-ttu-id="f5a24-244">Llama a la función **getUserInfo** para inicializar la variable global **projUser**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-244">Calls the **getUserInfo** function to initialize the **projUser** global variable.</span></span> 
        
    3. <span data-ttu-id="f5a24-245">Llama a la función **getAssignments**, que obtiene datos de asignación concretos del usuario.</span><span class="sxs-lookup"><span data-stu-id="f5a24-245">Calls the **getAssignments** function, which gets specified assignment data for the user.</span></span> 
        
    4. <span data-ttu-id="f5a24-246">Enlaza los controladores de eventos clic a la casilla de verificación del encabezado de la tabla y a las casillas de verificación de cada fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-246">Binds click event handlers to the table header check box, and to the check boxes in each row of the table.</span></span> <span data-ttu-id="f5a24-247">Los controladores de eventos clic administran el atributo **checked** de las casillas de verificación cuando el usuario activa o desactiva cualquier casilla de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-247">The click event handlers manage the **checked** attribute of the check boxes when the user selects or clears any check box in the table.</span></span> 
    
- <span data-ttu-id="f5a24-248">Si la función **getAssignments** es correcta, llama a la función **onGetAssignmentsSuccess**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-248">If the **getAssignments** function is successful, it calls the **onGetAssignmentsSuccess** function.</span></span> <span data-ttu-id="f5a24-249">Esa función inserta una fila en la tabla para cada asignación, inicializa los controles HTML de cada fila y, a continuación, inicializa las propiedades del botón inferior.</span><span class="sxs-lookup"><span data-stu-id="f5a24-249">That function inserts a row in the table for each assignment, initializes the HTML controls in each row, and then initializes the bottom button properties.</span></span> 
    
- <span data-ttu-id="f5a24-250">El controlador de eventos **onClick** del botón **Actualizar** llama a la función **updateAssignments**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-250">The **onClick** event handler for the **Update** button calls the **updateAssignments** function.</span></span> <span data-ttu-id="f5a24-251">Esa función obtiene el valor de porcentaje completado que se aplica a cada asignación seleccionada; si el cuadro de texto de porcentaje completado está vacío, la función obtiene el porcentaje completado de cada asignación seleccionada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-251">That function gets the percent complete value that is applied to each selected assignment; or if the percent complete text box is empty, the function gets the percent complete of each selected assignment in the table.</span></span> <span data-ttu-id="f5a24-252">Entonces, la función **updateAssignments** guarda las actualizaciones de estado y las envía y escribe un mensaje sobre los resultados en la parte inferior de la página.</span><span class="sxs-lookup"><span data-stu-id="f5a24-252">The **updateAssignments** function then saves and submits the status updates and writes a message about the results to the bottom of the page.</span></span> 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a><span data-ttu-id="f5a24-253">Procedimiento 3.</span><span class="sxs-lookup"><span data-stu-id="f5a24-253">Procedure 3.</span></span> <span data-ttu-id="f5a24-254">Crear las funciones JavaScript</span><span class="sxs-lookup"><span data-stu-id="f5a24-254">To create the JavaScript functions</span></span>

1. <span data-ttu-id="f5a24-255">En Visual Studio, abra el archivo App.js y elimine todo el contenido del mismo.</span><span class="sxs-lookup"><span data-stu-id="f5a24-255">In Visual Studio, open the App.js file, and then delete all the content in the file.</span></span>
    
2. <span data-ttu-id="f5a24-256">Agregue las variables globales y el controlador de eventos **ready** del documento.</span><span class="sxs-lookup"><span data-stu-id="f5a24-256">Add the global variables and the document **ready** event handler.</span></span> <span data-ttu-id="f5a24-257">Al objeto **document** se obtiene acceso mediante una función jQuery.</span><span class="sxs-lookup"><span data-stu-id="f5a24-257">The **document** object is accessed by using a jQuery function.</span></span> 
    
   <span data-ttu-id="f5a24-p142">El controlador de eventos clic de la casilla de verificación del encabezado de la tabla establece el estado activado de las casillas de fila. Si todas las casillas de fila están activadas o desactivadas, el controlador de eventos clic de las casillas de fila establece el estado activado de la casilla de encabezado. El controlador de eventos clic además establece el mensaje de resultados en la parte inferior de la página en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p142">The click event handler for the table header check box sets the checked state of the row check boxes. If all of the row check boxes are selected or all are clear, the click event handler for the row check boxes sets the checked state of the header check box. The click event handlers also set the results message at the bottom of the page to an empty string.</span></span>
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. <span data-ttu-id="f5a24-261">Agregue la función **getUserInfo**, que llama a **onGetUserNameSuccess** si la consulta es correcta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-261">Add the **getUserInfo** function, which calls **onGetUserNameSuccess** if the query is successful.</span></span> <span data-ttu-id="f5a24-262">La función **onGetUserNameSuccess** sustituye el contenido del párrafo **caption** por un título de tabla que incluye el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="f5a24-262">The **onGetUserNameSuccess** function replaces the contents of the **caption** paragraph with a table caption that includes the user name.</span></span> 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. <span data-ttu-id="f5a24-263">Agregue la función **getAssignments**, que llama a **onGetAssignmentsSuccess** (paso 5) si la consulta de asignación es correcta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-263">Add the **getAssignments** function, which calls **onGetAssignmentsSuccess** (see step 5) if the assignment query is successful.</span></span> <span data-ttu-id="f5a24-264">La opción **Include** limita la consulta a devolver únicamente los campos especificados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-264">The **Include** option limits the query to return only the fields specified.</span></span> 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. <span data-ttu-id="f5a24-265">Agregue la función **onGetAssignmentsSuccess**, que agrega una fila para cada asignación a la tabla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-265">Add the **onGetAssignmentsSuccess** function, which adds a row for each assignment to the table.</span></span> <span data-ttu-id="f5a24-266">La variable **prevProjName** se usa para determinar si una fila es para otro proyecto.</span><span class="sxs-lookup"><span data-stu-id="f5a24-266">The **prevProjName** variable is used to determine whether a row is for a different project.</span></span> <span data-ttu-id="f5a24-267">Si es así, el nombre del proyecto se muestra en negrita; si no, el nombre del proyecto se establece en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f5a24-267">If so, the project name is shown in a bold font; if not, the project name is set to an empty string.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-268">El JSOM no incluye las propiedades de **TimeSpan** que incluye el CSOM, como **ActualWorkTimeSpan**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-268">The JSOM does not include **TimeSpan** properties that the CSOM includes, such as **ActualWorkTimeSpan**.</span></span> <span data-ttu-id="f5a24-269">En su lugar, el JSOM usa propiedades para el número de milisegundos, como la propiedad [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-269">Instead, the JSOM uses properties for the number of milliseconds, such as the [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) property.</span></span> <span data-ttu-id="f5a24-270">El método para obtener esa propiedad es **Get\_actualWorkMilliseconds**, que devuelve un valor entero.</span><span class="sxs-lookup"><span data-stu-id="f5a24-270">The method to get that property is **get\_actualWorkMilliseconds**, which returns an integer value.</span></span> <span data-ttu-id="f5a24-271">> el método **get_actualWork** devuelve una cadena como "3H".</span><span class="sxs-lookup"><span data-stu-id="f5a24-271">> The **get_actualWork** method returns a string such as "3h".</span></span> <span data-ttu-id="f5a24-272">Podría usar cualquier valor en la aplicación **QuickStatus**, pero mostrarlo de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="f5a24-272">You could use either value in the **QuickStatus** app, but display it differently.</span></span> <span data-ttu-id="f5a24-273">La consulta de las asignaciones incluye ambas propiedades, de modo que puede probar el valor durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="f5a24-273">The assignments query includes both properties, so you can test the value during debugging.</span></span> <span data-ttu-id="f5a24-274">Si quita la variable **actualWork**, también puede quitar la propiedad **ActualWork** de la consulta de las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-274">If you remove the **actualWork** variable, you can also remove the **ActualWork** property in the assignments query.</span></span> 
  
   <span data-ttu-id="f5a24-275">Por último, la función **onGetAssignmentsSuccess** inicializa el botón **Actualizar** y el botón **Actualizar** con controladores de eventos clic.</span><span class="sxs-lookup"><span data-stu-id="f5a24-275">Finally, the **onGetAssignmentsSuccess** function initializes the **Update** button and the **Refresh** button with click event handlers.</span></span> <span data-ttu-id="f5a24-276">El valor de texto del botón **Actualizar** también se podría establecer en el código HTML.</span><span class="sxs-lookup"><span data-stu-id="f5a24-276">The text value of the **Update** button could also be set in the HTML code.</span></span> 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. <span data-ttu-id="f5a24-277">Agregue el controlador de eventos clic **updateAssignments** del botón **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-277">Add the **updateAssignments** click event handler for the **Update** button.</span></span> <span data-ttu-id="f5a24-278">Si el usuario cambia un valor para el porcentaje completado de una tarea o agrega un valor en el cuadro de texto **percentComplete**, dicho valor podría especificarse en varios formatos, como "60", "60%" o "60 %".</span><span class="sxs-lookup"><span data-stu-id="f5a24-278">When the user changes a value for percent complete of a task, or adds a value in the **percentComplete** text box, the value could be entered in several formats such as "60", "60%", or "60 %".</span></span> <span data-ttu-id="f5a24-279">El método **getNumericValue** devuelve el valor numérico del texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="f5a24-279">The **getNumericValue** method returns the numeric value of the input text.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-280">En una aplicación diseñada para uso en producción, los valores de entrada de la información numérica deben incluir validación de campos y comprobación de errores adicional.</span><span class="sxs-lookup"><span data-stu-id="f5a24-280">In an app that is designed for production use, input values for numeric information should include field validation and additional error checking.</span></span> 
  
   <span data-ttu-id="f5a24-281">El ejemplo **updateAssignments** incluye alguna comprobación de errores básica y muestra información en el párrafo **message** de la parte inferior de la página: verde si la consulta de actualización es correcta y roja si hay un error de entrada o la consulta de actualización no es correcta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-281">The **updateAssignments** example includes some basic error checking, and displays information in the **message** paragraph at the bottom of the page—green if the update query is successful and red if there is an input error or the update query is unsuccessful.</span></span> 
    
   <span data-ttu-id="f5a24-282">Antes de usar el método **submitAllStatusUpdates**, la aplicación tiene que guardar las actualizaciones en el servidor mediante el método **PS.StatusAssignmentCollection.update**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-282">Before using the **submitAllStatusUpdates** method, the app must save the updates to the server by using the **PS.StatusAssignmentCollection.update** method.</span></span> 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. <span data-ttu-id="f5a24-283">Agregue la función **exitToPwa** , que usa el parámetro de la cadena de consulta **SPHostUrl** para la dirección URL del sitio de Project Web App de host.</span><span class="sxs-lookup"><span data-stu-id="f5a24-283">Add the **exitToPwa** function, which uses the **SPHostUrl** query string parameter for the URL of the host Project Web App site.</span></span> <span data-ttu-id="f5a24-284">Para regresar a la página tareas, anexe `"/Tasks.aspx"` a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f5a24-284">To navigate back to the Tasks page, append  `"/Tasks.aspx"` to the URL.</span></span> <span data-ttu-id="f5a24-285">Por ejemplo, la variable **spHostUrl** se establecería en `https://ServerName/ProjectServerName/Tasks.aspx`.</span><span class="sxs-lookup"><span data-stu-id="f5a24-285">For example, the **spHostUrl** variable would be set to  `https://ServerName/ProjectServerName/Tasks.aspx`.</span></span>
    
   <span data-ttu-id="f5a24-286">La función **getQueryStringParameter** divide la dirección URL de la página **QuickStatus** para extraer y devolver el parámetro especificado en las opciones de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f5a24-286">The **getQueryStringParameter** function splits the URL of the **QuickStatus** page to extract and return the specified parameter in the URL options.</span></span> <span data-ttu-id="f5a24-287">El siguiente es un ejemplo del valor **document.URL** del documento **QuickStatus** (todo en una línea):</span><span class="sxs-lookup"><span data-stu-id="f5a24-287">Following is an example of the **document.URL** value for the **QuickStatus** document (all on one line):</span></span> 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   <span data-ttu-id="f5a24-288">Para la dirección URL anterior, la función **getQueryStringParameter** devuelve el valor de cadena de `https://ServerName/pwa`consulta **SPHostUrl** ,.</span><span class="sxs-lookup"><span data-stu-id="f5a24-288">For the previous URL, the **getQueryStringParameter** function returns the **SPHostUrl** query string value,  `https://ServerName/pwa`.</span></span> 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

<span data-ttu-id="f5a24-289">Si publica la aplicación **QuickStatus** en este punto y la agrega a Project Web App, la aplicación puede ejecutarse desde la página contenidos del sitio, pero no está disponible para los usuarios de forma sencilla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-289">If you publish the **QuickStatus** app at this point and add it to Project Web App, the app can be run from the Site Contents page, but it is not easily available to users.</span></span> <span data-ttu-id="f5a24-290">Para ayudar a los usuarios a encontrar y ejecutar la aplicación, puede agregar un botón para ella a la cinta de opciones de la página Tareas.</span><span class="sxs-lookup"><span data-stu-id="f5a24-290">To help users find and run the app, you can add a button for it to the ribbon on the Tasks page.</span></span> <span data-ttu-id="f5a24-291">El procedimiento 4 muestra cómo agregar una acción personalizada de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-291">Procedure 4 shows how to add a ribbon custom action.</span></span> 

<span data-ttu-id="f5a24-292"><a name="pj15_StatusingApp_ribbon"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-292"><a name="pj15_StatusingApp_ribbon"> </a></span></span>

### <a name="adding-a-ribbon-custom-action"></a><span data-ttu-id="f5a24-293">Adición de una acción personalizada de cinta</span><span class="sxs-lookup"><span data-stu-id="f5a24-293">Adding a ribbon custom action</span></span>

<span data-ttu-id="f5a24-294">Las fichas, grupos y controles de la cinta de de Project Web App se especifican en el archivo pwaribbon. XML, que `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` se instala en el directorio del equipo que ejecuta Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-294">Ribbon tabs, groups, and controls for Project Web App are specified in the pwaribbon.xml file, which is installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directory on the computer running Project Server.</span></span> <span data-ttu-id="f5a24-295">Para ayudar a diseñar acciones personalizadas para la cinta de Project Web App, la descarga del SDK de Project 2013 incluye una copia de pwaribbon. Xml.</span><span class="sxs-lookup"><span data-stu-id="f5a24-295">To help design custom actions for the Project Web App ribbon, the Project 2013 SDK download includes a copy of pwaribbon.xml.</span></span> 
  
<span data-ttu-id="f5a24-296">Project Web App usa diferentes definiciones de cinta de opciones para la página tareas, en función de si la instancia de Project Web App usa un modo de entrada único que permite a los usuarios escribir valores para el parte de horas y el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f5a24-296">Project Web App uses different ribbon definitions for the Tasks page, depending on whether the Project Web App instance uses single entry mode that enables users to enter values for both the timesheet and task status.</span></span> <span data-ttu-id="f5a24-297">Si tiene permisos administrativos para Project Web App, para determinar el modo de entrada, elija **configuración de PWA** en el menú desplegable configuración en la esquina superior derecha de la página.</span><span class="sxs-lookup"><span data-stu-id="f5a24-297">If you have administrative permissions for Project Web App, to determine the entry mode, choose **PWA Settings** in the drop-down settings menu at the top-right corner of the page.</span></span> <span data-ttu-id="f5a24-298">En la página Configuración de PWA, seleccione **Configuración y valores predeterminados del parte de horas** y luego mire la casilla de verificación **Modo de entrada único** en la parte inferior de la página.</span><span class="sxs-lookup"><span data-stu-id="f5a24-298">On the PWA Settings page, choose **Timesheet Settings and Defaults**, and then look at the **Single Entry Mode** check box at the bottom of the page.</span></span> 
  
<span data-ttu-id="f5a24-299">Si el modo de entrada único está desactivado, la cinta de opciones de la página Tareas es definida por la región Mi trabajo de pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="f5a24-299">When single entry mode is off, the ribbon on the Tasks page is defined by the My Work region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

<span data-ttu-id="f5a24-300">Si el modo de entrada único está activado, la cinta de opciones de la página Tareas es definida por la región Modo vinculado de pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="f5a24-300">When single entry mode is on, the Tasks page ribbon is defined by the Tied Mode region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

<span data-ttu-id="f5a24-301">Aunque los grupos y los controles de cada región parecen similares, un control del modo vinculado puede llamar a una función distinta que el mismo control del modo no vinculado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-301">Although the groups and controls in each region look similar, a control for the tied mode can call a different function than the same control for the non-tied mode.</span></span> <span data-ttu-id="f5a24-302">El procedimiento 4 muestra cómo agregar un control de botón para la aplicación **QuickStatus** si el modo de entrada único está desactivado (la casilla de verificación **Modo de entrada único** está desactivada).</span><span class="sxs-lookup"><span data-stu-id="f5a24-302">Procedure 4 shows how to add a button control for the **QuickStatus** app when single entry mode is off (the **Single Entry Mode** check box is clear).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f5a24-303">Para obtener información general sobre cómo agregar acciones personalizadas a una cinta de opciones o a un menú en una aplicación de SharePoint, vea [crear acciones personalizadas para implementar con aplicaciones para SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-303">For general information about adding custom actions to a ribbon or to a menu in a SharePoint application, see [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span></span> 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a><span data-ttu-id="f5a24-304">Procedimiento 4.</span><span class="sxs-lookup"><span data-stu-id="f5a24-304">Procedure 4.</span></span> <span data-ttu-id="f5a24-305">Agregar una acción personalizada de cinta de opciones a la página Tareas</span><span class="sxs-lookup"><span data-stu-id="f5a24-305">To add a ribbon custom action to the Tasks page</span></span>

1. <span data-ttu-id="f5a24-306">Examine la cinta de la página tareas en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-306">Examine the ribbon on the Tasks page in Project Web App.</span></span> <span data-ttu-id="f5a24-307">Seleccione la pestaña **TAREAS** en la cinta de opciones y planee cómo modificarla.</span><span class="sxs-lookup"><span data-stu-id="f5a24-307">Select the **TASKS** tab on the ribbon and plan how to modify it.</span></span> <span data-ttu-id="f5a24-308">Hay siete grupos, como **Enviar**, **Tareas** y **Periodo**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-308">There are seven groups, such as **Submit**, **Tasks**, and **Period**.</span></span> <span data-ttu-id="f5a24-309">El grupo **Enviar** tiene dos controles, un botón **Guardar** y un menú desplegable **Enviar estado**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-309">The **Submit** group has two controls, a **Save** button and a **Send Status** drop-down menu.</span></span> <span data-ttu-id="f5a24-310">Puede agregar un control en cualquier ubicación de un grupo, agregar un grupo con un control nuevo en cualquier ubicación de la pestaña **TAREAS** o agregar otra pestaña de la cinta de opciones que tenga grupos y controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="f5a24-310">You can add a control at any location in a group, add a group with a new control at any location in the **TASKS** tab, or add another ribbon tab that has custom groups and controls.</span></span> <span data-ttu-id="f5a24-311">En este ejemplo, se agrega un tercer botón al grupo **Enviar**, botón que invoca a la dirección URL de la aplicación **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-311">In this example, we add a third button to the **Submit** group, where the button invokes the URL of the **QuickStatus** app.</span></span> 
    
2. <span data-ttu-id="f5a24-312">En el panel **Explorador de soluciones** de Visual Studio, haga clic con el botón secundario en el proyecto **QuickStatus** y luego agregue un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="f5a24-312">In the **Solution Explorer** pane in Visual Studio, right-click the **QuickStatus** project, and then add a new item.</span></span> <span data-ttu-id="f5a24-313">En el cuadro de diálogo **Agregar nuevo elemento**, seleccione **Acción personalizada de cinta** (ilustración 4).</span><span class="sxs-lookup"><span data-stu-id="f5a24-313">In the **Add New Item** dialog box, choose **Ribbon Custom Action** (see Figure 4).</span></span> <span data-ttu-id="f5a24-314">Por ejemplo, asigne un nombre a la acción personalizada RibbonQuickStatusAction y, a continuación, elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-314">For example, name the custom action RibbonQuickStatusAction, and then choose **Add**.</span></span>
    
   <span data-ttu-id="f5a24-315">**Ilustración 4. Adición de una acción personalizada de cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="f5a24-315">**Figure 4. Adding a ribbon custom action**</span></span>

   <span data-ttu-id="f5a24-316">![Adición de una acción personalizada de cinta](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adición de una acción personalizada de cinta")</span><span class="sxs-lookup"><span data-stu-id="f5a24-316">![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")</span></span>
  
3. <span data-ttu-id="f5a24-p158">En la primera página del asistente **Crear acción personalizada para cinta**, deje seleccionada la opción **Web host**, seleccione **Ninguno** en la lista desplegable del ámbito de acción personalizada y luego seleccione **Siguiente** (ilustración 5). Los elementos de las listas desplegables son relevantes para SharePoint, no para Project Server. Se sustituirá la mayor parte del XML generado para la acción personalizada de modo que se aplique a Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p158">On the first page of the **Create Custom Action for Ribbon** wizard, leave the **Host Web** option selected, choose **None** in the drop-down list for the custom action scope, and then choose **Next** (see Figure 5). The items in the drop-down lists are relevant to SharePoint, not to Project Server. We will replace most of the generated XML for the custom action so that it applies to Project Server.</span></span> 
    
   <span data-ttu-id="f5a24-320">**Ilustración 5. Especificación de propiedades para la acción personalizada de la cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="f5a24-320">**Figure 5. Specifying properties for the ribbon custom action**</span></span>

   <span data-ttu-id="f5a24-321">![Especificación de propiedades de la acción personalizada de cinta](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Especificación de propiedades de la acción personalizada de cinta")</span><span class="sxs-lookup"><span data-stu-id="f5a24-321">![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")</span></span>
  
4. <span data-ttu-id="f5a24-p159">En la página siguiente del asistente **Crear acción personalizada para cinta**, deje todos los valores predeterminados de la configuración y luego seleccione **Finalizar** (ilustración 6). Visual Studio crea la carpeta **RibbonQuickStatusAction**, que contiene un archivo Elements.xml.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p159">On the next page of the **Create Custom Action for Ribbon** wizard, leave all the default values for the settings, and then choose **Finish** (see Figure 6). Visual Studio creates the **RibbonQuickStatusAction** folder, which contains an Elements.xml file.</span></span> 
    
   <span data-ttu-id="f5a24-324">**Ilustración 6. Especificación de la configuración de un control de botón**</span><span class="sxs-lookup"><span data-stu-id="f5a24-324">**Figure 6. Specifying the settings for a button control**</span></span>

   <span data-ttu-id="f5a24-325">![Especificación de la configuración de un control de botón](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Especificación de la configuración de un control de botón")</span><span class="sxs-lookup"><span data-stu-id="f5a24-325">![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")</span></span>
  
5. <span data-ttu-id="f5a24-326">Modifique el código predeterminado generado en el archivo Elements.xml para la acción personalizada de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-326">Modify the default generated code in the Elements.xml file for the ribbon custom action.</span></span> <span data-ttu-id="f5a24-327">Este es el código XML predeterminado:</span><span class="sxs-lookup"><span data-stu-id="f5a24-327">Following is the default XML code:</span></span>
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. <span data-ttu-id="f5a24-328">En el elemento **CustomAction**, elimine los atributos **Sequence** y **Title**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-328">In the **CustomAction** element, delete the **Sequence** attribute and the **Title** attribute.</span></span> 
    
   2. <span data-ttu-id="f5a24-329">Para agregar un control al grupo de **envío** , busque el primer grupo de la `Ribbon.ContextualTabs.MyWork.Home.Groups` colección en el archivo pwaribbon. XML, que es el elemento que empieza, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span><span class="sxs-lookup"><span data-stu-id="f5a24-329">To add a control to the **Submit** group, find the first group in the  `Ribbon.ContextualTabs.MyWork.Home.Groups` collection in the pwaribbon.xml file, which is the element that begins,  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span></span> <span data-ttu-id="f5a24-330">Para agregar un control secundario al grupo **Enviar**, el siguiente código muestra el atributo **Location** correcto del elemento **CommandUIDefinition** del archivo Elements.xml:</span><span class="sxs-lookup"><span data-stu-id="f5a24-330">To add a child control to the **Submit** group, the following code shows the correct **Location** attribute of the **CommandUIDefinition** element in the Elements.xml file:</span></span> 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. <span data-ttu-id="f5a24-331">Cambie los valores de atributo del elemento secundario **Button** de este modo:</span><span class="sxs-lookup"><span data-stu-id="f5a24-331">Change the attribute values of the child **Button** element as follows:</span></span> 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - <span data-ttu-id="f5a24-332">Para convertir el botón en el tercer control del grupo, el atributo **Sequence** puede ser cualquier número mayor que el `Sequence="20"` valor del control de **Estado de envío** existente (que es un elemento **FlyoutAnchor** de pwaribbon. xml).</span><span class="sxs-lookup"><span data-stu-id="f5a24-332">To make the button the third control in the group, the **Sequence** attribute can be any number higher than the  `Sequence="20"` value of the existing **Send Status** control (which is a **FlyoutAnchor** element in pwaribbon.xml).</span></span> <span data-ttu-id="f5a24-333">Por Convención, los números de secuencia de los grupos y `10, 20, 30, …`controles son, lo que permite que los elementos se inserten en posiciones intermedias.</span><span class="sxs-lookup"><span data-stu-id="f5a24-333">By convention, the sequence numbers of groups and controls are  `10, 20, 30, …`, which enables elements to be inserted in intermediate positions.</span></span>
    
       - <span data-ttu-id="f5a24-334">El atributo **Command** especifica el comando que se va a ejecutar en el elemento **CommandUIHandler** (siguiente paso 5.d).</span><span class="sxs-lookup"><span data-stu-id="f5a24-334">The **Command** attribute specifies the command to run in the **CommandUIHandler** element (see the following step 5.d).</span></span> <span data-ttu-id="f5a24-335">Puede simplificar el nombre del comando para hacerlo más sencillo para el siguiente desarrollador.</span><span class="sxs-lookup"><span data-stu-id="f5a24-335">You can simplify the command name to make it easier for the next developer.</span></span> <span data-ttu-id="f5a24-336">Por ejemplo `Command="Invoke_QuickStatus"` , es más fácil de `Command="Invoke_RibbonQuickStatusActionButtonRequest"`leer.</span><span class="sxs-lookup"><span data-stu-id="f5a24-336">For example  `Command="Invoke_QuickStatus"` is easier to read than  `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span></span>
    
       - <span data-ttu-id="f5a24-337">Los atributos Image especifican el icono de 16 x 16 píxeles y el icono 32 x 32 píxeles para el control botón.</span><span class="sxs-lookup"><span data-stu-id="f5a24-337">The image attributes specify the 16 x 16-pixel icon and the 32 x 32-pixel icon for the button control.</span></span> <span data-ttu-id="f5a24-338">En el archivo Elements. XML predeterminado `Image32by32="_layouts/15/images/placeholder32x32.png"` , especifica un punto naranja.</span><span class="sxs-lookup"><span data-stu-id="f5a24-338">In the default Elements.xml file,  `Image32by32="_layouts/15/images/placeholder32x32.png"` specifies an orange dot.</span></span> <span data-ttu-id="f5a24-339">Puede extraer iconos de los archivos de mapa de imágenes (ps16x16. png y ps32x32. png) que se instalan `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` en el directorio en el equipo que ejecuta Project Server.</span><span class="sxs-lookup"><span data-stu-id="f5a24-339">You can extract icons from the image map files (ps16x16.png and ps32x32.png) that are installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directory on the computer running Project Server.</span></span> <span data-ttu-id="f5a24-340">Por ejemplo, el icono 32 x 32 píxeles está en la segunda columna de iconos desde la izquierda y la décima fila hacia abajo desde la parte superior del mapa de imágenes ps32x32. png (la parte superior del icono se encuentra después del final de la novena fila; 9 filas x 32 píxeles/fila = 288 píxeles).</span><span class="sxs-lookup"><span data-stu-id="f5a24-340">For example, the 32 x 32-pixel icon is in the second column of icons from the left and the tenth row down from the top of the ps32x32.png image map (the top of the icon is after the end of the ninth row; 9 rows x 32 pixels/row = 288 pixels).</span></span> 
    
       - <span data-ttu-id="f5a24-341">Para mostrar información sobre herramientas para el control de botón, agregue los atributos **ToolTipTitle** y **ToolTipDescription**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-341">To show a tool tip for the button control, add the **ToolTipTitle** attribute and the **ToolTipDescription** attribute.</span></span> 
    
    4. <span data-ttu-id="f5a24-342">Cambie los atributos del elemento **CommandUIHandler**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-342">Change the attributes of the **CommandUIHandler** element.</span></span> <span data-ttu-id="f5a24-343">Por ejemplo, asegúrese de que el atributo **Command** coincide con el valor del atributo **Command** del elemento **Button**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-343">For example, ensure that the **Command** attribute matches the **Command** attribute value for the **Button** element.</span></span> <span data-ttu-id="f5a24-344">Para el atributo **del commandAction** , `~appWebUrl` es un marcador de posición para la dirección URL de la Página Web de **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="f5a24-344">For the **CommandAction** attribute,  `~appWebUrl` is a placeholder for the URL of the **QuickStatus** webpage.</span></span> <span data-ttu-id="f5a24-345">Si el botón de la cinta de opciones invoca a la aplicación **QuickStatus**, el token **{StandardTokens}** se sustituye por opciones de la dirección URL que incluyen **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber** y **SPAppWebUrl**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-345">When the ribbon button invokes the **QuickStatus** app, the **{StandardTokens}** token is replaced by URL options that include **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**, and **SPAppWebUrl**.</span></span>
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. <span data-ttu-id="f5a24-346">En el **Explorador de soluciones**, abra el diseñador **Feature1.feature** y mueva el elemento **RibbonQuickStatusAction** del panel **Elementos de la solución** al panel **Elementos de la característica**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-346">In **Solution Explorer**, open the **Feature1.feature** designer, and move the **RibbonQuickStatusAction** item from the **Items in the Solution** pane to the **Items in the Feature** pane.</span></span> <span data-ttu-id="f5a24-347">Si a continuación abre el diseñador **Package.package**, el elemento **RibbonQuickStatusAction** estará en el panel **Elementos del paquete**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-347">If you then open the **Package.package** designer, the **RibbonQuickStatusAction** item will be in the **Items in the Package** pane.</span></span> 
    
<span data-ttu-id="f5a24-348">A medida que desarrolla la aplicación y agrega un botón de la cinta, normalmente se prueba la aplicación y se establecen puntos de interrupción en el código JavaScript para la depuración.</span><span class="sxs-lookup"><span data-stu-id="f5a24-348">As you develop the app and add a ribbon button, you normally test the app and set breakpoints in the JavaScript code for debugging.</span></span> <span data-ttu-id="f5a24-349">Si presiona **F5** para comenzar a depurar, Visual Studio compila la aplicación, la implementa en el sitio especificado en la propiedad **Dirección URL del sitio** del proyecto **QuickStatus** y muestra una página que pregunta si confía en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-349">When you press **F5** to start debugging, Visual Studio compiles the app, deploys it to the site that is specified in the **Site URL** property of the **QuickStatus** project, and displays a page that asks whether you trust the app.</span></span> <span data-ttu-id="f5a24-350">Cuando continúa y, a continuación, sale de la aplicación **QuickStatus** , vuelve a la página tareas en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-350">When you proceed and then exit the **QuickStatus** app, it returns to the Tasks page in Project Web App.</span></span> 

> [!NOTE]
> <span data-ttu-id="f5a24-351">La ilustración 7 muestra que el botón **Quick Status** de la pestaña **TAREAS** de la cinta de opciones está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-351">Figure 7 shows that the **Quick Status** button on the **TASKS** tab of the ribbon is disabled.</span></span> <span data-ttu-id="f5a24-352">Después de muchas implementaciones de depuración con Visual Studio, es posible bloquear los controles personalizados de la cinta de opciones al continuar depurando o implementar la aplicación publicada en el mismo servidor de prueba.</span><span class="sxs-lookup"><span data-stu-id="f5a24-352">After many debug deployments with Visual Studio, custom ribbon controls can be blocked when you continue to debug or deploy the published app on the same test server.</span></span> <span data-ttu-id="f5a24-353">Para habilitar el botón, elimine el elemento **RibbonQuickStatusAction** en Visual Studio y cree una nueva acción de la cinta de opciones con un nombre y un Id. distintos.</span><span class="sxs-lookup"><span data-stu-id="f5a24-353">To enable the button, delete the **RibbonQuickStatusAction** item in Visual Studio, and then create a new ribbon action that has a different name and ID.</span></span> <span data-ttu-id="f5a24-354">Si esto no resuelve el problema, intente quitar la aplicación de la instancia de prueba de Project Web App y, a continuación, vuelva a crear la aplicación con un identificador de aplicación diferente.</span><span class="sxs-lookup"><span data-stu-id="f5a24-354">If that doesn't solve the problem, try removing the app from the Project Web App test instance, and then recreate the app with a different app ID.</span></span> 
  
<span data-ttu-id="f5a24-355">**Ilustración 7. Visualización de la información sobre herramientas del botón Quick Status deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="f5a24-355">**Figure 7. Viewing the tooltip of the disabled Quick Status button**</span></span>

<span data-ttu-id="f5a24-356">![Visualización de la información sobre herramientas del botón deshabilitado](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Visualización de la información sobre herramientas del botón deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="f5a24-356">![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")</span></span>
  
<span data-ttu-id="f5a24-357">El procedimiento 5 muestra cómo implementar e instalar la aplicación **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-357">Procedure 5 shows how to deploy and install the **QuickStatus** app.</span></span> <span data-ttu-id="f5a24-358">El procedimiento 6 muestra algunos pasos adicionales a la hora de probar la aplicación una vez instalada.</span><span class="sxs-lookup"><span data-stu-id="f5a24-358">Procedure 6 shows some additional steps in testing the app after you have installed it.</span></span> 

<span data-ttu-id="f5a24-359"><a name="pj15_StatusingApp_Deploying"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-359"><a name="pj15_StatusingApp_Deploying"> </a></span></span>

## <a name="deploying-the-quickstatus-app"></a><span data-ttu-id="f5a24-360">Implementación de la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-360">Deploying the QuickStatus app</span></span>

<span data-ttu-id="f5a24-361">Hay varias formas de implementar una aplicación en una aplicación Web de SharePoint, como Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-361">There are several ways to deploy an app to a SharePoint web application such as Project Web App.</span></span> <span data-ttu-id="f5a24-362">La implementación que se use dependerá de si desea publicar la aplicación en un catálogo privado de SharePoint o en la tienda Office pública, y si SharePoint está instalado de forma local o es un arrendamiento en línea.</span><span class="sxs-lookup"><span data-stu-id="f5a24-362">Which deployment you use will depend on whether you want to publish the app to a private SharePoint catalog or to the public Office Store, and whether SharePoint is installed on-premises or is an online tenancy.</span></span> <span data-ttu-id="f5a24-363">El procedimiento 5 muestra cómo implementar la aplicación **QuickStatus** en una instalación local de un catálogo de aplicaciones privado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-363">Procedure 5 shows how to deploy the **QuickStatus** app to an on-premises installation in a private app catalog.</span></span> <span data-ttu-id="f5a24-364">Para obtener más información, consulte [instalar y administrar aplicaciones para sharepoint 2013](https://technet.microsoft.com/library/fp161232.aspx) y [publicar aplicaciones para SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5a24-364">For more information, see [Install and manage apps for SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) and [Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span></span>
  
> [!NOTE]
> <span data-ttu-id="f5a24-365">La adición de una aplicación a un catálogo de SharePoint exige permisos de administrador de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f5a24-365">Adding an app to a SharePoint catalog requires SharePoint administrator permissions.</span></span> 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a><span data-ttu-id="f5a24-p171">Procedimiento 5. Implementar la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-p171">Procedure 5. To deploy the QuickStatus app</span></span>

1. <span data-ttu-id="f5a24-368">En Visual Studio, guarde todos los archivos y luego haga clic con el botón secundario en el proyecto **QuickStatus** del **Explorador de soluciones** y seleccione **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-368">In Visual Studio, save all of the files, and then right-click the **QuickStatus** project in the **Solution Explorer** and choose **Publish**.</span></span>
    
2. <span data-ttu-id="f5a24-369">Dado que la aplicación **QuickStatus** está hospedada por SharePoint, hay muy pocas opciones para publicar (ilustración 8).</span><span class="sxs-lookup"><span data-stu-id="f5a24-369">Because the **QuickStatus** app is SharePoint-hosted, there are very few options for publishing (see Figure 8).</span></span> <span data-ttu-id="f5a24-370">En el cuadro de diálogo **Publicar aplicaciones para Office y SharePoint**, seleccione **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-370">In the **Publish apps for Office and SharePoint** dialog box, choose **Finish**.</span></span>
    
   <span data-ttu-id="f5a24-371">**Ilustración 8. Publicación de la aplicación QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="f5a24-371">**Figure 8. Publishing the QuickStatus app**</span></span>

   <span data-ttu-id="f5a24-372">![Uso del Asistente para publicación](media/pj15_CreateStatusingApp_PublishWizard.gif "Uso del Asistente para publicación")</span><span class="sxs-lookup"><span data-stu-id="f5a24-372">![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")</span></span>
  
3. <span data-ttu-id="f5a24-373">Copie el archivo QuickStatus. app del `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directorio a un directorio conveniente del equipo local (o al equipo de SharePoint para una instalación local).</span><span class="sxs-lookup"><span data-stu-id="f5a24-373">Copy the QuickStatus.app file from the  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directory to a convenient directory on the local computer (or to the SharePoint computer for an on-premises installation).</span></span> 
    
4. <span data-ttu-id="f5a24-374">En Administración central de SharePoint, seleccione **Aplicaciones** en el Inicio rápido y, luego, **Administrar catálogo de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-374">In SharePoint Central Administration, choose **Apps** in the Quick Launch, and then choose **Manage App Catalog**.</span></span>
    
5. <span data-ttu-id="f5a24-375">Si no existe un catálogo de aplicaciones, cree una colección de sitios para el catálogo de aplicaciones, siguiendo los pasos de la sección *configurar el sitio de catálogo de aplicaciones para una aplicación web* en [Manage The App catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a24-375">If an app catalog does not exist, create a site collection for the app catalog, by following the  *Configure the App Catalog site for a web application*  section in [Manage the App Catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span></span>
    
   <span data-ttu-id="f5a24-376">Si existe un catálogo de aplicaciones, vaya a la dirección URL del sitio en la página Administrar catálogo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-376">If an app catalog exists, navigate to the site URL on the Manage App Catalog page.</span></span> <span data-ttu-id="f5a24-377">Por ejemplo, en los siguientes pasos, el sitio del catálogo de `https://ServerName/sites/TestApps`aplicaciones es.</span><span class="sxs-lookup"><span data-stu-id="f5a24-377">For example, in the following steps, the app catalog site is  `https://ServerName/sites/TestApps`.</span></span>
    
6. <span data-ttu-id="f5a24-p174">En la página del catálogo de aplicaciones, seleccione **Aplicaciones para SharePoint** en el Inicio rápido. En la página Aplicaciones para SharePoint, en la pestaña **ARCHIVOS** de la cinta de opciones, seleccione **Cargar documento**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p174">On the app catalog page, choose **Apps for SharePoint** in the Quick Launch. On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Upload Document**.</span></span>
    
7. <span data-ttu-id="f5a24-380">En el cuadro de diálogo **Agregar un documento**, busque el archivo QuickStatus.app, agregue comentarios de la versión y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-380">In the **Add a document** dialog box, browse for the QuickStatus.app file, add comments for the version, and then choose **OK**.</span></span>
    
8. <span data-ttu-id="f5a24-381">Al agregar una aplicación, también puede agregar información local para la descripción, el icono y otra información local.</span><span class="sxs-lookup"><span data-stu-id="f5a24-381">When you add an app, you can also add local information for the app description, icon, and other information.</span></span> <span data-ttu-id="f5a24-382">En el cuadro de diálogo **apps for SharePoint-QuickStatus. app** , agregue la información que desea mostrar para la aplicación en la colección de sitios de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f5a24-382">In the **Apps for SharePoint - QuickStatus.app** dialog box, add the information that you want to show for the app in the SharePoint site collection.</span></span> <span data-ttu-id="f5a24-383">Por ejemplo, agregue la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="f5a24-383">For example, add the following information:</span></span> 
    
   1. <span data-ttu-id="f5a24-384">Campo de **Descripción breve** : escriba aplicación de prueba de estado rápida.</span><span class="sxs-lookup"><span data-stu-id="f5a24-384">**Short Description** field: Type Quick Status test app.</span></span>
    
   2. <span data-ttu-id="f5a24-385">Campo de **Descripción** : escriba aplicación de prueba para actualizar el porcentaje completado de las tareas de varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="f5a24-385">**Description** field: Type Test app to update percent complete for tasks in multiple projects.</span></span>
    
   3. <span data-ttu-id="f5a24-386">Campos de **dirección URL del icono** : agregue una imagen de 96 x 96 píxeles para el icono de la aplicación a los activos del sitio para el catálogo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-386">**Icon URL** fields: Add a 96 x 96-pixel image for the app icon to the site assets for the app catalog.</span></span> <span data-ttu-id="f5a24-387">Por ejemplo, vaya a `https://ServerName/sites/TestApps`, elija **contenidos del sitio** en el menú desplegable **configuración** , seleccione **activos del sitio**y, a continuación, agregue la imagen quickStatusApp. png.</span><span class="sxs-lookup"><span data-stu-id="f5a24-387">For example, navigate to  `https://ServerName/sites/TestApps`, choose **Site contents** in the **Settings** drop-down menu, choose **Site Assets**, and then add the quickStatusApp.png image.</span></span> <span data-ttu-id="f5a24-388">Haga clic con el botón secundario en el elemento **quickStatusApp**, seleccione **Propiedades** y copie el valor **Dirección (URL)** en el cuadro de diálogo **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-388">Right-click the **quickStatusApp** item, choose **Properties**, and then copy the **Address (URL)** value in the **Properties** dialog box.</span></span> <span data-ttu-id="f5a24-389">Por ejemplo, copie `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`y pegue el valor en el campo Dirección web de **dirección URL del icono** .</span><span class="sxs-lookup"><span data-stu-id="f5a24-389">For example, copy  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, and then paste the value in the **Icon URL** web address field.</span></span> <span data-ttu-id="f5a24-390">Escriba una descripción para el icono, por ejemplo (como en la ilustración 9), escriba Icono de la aplicación QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="f5a24-390">Type a description for the icon, for example (as in Figure 9), type QuickStatus app icon.</span></span> <span data-ttu-id="f5a24-391">Pruebe que la dirección URL sea válida.</span><span class="sxs-lookup"><span data-stu-id="f5a24-391">Test that the URL is valid.</span></span>
    
      <span data-ttu-id="f5a24-392">**Ilustración 9. Adición de una dirección URL de icono para la aplicación QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="f5a24-392">**Figure 9. Adding an icon URL for the QuickStatus app**</span></span>

      <span data-ttu-id="f5a24-393">![Definición de propiedades en SharePoint para la aplicación](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Definición de propiedades en SharePoint para la aplicación")</span><span class="sxs-lookup"><span data-stu-id="f5a24-393">![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")</span></span>
  
   4. <span data-ttu-id="f5a24-394">Campo **Categoría**: seleccione una categoría existente o especifique su propio valor.</span><span class="sxs-lookup"><span data-stu-id="f5a24-394">**Category** field: Choose an existing category, or specify your own value.</span></span> <span data-ttu-id="f5a24-395">Por ejemplo, escriba Estado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-395">For example, type Statusing.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="f5a24-396">Una categoría llamada **Estado** es solo para fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="f5a24-396">A category named **Statusing** is just for testing purposes.</span></span> <span data-ttu-id="f5a24-397">Una categoría típica de las aplicaciones de Project Server es **Administración de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-397">A typical category for Project Server apps is **Project Management**.</span></span> 
  
   5. <span data-ttu-id="f5a24-398">Campo **Nombre del publicador**: escriba el nombre del publicador.</span><span class="sxs-lookup"><span data-stu-id="f5a24-398">**Publisher name** field: Type the name of the publisher.</span></span> <span data-ttu-id="f5a24-399">En este ejemplo, escriba SDK de Project.</span><span class="sxs-lookup"><span data-stu-id="f5a24-399">In this example, type Project SDK.</span></span>
    
   6. <span data-ttu-id="f5a24-400">Campo **habilitado** : para que la aplicación sea visible para los administradores del sitio de Project Web App para su instalación, active la casilla **habilitada** .</span><span class="sxs-lookup"><span data-stu-id="f5a24-400">**Enabled** field: To make the app visible to Project Web App site administrators for installation, select the **Enabled** check box.</span></span> 
    
   7. <span data-ttu-id="f5a24-p180">Los campos adicionales son opcionales. Por ejemplo, puede agregar una dirección URL de soporte y varias imágenes de ayuda para la página de detalles de la aplicación. En la ilustración 9, los campos **Dirección URL de la imagen 1** incluyen la dirección URL de una captura de pantalla de la aplicación y una descripción de la misma.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p180">Additional fields are optional. For example, you can add a support URL and multiple help images for the app details page. In Figure 9, the **Image URL 1** fields include the URL for a screenshot of the app and a description of the screenshot.</span></span> 
    
   8. <span data-ttu-id="f5a24-404">En el cuadro de diálogo **aplicaciones para SharePoint-QuickStatus. app** , elija **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-404">In the **Apps for SharePoint - QuickStatus.app** dialog box, choose **Save**.</span></span> <span data-ttu-id="f5a24-405">En la ilustración 9, el elemento **Actualización de estado rápida** de la biblioteca Aplicaciones para SharePoint está desprotegido para edición, así que en la pestaña **EDITAR** de la cinta de opciones seleccionaría **Proteger** para terminar el proceso (ilustración 10).</span><span class="sxs-lookup"><span data-stu-id="f5a24-405">In Figure 9, the **Quick Status Update** item in the Apps for SharePoint library is checked out for editing, so on the **EDIT** tab of the dialog box ribbon, you would choose **Check In** to complete the process (see Figure 10).</span></span> 
    
      <span data-ttu-id="f5a24-406">**Ilustración 10. La aplicación QuickStatus se agrega a la biblioteca Aplicaciones para SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="f5a24-406">**Figure 10. The QuickStatus app is added to the Apps for SharePoint library.**</span></span>

      <span data-ttu-id="f5a24-407">![La aplicación QuickStatus se agrega a SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "La aplicación QuickStatus se agrega a SharePoint")</span><span class="sxs-lookup"><span data-stu-id="f5a24-407">![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")</span></span>
  
9. <span data-ttu-id="f5a24-408">En Project Web App, en el menú desplegable **configuración** , elija **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-408">In Project Web App, in the **Settings** drop-down menu, choose **Add an app**.</span></span> <span data-ttu-id="f5a24-409">En la página Sus aplicaciones, en el Inicio rápido, seleccione **De su organización** y, a continuación, seleccione **Detalles de la aplicación** para la aplicación **Actualización de estado rápida**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-409">On the Your Apps page, in the Quick Launch, choose **From Your Organization**, and then choose **App Details** for the **Quick Status Update** app.</span></span> <span data-ttu-id="f5a24-410">La ilustración 11 muestra la página de detalles con el icono de la aplicación, la captura de pantalla y otra información que agregó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="f5a24-410">Figure 11 shows the details page with the app icon, screenshot, and other information that you added in the previous step.</span></span> 
    
   <span data-ttu-id="f5a24-411">**Ilustración 11. Empleo de la página de detalles Actualización de estado rápida en Project Web App**</span><span class="sxs-lookup"><span data-stu-id="f5a24-411">**Figure 11. Using the Quick Status Update details page in Project Web App**</span></span>

   <span data-ttu-id="f5a24-412">![Adición de la aplicación QuickStatus a Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adición de la aplicación QuickStatus a Project Web App")</span><span class="sxs-lookup"><span data-stu-id="f5a24-412">![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")</span></span>
  
10. <span data-ttu-id="f5a24-413">En la página de detalles Actualización de estado rápida, seleccione **AGREGARLA**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-413">On the Quick Status Update details page, choose **ADD IT**.</span></span> <span data-ttu-id="f5a24-414">Project Web App muestra un cuadro de diálogo que enumera las operaciones que puede realizar la aplicación QuickStatus (vea la figura 12).</span><span class="sxs-lookup"><span data-stu-id="f5a24-414">Project Web App displays a dialog box that lists the operations that the QuickStatus app can perform (see Figure 12).</span></span> <span data-ttu-id="f5a24-415">La lista de operaciones deriva de los elementos **AppPermissionRequest** del archivo AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="f5a24-415">The list of operations is derived from the **AppPermissionRequest** elements in the AppManifest.xml file.</span></span> 
    
    <span data-ttu-id="f5a24-416">**Ilustración 12. Verificación de la confianza en la aplicación Quick Status**</span><span class="sxs-lookup"><span data-stu-id="f5a24-416">**Figure 12. Verifying that you trust the Quick Status app**</span></span>

    <span data-ttu-id="f5a24-417">![Comprobación de la confianza para la aplicación QuickStatus](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Comprobación de la confianza para la aplicación QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="f5a24-417">![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")</span></span>
  
11. <span data-ttu-id="f5a24-418">En el cuadro de diálogo **¿Confía en Actualización de estado rápida?**, seleccione **Confiar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-418">In the **Do you trust Quick Status Update** dialog box, choose **Trust It**.</span></span> <span data-ttu-id="f5a24-419">La aplicación se agrega a la página contenido del sitio de Project Web App (vea la figura 13).</span><span class="sxs-lookup"><span data-stu-id="f5a24-419">The app is added to the Project Web App Site Contents page (see Figure 13).</span></span>
    
    <span data-ttu-id="f5a24-420">**Ilustración 13. Visualización de la aplicación Quick Status en la página Contenido del sitio**</span><span class="sxs-lookup"><span data-stu-id="f5a24-420">**Figure 13. Viewing the Quick Status app on the Site Contents page**</span></span>

    <span data-ttu-id="f5a24-421">![Visualización de la aplicación QuickStatus en Contenido del sitio](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Visualización de la aplicación QuickStatus en Contenido del sitio")</span><span class="sxs-lookup"><span data-stu-id="f5a24-421">![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")</span></span>
  
<span data-ttu-id="f5a24-422">En la página Contenido del sitio, puede seleccionar el icono **Actualización de estado rápida** para ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5a24-422">On the Site Contents page, you can select the **Quick Status Update** icon to run the app.</span></span>

> [!NOTE]
> <span data-ttu-id="f5a24-423">Para obtener más información sobre la aplicación, en la página contenidos del sitio, elija la región que contiene el nombre de **actualización rápida de estado** y los puntos suspensivos (...). Puede consultar la página acerca de para la aplicación, ver la página de detalles de la aplicación que contiene información sobre los errores de la aplicación, revisar la página de permisos de la aplicación o quitar la aplicación de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-423">For additional commands that provide information about the app, on the Site Contents page, choose the region that contains the **Quick Status Update** name and the ellipsis (...). You can review the About page for the app, view the App Details page that contains information about app errors, review the app permissions page, or remove the app from Project Web App.</span></span> 
  
<span data-ttu-id="f5a24-424">En la página tareas de Project Web App (vea la figura 14), el botón **QuickStatus** debe estar habilitado en la cinta.</span><span class="sxs-lookup"><span data-stu-id="f5a24-424">On the Tasks page in Project Web App (see Figure 14), the **QuickStatus** button should be enabled on the ribbon.</span></span> <span data-ttu-id="f5a24-425">Si el botón **Quick Status** está deshabilitado, pruebe las acciones descritas en la nota de la ilustración 7.</span><span class="sxs-lookup"><span data-stu-id="f5a24-425">If the **Quick Status** button is disabled, try the actions described in the note for Figure 7.</span></span> 

<span data-ttu-id="f5a24-426">**Ilustración 14. Inicio de la aplicación QuickStatus desde la pestaña TAREAS**</span><span class="sxs-lookup"><span data-stu-id="f5a24-426">**Figure 14. Starting the QuickStatus app from the TASKS tab**</span></span>

<span data-ttu-id="f5a24-427">![Inicio de la aplicación QuickStatus desde la pestaña TAREAS](media/pj15_CreateStatusingApp_TasksRibbon.gif "Inicio de la aplicación QuickStatus desde la pestaña TAREAS")</span><span class="sxs-lookup"><span data-stu-id="f5a24-427">![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")</span></span>
  
<span data-ttu-id="f5a24-428">El procedimiento 6 muestra algunas pruebas que se pueden realizar con la aplicación QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="f5a24-428">Procedure 6 shows some tests to make with the QuickStatus app.</span></span>

<span data-ttu-id="f5a24-429"><a name="pj15_StatusingApp_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-429"><a name="pj15_StatusingApp_Testing"> </a></span></span>

## <a name="testing-the-quickstatus-app"></a><span data-ttu-id="f5a24-430">Prueba de la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-430">Testing the QuickStatus app</span></span>

<span data-ttu-id="f5a24-431">Todas las operaciones que un usuario puede probar en la aplicación **QuickStatus** deben probarse en una instalación de prueba de Project Server antes de implementar la aplicación en un servidor de producción o en un inquilino de producción de Project online.</span><span class="sxs-lookup"><span data-stu-id="f5a24-431">Every operation that a user might try in the **QuickStatus** app should be tested on a test installation of Project Server before deploying the app to a production server or to a production tenant of Project Online.</span></span> <span data-ttu-id="f5a24-432">Una instalación de prueba permite cambiar y eliminar asignaciones de los usuarios sin afectar a los proyectos reales.</span><span class="sxs-lookup"><span data-stu-id="f5a24-432">A test installation enables you to change and delete assignments for users without affecting actual projects.</span></span> <span data-ttu-id="f5a24-433">Las pruebas deberían implicar a varios usuarios con distintos conjuntos de permisos, como administrador, jefe de proyecto y miembro de equipo.</span><span class="sxs-lookup"><span data-stu-id="f5a24-433">Testing should also involve several users who have different sets of permissions, such as administrator, project manager, and team member.</span></span> <span data-ttu-id="f5a24-434">Unas pruebas exhaustivas pueden detectar cambios que deberían realizarse en la aplicación y que no eran aparentes en las pruebas durante el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f5a24-434">Thorough testing can uncover changes that should be made in the app, which were not apparent in testing during development.</span></span> <span data-ttu-id="f5a24-435">El procedimiento 6 enumera varias pruebas para la aplicación **QuickStatus**, pero no incluye una serie exhaustiva de pruebas.</span><span class="sxs-lookup"><span data-stu-id="f5a24-435">Procedure 6 lists several tests for the **QuickStatus** app, but does not include an exhaustive series of tests.</span></span> 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a><span data-ttu-id="f5a24-436">Procedimiento 6.</span><span class="sxs-lookup"><span data-stu-id="f5a24-436">Procedure 6.</span></span> <span data-ttu-id="f5a24-437">Probar la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-437">To test the QuickStatus app</span></span>

1. <span data-ttu-id="f5a24-438">Ejecute la aplicación **QuickStatus** en un escenario en el que el usuario no tenga asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-438">Run the **QuickStatus** app where the user has no assignments.</span></span> <span data-ttu-id="f5a24-439">La aplicación debería mostrar un mensaje azul en la parte inferior de la página, por ejemplo, **El nombre de usuario no tiene asignaciones**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-439">The app should show a blue message at the bottom of the page, for example, **User Name has no assignments**.</span></span>
    
   <span data-ttu-id="f5a24-440">Seleccione **Actualizar** y el mensaje cambia a uno verde **Se han actualizado las asignaciones**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-440">Choose **Update**, and the message changes to a green **Assignments have been updated**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="f5a24-441">El comportamiento de la aplicación debería cambiarse de modo que el botón **Actualizar** se deshabilite si no hay asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f5a24-441">The app behavior should be changed so that the **Update** button is disabled when there are no assignments.</span></span> 
  
2. <span data-ttu-id="f5a24-p189">Ejecute la aplicación en un escenario en el que el usuario tenga varias asignaciones en varios proyectos distintos y algunas no estén terminadas. Observe el aspecto de la aplicación y realice las acciones siguientes (ilustración 15):</span><span class="sxs-lookup"><span data-stu-id="f5a24-p189">Run the app where the user has multiple assignments in several different projects and some assignments are not complete. Notice the appearance of the app and perform actions as follows (see Figure 15):</span></span>
    
   1. <span data-ttu-id="f5a24-444">La función **onGetAssignmentsSuccess** crea una fila en la tabla para cada asignación del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="f5a24-444">The **onGetAssignmentsSuccess** function creates a row in the table for each assignment for the current user.</span></span> <span data-ttu-id="f5a24-445">El nombre del proyecto solo aparece una vez, en negrita, para la primera asignación de cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="f5a24-445">The project name shows only once, in a bold font, for the first assignment in each project.</span></span> 
    
   2. <span data-ttu-id="f5a24-p191">Desactive la casilla de verificación del encabezado de columna **Nombre de tarea**. El controlador de eventos clic del encabezado de columna desactiva las demás casillas de verificación de las filas de tareas.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p191">Clear the check box in the **Task name** column header. The table header click event handler clears all of the other check boxes in the task rows.</span></span> 
    
   3. <span data-ttu-id="f5a24-p192">Seleccione todas las tareas. El controlador de eventos clic de cada fila determina si se seleccionan todas las filas y, si es así, selecciona el encabezado de columna **Nombre de tarea**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p192">Select all of the tasks. The click event handler for each row determines whether all rows are selected, and if so, selects the **Task name** column header.</span></span> 
    
   4. <span data-ttu-id="f5a24-p193">Vuelva a desactivar todas las casillas de verificación y seleccione una asignación que tenga algún trabajo restante. Por ejemplo, la ilustración 15 muestra que la tarea superior T1 tiene un 20 % de trabajo restante para finalizar.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p193">Clear all of the check boxes again, and then select one assignment that has some remaining work. For example, Figure 15 shows the top task T1 has 20% remaining work to complete.</span></span>
    
   5. <span data-ttu-id="f5a24-452">En el cuadro de texto **establecer porcentaje completado** , escriba 80 y, a continuación, elija **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-452">In the **Set percent complete** text box, type 80, and then choose **Update**.</span></span> <span data-ttu-id="f5a24-453">La parte inferior de la página debería mostrar un mensaje verde, **Se han actualizado las asignaciones**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-453">The bottom of the page should show a green message, **Assignments have been updated**.</span></span>
    
      <span data-ttu-id="f5a24-454">**Ilustración 15. Actualización de una asignación en la aplicación QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="f5a24-454">**Figure 15. Updating an assignment in the QuickStatus app**</span></span>

      <span data-ttu-id="f5a24-455">![Actualización de una asignación en la aplicación QuickStatus](media/pj15_CreateStatusingApp_Testing1Update.gif "Actualización de una asignación en la aplicación QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="f5a24-455">![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")</span></span>
  
3. <span data-ttu-id="f5a24-456">Seleccione **Actualizar** (ilustración 16).</span><span class="sxs-lookup"><span data-stu-id="f5a24-456">Choose **Refresh** (see Figure 16).</span></span> <span data-ttu-id="f5a24-457">Todas las tareas están seleccionadas de nuevo y la tarea superior muestra 80 % completado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-457">All of the tasks are selected again, and the top task shows 80% complete.</span></span> 
    
      <span data-ttu-id="f5a24-458">**Ilustración 16. Actualización de la página Actualización de estado rápida**</span><span class="sxs-lookup"><span data-stu-id="f5a24-458">**Figure 16. Refreshing the Quick Status Update page**</span></span>

      <span data-ttu-id="f5a24-459">![Actualización de la página de QuickStatus](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Actualización de la página de QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="f5a24-459">![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")</span></span>
  
4. <span data-ttu-id="f5a24-p196">Desactive todas las casillas de verificación y luego seleccione otra tarea. Por ejemplo, seleccione **Nueva tarea de PWA**. Deje vacío el cuadro de texto **Establecer el porcentaje completado**, elimine todo el texto de la columna **% completado** de la tarea seleccionada y seleccione **Actualizar**. Dado que ambos cuadros de texto están vacíos, la aplicación muestra un mensaje de error rojo (ilustración 17).</span><span class="sxs-lookup"><span data-stu-id="f5a24-p196">Clear all of the check boxes, and then select another task. For example, select **New task from PWA**. Leave the **Set percent complete** text box empty, delete all text in the **% complete** column for the selected task, and then choose **Update**. Because both text boxes are empty, the app shows a red error message (see Figure 17).</span></span>
    
      <span data-ttu-id="f5a24-464">**Ilustración 17. Prueba del mensaje de error**</span><span class="sxs-lookup"><span data-stu-id="f5a24-464">**Figure 17. Testing the error message**</span></span>

      <span data-ttu-id="f5a24-465">![Comprobación del mensaje de error](media/pj15_CreateStatusingApp_Testing3Error.gif "Comprobación del mensaje de error")</span><span class="sxs-lookup"><span data-stu-id="f5a24-465">![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")</span></span>
  
5. <span data-ttu-id="f5a24-466">Actualice la tarea anterior al 80 % completado y seleccione **Salir**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-466">Update the previous task to 80% complete, and then choose **Exit**.</span></span> <span data-ttu-id="f5a24-467">La función **exitToPwa** cambia la ubicación de la ventana del explorador a la página tareas de la aplicación host de SharePoint (es decir, https://ServerName/pwa/Tasks.aspx)la dirección URL cambia a.</span><span class="sxs-lookup"><span data-stu-id="f5a24-467">The **exitToPwa** function changes the browser window location to the Tasks page in the SharePoint host application (that is, the URL changes to https://ServerName/pwa/Tasks.aspx).</span></span> <span data-ttu-id="f5a24-468">La ilustración 18 muestra que la tarea **T1** y la tarea **Nueva tarea de PWA** cada una muestra un 80 % completado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-468">Figure 18 shows that the **T1** task and the **New task from PWA** task each show 80% complete.</span></span> 
    
      <span data-ttu-id="f5a24-469">**Ilustración 18. Verificación de que las tareas están actualizadas en Project Web App**</span><span class="sxs-lookup"><span data-stu-id="f5a24-469">**Figure 18. Verifying the tasks are updated in Project Web App**</span></span>

      <span data-ttu-id="f5a24-470">![Comprobación de las tareas actualizadas en Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Comprobación de las tareas actualizadas en Project Web App")</span><span class="sxs-lookup"><span data-stu-id="f5a24-470">![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")</span></span>
  
6. <span data-ttu-id="f5a24-471">Antes de que el estado actualizado se muestre en Project Professional 2013, los cambios deben enviarse para su aprobación y ser aprobados por el jefe de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f5a24-471">Before the updated status shows in Project Professional 2013, the changes must be submitted for approval, and then approved by the project manager.</span></span>
    
<span data-ttu-id="f5a24-472">Las pruebas revelan varios otros cambios que tendrían que realizarse en la aplicación **QuickStatus** para un mejor uso.</span><span class="sxs-lookup"><span data-stu-id="f5a24-472">Testing reveals several other changes that should be made in the **QuickStatus** app for improved usability.</span></span> <span data-ttu-id="f5a24-473">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f5a24-473">For example:</span></span>

- <span data-ttu-id="f5a24-p199">Debería haber comprobaciones de errores adicionales y validación de valores de cuadros de texto. En la actualidad, un usuario puede especificar un valor no numérico o negativo como porcentaje completado, lo que da lugar a un mensaje de error poco descriptivo. Por ejemplo, con un valor negativo, el mensaje de error es **Error al actualizar las asignaciones: PJClientCallableException: StatusingSetDataValueInvalid**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p199">There should be additional error checks and validation of text box values. Currently, a user can enter a non-numeric value or a negative value for percent complete, which results in an unfriendly error message. For example, with a negative value, the error message is **Error updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.</span></span>
    
- <span data-ttu-id="f5a24-477">El mensaje de error de los cuadros de texto en blanco podría enumerar el proyecto y la tarea, además del número de fila.</span><span class="sxs-lookup"><span data-stu-id="f5a24-477">The error message for blank text boxes could list the project and task, in addition to the row number.</span></span>
    
- <span data-ttu-id="f5a24-478">El mensaje de correcto podría incluir una lista de las tareas actualizadas; o si la función **updateAssignments** es correcta, podría realizar una actualización de página automática y mostrar las tareas o los porcentajes actualizados en otro color y en negrita.</span><span class="sxs-lookup"><span data-stu-id="f5a24-478">The success message could include a list of the tasks updated; or if the **updateAssignments** function is successful, it could perform an automatic page refresh and show updated tasks or percentages in a different color and bold font.</span></span> 
    
- <span data-ttu-id="f5a24-p200">Para evitar una tabla muy grande, la tabla de asignaciones debería limitarse a las tareas que tienen menos de un 100 % completado. O bien, agregar una opción para mostrar todas las tareas. Este problema también se podría solucionar mediante el empleo de una cuadrícula basada en jQuery en lugar de una tabla, donde es posible implementar fácilmente el filtrado y la paginación de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="f5a24-p200">To avoid a very large table, the table of assignments should be limited to tasks that are less than 100% complete. Or, add an option to show all tasks. This problem could also be solved by using a jQuery-based grid instead of a table, where you can easily implement filtering and grid paging.</span></span>
    
- <span data-ttu-id="f5a24-482">Dado que la aplicación **QuickStatus** no envía el estado, el icono **Quick Status** de la pestaña **TAREAS** de la cinta de opciones sería más lógicamente el primer icono del grupo **Tareas**, en lugar del último del grupo **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-482">Because the **QuickStatus** app does not submit status, the **Quick Status** icon on the **TASKS** tab of the ribbon would more logically be the first icon in the **Tasks** group, rather than the last icon in the **Submit** group.</span></span> 
    
- <span data-ttu-id="f5a24-483">Dado que la función **onGetAssignmentsSuccess** inicializa el texto del botón **btnSubmitUpdate**, pero los valores de texto de los otros botones son inicializados en HTML, la página se deja en un estado parcialmente inicializado mientras se ejecuta la función **getAssignments**.</span><span class="sxs-lookup"><span data-stu-id="f5a24-483">Because the **onGetAssignmentsSuccess** function initializes the **btnSubmitUpdate** button text, but the other button text values are initialized in HTML, the page is left in a partially initialized state while the **getAssignments** function runs.</span></span> <span data-ttu-id="f5a24-484">Los botones de la página parecerían más coherentes si todos los valores de texto se inicializaran en HTML.</span><span class="sxs-lookup"><span data-stu-id="f5a24-484">Buttons on the page would appear more consistent if the text values were all initialized in HTML.</span></span> 
    
<span data-ttu-id="f5a24-485">Lo que es más importante, el enfoque que emplea la aplicación **QuickStatus**, donde cambia el porcentaje completado de las asignaciones, debería revisarse en una aplicación de producción.</span><span class="sxs-lookup"><span data-stu-id="f5a24-485">Most importantly, the approach that the **QuickStatus** app uses, where it changes percent complete for assignments, should be revised in a production app.</span></span> <span data-ttu-id="f5a24-486">Para obtener más información, consulte la sección [Siguientes pasos](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="f5a24-486">For more information, see the [Next steps](#pj15_StatusingApp_NextSteps) section.</span></span> 

<span data-ttu-id="f5a24-487"><a name="pj15_StatusingApp_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-487"><a name="pj15_StatusingApp_Example"> </a></span></span>

## <a name="example-code-for-the-quickstatus-app"></a><span data-ttu-id="f5a24-488">Código de ejemplo de la aplicación QuickStatus</span><span class="sxs-lookup"><span data-stu-id="f5a24-488">Example code for the QuickStatus app</span></span>

### <a name="defaultaspx-file"></a><span data-ttu-id="f5a24-489">Archivo Default.aspx</span><span class="sxs-lookup"><span data-stu-id="f5a24-489">Default.aspx file</span></span>

<span data-ttu-id="f5a24-490">El siguiente código está en el `Pages\Default.aspx` archivo del proyecto **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="f5a24-490">The following code is in the  `Pages\Default.aspx` file of the **QuickStatus** project:</span></span> 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a><span data-ttu-id="f5a24-491">Archivo App.js</span><span class="sxs-lookup"><span data-stu-id="f5a24-491">App.js file</span></span>

<span data-ttu-id="f5a24-492">El siguiente código está en el `Scripts\App.js` archivo del proyecto **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="f5a24-492">The following code is in the  `Scripts\App.js` file of the **QuickStatus** project:</span></span> 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a><span data-ttu-id="f5a24-493">Archivo app.css</span><span class="sxs-lookup"><span data-stu-id="f5a24-493">App.css file</span></span>

<span data-ttu-id="f5a24-494">El siguiente código CSS está en el `Content\App.css` archivo del proyecto **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="f5a24-494">The following CSS code is in the  `Content\App.css` file of the **QuickStatus** project:</span></span> 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a><span data-ttu-id="f5a24-495">Archivo Elements.xml de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f5a24-495">Elements.xml file for the ribbon</span></span>

<span data-ttu-id="f5a24-496">La siguiente definición de XML, para el botón Agregar de la ficha **tareas** de la cinta de opciones, `RibbonQuickStatusAction\Elements.xml` se encuentra en el archivo del proyecto **QuickStatus** :</span><span class="sxs-lookup"><span data-stu-id="f5a24-496">The following XML definition, for the added button on the **TASKS** tab on the ribbon, is in the  `RibbonQuickStatusAction\Elements.xml` file of the **QuickStatus** project:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a><span data-ttu-id="f5a24-497">Archivo AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="f5a24-497">AppManifest.xml file</span></span>

<span data-ttu-id="f5a24-498">Este es el XML del manifiesto de la aplicación del proyecto **QuickStatus**, que incluye los dos ámbitos de solicitud de permisos necesarios para actualizar el estado de asignación del usuario de la aplicación en varios proyectos:</span><span class="sxs-lookup"><span data-stu-id="f5a24-498">Following is the XML for the app manifest of the **QuickStatus** project, which includes the two permission request scopes that are necessary for updating the app user's assignment status in multiple projects:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a><span data-ttu-id="f5a24-499">Archivo AppIcon.png</span><span class="sxs-lookup"><span data-stu-id="f5a24-499">AppIcon.png file</span></span>

<span data-ttu-id="f5a24-500">La solución completa de Visual Studio para la aplicación **QuickStatus** incluye un archivo AppIcon.png personalizado.</span><span class="sxs-lookup"><span data-stu-id="f5a24-500">The complete Visual Studio solution for the **QuickStatus** app includes a custom AppIcon.png file.</span></span> <span data-ttu-id="f5a24-501">La solución se incluirá en la descarga del SDK de Project 2013.</span><span class="sxs-lookup"><span data-stu-id="f5a24-501">The solution will be included in the Project 2013 SDK download.</span></span> 

<span data-ttu-id="f5a24-502"><a name="pj15_StatusingApp_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-502"><a name="pj15_StatusingApp_NextSteps"> </a></span></span>

## <a name="next-steps"></a><span data-ttu-id="f5a24-503">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f5a24-503">Next steps</span></span>

<span data-ttu-id="f5a24-504">La aplicación **QuickStatus** es un ejemplo relativamente sencillo de cómo escribir aplicaciones que se pueden instalar en project Server 2013 y Project online.</span><span class="sxs-lookup"><span data-stu-id="f5a24-504">The **QuickStatus** app is a relatively simple example of how to write apps that can be installed on Project Server 2013 and Project Online.</span></span> <span data-ttu-id="f5a24-505">La sección [Prueba de la aplicación QuickStatus](#pj15_StatusingApp_Testing) enumera varias mejoras que se pueden realizar para un mejor uso.</span><span class="sxs-lookup"><span data-stu-id="f5a24-505">The [Testing the QuickStatus app](#pj15_StatusingApp_Testing) section lists several improvements that can be made for better usability.</span></span> <span data-ttu-id="f5a24-506">La aplicación **QuickStatus** usa funciones de JavaScript para actualizar el estado de asignación de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="f5a24-506">The **QuickStatus** app uses JavaScript functions to update assignment status for Project Web App.</span></span> <span data-ttu-id="f5a24-507">No obstante, cambiar el porcentaje completado de las asignaciones no es una práctica de administración de proyectos recomendada.</span><span class="sxs-lookup"><span data-stu-id="f5a24-507">But, changing the assignment percent complete is not a recommended project management practice.</span></span> <span data-ttu-id="f5a24-508">Otro enfoque sería actualizar la fecha de inicio real y la duración restante de las tareas asignadas.</span><span class="sxs-lookup"><span data-stu-id="f5a24-508">Another approach would be to update the actual start date and remaining duration of assigned tasks.</span></span> <span data-ttu-id="f5a24-509">Para obtener una descripción de los problemas, consulte la [actualización mejor](https://www.mpug.com/articles/update-better) en el boletín MPUG.</span><span class="sxs-lookup"><span data-stu-id="f5a24-509">For a discussion of the issues, see [Update Better](https://www.mpug.com/articles/update-better) in the MPUG newsletter.</span></span> 

<span data-ttu-id="f5a24-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="f5a24-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="f5a24-511">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5a24-511">See also</span></span>

- [<span data-ttu-id="f5a24-512">Tareas de programación de Project Server </span><span class="sxs-lookup"><span data-stu-id="f5a24-512">Project Server programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="f5a24-513">Complementos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="f5a24-513">SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163230.aspx)
- [<span data-ttu-id="f5a24-514">Administración de actualizaciones de tareas en Project Web App</span><span class="sxs-lookup"><span data-stu-id="f5a24-514">Managing task updates in Project Web App</span></span>](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [<span data-ttu-id="f5a24-515">Crear acciones personalizadas para implementar complementos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="f5a24-515">Create custom actions to deploy with SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163954.aspx)
    

