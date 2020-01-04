---
title: Desarrollo de una aplicación de Project Online con el modelo de objetos de cliente
manager: lindalu
ms.date: 12/18/2019
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: 'En este artículo se describe el desarrollo de la aplicación de Microsoft Project Online con .NET Framework 4.0 y CSOM. '
localization_priority: Priority
ms.openlocfilehash: 33ddafe2e3a75039bf55381524accf1a25692885
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825775"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model-csom"></a><span data-ttu-id="7b71f-103">Desarrollo de una aplicación de Project Online con el modelo de objetos de cliente (CSOM)</span><span class="sxs-lookup"><span data-stu-id="7b71f-103">Developing a Project Online application using the client-side object model</span></span>

>[!NOTE] 
><span data-ttu-id="7b71f-104">En este artículo se describe el desarrollo de aplicaciones de Microsoft Project Online con CSOM.</span><span class="sxs-lookup"><span data-stu-id="7b71f-104">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="7b71f-105">Le recomendamos que explore cómo desarrollar aplicaciones con el [nuevo proyecto para la web](https://developer.microsoft.com/es-ES/office/blogs/developing-applications-and-reports-using-the-new-project/).</span><span class="sxs-lookup"><span data-stu-id="7b71f-105">We recommend you explore how to develop applications using the [new Project for the web](https://developer.microsoft.com/es-ES/office/blogs/developing-applications-and-reports-using-the-new-project/).</span></span>
  
## <a name="background"></a><span data-ttu-id="7b71f-106">Fondo</span><span class="sxs-lookup"><span data-stu-id="7b71f-106">Background</span></span>

<span data-ttu-id="7b71f-107">Microsoft Project empezó como una aplicación de escritorio a principios de los años noventa.</span><span class="sxs-lookup"><span data-stu-id="7b71f-107">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="7b71f-108">Hoy, Project es mucho más, como sus diversas modalidades lo confirman:</span><span class="sxs-lookup"><span data-stu-id="7b71f-108">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="7b71f-109">Project Standard Edition es una aplicación de escritorio que se ejecuta como una aplicación independiente.</span><span class="sxs-lookup"><span data-stu-id="7b71f-109">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="7b71f-110">Project Professional Edition es una aplicación de escritorio que puede interactuar con un servidor y compartir datos con él a mayor escala, así como desempeñar las funciones que se encuentran en Project Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="7b71f-110">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="7b71f-111">Project Online es un servicio hospedado de Microsoft que ofrece a las empresas una solución de nivel de departamento de gestión de proyectos para coordinar y administrar proyectos, programas y carteras.</span><span class="sxs-lookup"><span data-stu-id="7b71f-111">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="7b71f-112">Con una oferta diferente a las ediciones de escritorio, Project Online puede mantener y realizar un seguimiento de los detalles de un proyecto a lo largo del ciclo de vida de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-112">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="7b71f-113">Project Server es un servicio hospedado de empresa en el que la empresa administra y protege el servidor con la información del proyecto, el programa y la cartera.</span><span class="sxs-lookup"><span data-stu-id="7b71f-113">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="7b71f-114">Project Server, en virtud de proteger el servidor internamente, ofrece las características orientadas a proyectos, programas y carteras de Project Online hospedado externamente con una mayor capacidad de personalización.</span><span class="sxs-lookup"><span data-stu-id="7b71f-114">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="7b71f-115">Project Online tiene tres conjuntos de API en línea: modelo de objetos de cliente (CSOM), modelo de objetos de JavaScript (JSOM) y transferencia de estado representacional (REST).</span><span class="sxs-lookup"><span data-stu-id="7b71f-115">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="7b71f-116">La implementación de CSOM de .NET es la interfaz preferida para el desarrollo de aplicaciones de Windows que interactúan con espacios empresariales de Project Online.</span><span class="sxs-lookup"><span data-stu-id="7b71f-116">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="7b71f-117">Los entornos típicos para aplicaciones centradas en el usuario incluyen equipos de escritorio de Windows y dispositivos de Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="7b71f-117">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="7b71f-118">Las aplicaciones de back-end escritas con CSOM de .NET pueden conectarse a otros servidores con lógica de negocios y orígenes de datos que son externos a Project Online.</span><span class="sxs-lookup"><span data-stu-id="7b71f-118">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="7b71f-119">Las solicitudes de recuperación en Project Online usan un sistema de consulta similar a LINQ que ofrece varias mejoras sobre funciones básicas de recuperación.</span><span class="sxs-lookup"><span data-stu-id="7b71f-119">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="7b71f-120">La interfaz del modelo de objetos de JavaScript (JSOM) proporciona compatibilidad con exploradores para los complementos de Project Online. Un complemento es una aplicación web que se almacena en el espacio empresarial de Project Online.</span><span class="sxs-lookup"><span data-stu-id="7b71f-120">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="7b71f-121">Cuando un usuario desea ejecutar un complemento, el código para el complemento se descarga y se ejecuta en el explorador del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b71f-121">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="7b71f-122">El modelo REST/Odata proporciona comunicación basada en HTTP. Se recomienda esta interfaz para las aplicaciones en entornos distintos de Windows.</span><span class="sxs-lookup"><span data-stu-id="7b71f-122">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="7b71f-123">Los puntos de conexión de comunicación son los objetos en el sitio de la aplicación web de Project (PWA).</span><span class="sxs-lookup"><span data-stu-id="7b71f-123">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="7b71f-124">Los resultados de proporcionan códigos de estado HTTP normales.</span><span class="sxs-lookup"><span data-stu-id="7b71f-124">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="7b71f-125">Este artículo se centra en una aplicación que utiliza la interfaz CSOM de .NET.</span><span class="sxs-lookup"><span data-stu-id="7b71f-125">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="7b71f-126">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7b71f-126">Prerequisites</span></span>

<span data-ttu-id="7b71f-127">Empiece con un sistema básico con Windows 10 y agregue los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7b71f-127">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="7b71f-128">.Net Framework 4.0 o posterior. Use el marco completo.</span><span class="sxs-lookup"><span data-stu-id="7b71f-128">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="7b71f-129">El sitio de descarga es https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="7b71f-129">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="7b71f-130">Visual Studio 2013 o posterior. Cualquier edición es aceptable.</span><span class="sxs-lookup"><span data-stu-id="7b71f-130">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="7b71f-131">La edición de la comunidad de Visual Studio 2015 se usó para desarrollar la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7b71f-131">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="7b71f-132">La edición de la comunidad está disponible en https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="7b71f-132">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="7b71f-133">SDK de componentes cliente de SharePoint. Project Online y Project Server se colocan por encima de SharePoint y los ensamblados de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7b71f-133">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="7b71f-134">Los componentes de cliente de SharePoint se incluyen en Visual Studio Professional y Enterprise.</span><span class="sxs-lookup"><span data-stu-id="7b71f-134">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="7b71f-135">Si usa Visual Studio Community, la versión más reciente del SDK de Office Developer Tools está disponible en el sitio siguiente: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="7b71f-135">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="7b71f-136">Una cuenta de Project Online. Esto proporciona acceso al sitio de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7b71f-136">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="7b71f-137">Para obtener más información acerca de cómo obtener una cuenta de Project Online, vea https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="7b71f-137">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="7b71f-138">Proyectos en el sitio de hospedaje que se rellenan con información</span><span class="sxs-lookup"><span data-stu-id="7b71f-138">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="7b71f-139">La edición estándar de .NET Framework (4.0 o posterior) es el marco correcto para usar.</span><span class="sxs-lookup"><span data-stu-id="7b71f-139">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="7b71f-140">No use .NET Framework 4 Client Profile.</span><span class="sxs-lookup"><span data-stu-id="7b71f-140">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="7b71f-141">Desarrollo de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7b71f-141">Develop the application</span></span>

<span data-ttu-id="7b71f-142">Al desarrollar una aplicación de escritorio de SharePoint, la interfaz preferida es el modelo de objetos de cliente (CSOM) de Project.</span><span class="sxs-lookup"><span data-stu-id="7b71f-142">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="7b71f-143">Puede descargar los [ejemplos de CSOM de Project](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) de la galería de recursos para desarrolladores de Project en el Centro para desarrolladores de Office.</span><span class="sxs-lookup"><span data-stu-id="7b71f-143">You can download the [Project CSOM samples](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) from the Project Developer resource gallery on the Office Dev Center.</span></span>
  
<span data-ttu-id="7b71f-144">Los dos primeros temas tratan los aspectos básicos: la creación de un proyecto de Visual Studio con ensamblados y espacios de nombres adecuados y el acceso al servidor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7b71f-144">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="7b71f-145">Los temas restantes abordan la recuperación de información a través del CSOM, desde uno a varios objetos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-145">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="7b71f-146">La recuperación de información desde el host es un proceso de dos acciones en las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="7b71f-146">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="7b71f-147">En primer lugar, la aplicación especifica y envía una o varias solicitudes de recuperación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7b71f-147">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="7b71f-148">En segundo lugar, la aplicación emite una notificación en el servidor para ejecutar las consultas enviadas.</span><span class="sxs-lookup"><span data-stu-id="7b71f-148">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="7b71f-149">El servidor responde enviando los resultados de la consulta al cliente.</span><span class="sxs-lookup"><span data-stu-id="7b71f-149">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="7b71f-150">Configuración del proyecto de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7b71f-150">Set up the Visual Studio project</span></span>

<span data-ttu-id="7b71f-151">La configuración de la aplicación consiste en crear un nuevo proyecto, vincular los ensamblados adecuados y declarar los espacios de nombres necesarios.</span><span class="sxs-lookup"><span data-stu-id="7b71f-151">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="7b71f-152">Visual Studio presenta varios tipos de proyectos de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="7b71f-152">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="7b71f-153">Seleccionar un proyecto de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7b71f-153">Select a Visual Studio project</span></span>

1. <span data-ttu-id="7b71f-154">Inicie Visual Studio y seleccione **Iniciar un nuevo proyecto** en la página de inicio.</span><span class="sxs-lookup"><span data-stu-id="7b71f-154">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="7b71f-155">El cuadro de diálogo Nuevo proyecto muestra las plantillas de aplicación disponibles y los campos de datos para cualquier plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7b71f-155">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="7b71f-156">Para esta aplicación, especifique los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-156">For this application, specify the following items.</span></span> <span data-ttu-id="7b71f-157">Las palabras clave que se encuentran en la pantalla tienen un atributo en negrita:</span><span class="sxs-lookup"><span data-stu-id="7b71f-157">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="7b71f-158">En las plantillas instaladas en el panel izquierdo, seleccione **C#** => **Escritorio clásico** => **de Windows**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-158">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="7b71f-159">En la parte superior del panel central, seleccione **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-159">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="7b71f-160">En los tipos de aplicación en el panel central, elija **Aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-160">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="7b71f-161">En la sección inferior, especifique un nombre y una ubicación para el proyecto, así como un nombre de la solución.</span><span class="sxs-lookup"><span data-stu-id="7b71f-161">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="7b71f-162">También en la sección inferior, active la casilla **Crear directorio para la solución**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-162">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="7b71f-163">Haga clic en **Aceptar** para crear un proyecto inicial.</span><span class="sxs-lookup"><span data-stu-id="7b71f-163">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="7b71f-164">Agregar ensamblados</span><span class="sxs-lookup"><span data-stu-id="7b71f-164">Add assemblies</span></span>

<span data-ttu-id="7b71f-165">La solución de VS necesita el ensamblado ProjectServerClient del SDK de Project 2103, un par de ensamblados del SDK de SharePoint y el ensamblado System.Security de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7b71f-165">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="7b71f-166">En el Explorador de soluciones de VS, haga clic con el botón derecho en la entrada Referencias y seleccione **Agregar referencia**</span><span class="sxs-lookup"><span data-stu-id="7b71f-166">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="7b71f-167">en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="7b71f-167">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="7b71f-168">Compruebe **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-168">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="7b71f-169">Si es necesario, haga clic en el botón **Examinar**</span><span class="sxs-lookup"><span data-stu-id="7b71f-169">If needed, click the **Browse…**</span></span> <span data-ttu-id="7b71f-170">en la parte inferior del cuadro de diálogo y navegue hasta el directorio de instalación del SDK de Project 2013 para localizar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-170">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="7b71f-171">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-171">Click **OK**.</span></span> 
    
4. <span data-ttu-id="7b71f-172">Agregue el espacio de nombres PrjoctServer Client al archivo. cs.</span><span class="sxs-lookup"><span data-stu-id="7b71f-172">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="7b71f-173">Agregue los ensamblados de SDK de SharePoint 2013 SDK con la Consola del Administrador de paquetes de NuGet.</span><span class="sxs-lookup"><span data-stu-id="7b71f-173">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="7b71f-174">En el menú Herramientas de VS, haga clic en los siguientes menús: **Herramientas =\> Administrador de paquetes de NuGet =\> Consola del Administrador paquetes**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-174">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="7b71f-175">En la Consola del Administrador de paquetes, escriba el siguiente comando y presione \<ENTRAR\>:</span><span class="sxs-lookup"><span data-stu-id="7b71f-175">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="7b71f-176">La **Consola del Administrador de paquetes** ofrece una descripción de los resultados del comando. El Explorador de soluciones de VS muestra los ensamblados de SharePoint en las referencias del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-176">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="7b71f-177">Agregue los espacios de nombres en el archivo. cs:</span><span class="sxs-lookup"><span data-stu-id="7b71f-177">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="7b71f-178">El ensamblado System.Security forma parte de .NET Framework y se instaló con el marco.</span><span class="sxs-lookup"><span data-stu-id="7b71f-178">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="7b71f-179">La aplicación de ejemplo tiene un espacio de nombres más que proporciona una cadena cifrada en el sistema de hospedaje para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7b71f-179">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="7b71f-180">Una vez autenticada, la aplicación puede obtener acceso a los proyectos en el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7b71f-180">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="7b71f-181">Agregue el espacio de nombres System.Security al archivo. cs de esta forma:</span><span class="sxs-lookup"><span data-stu-id="7b71f-181">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="7b71f-182">En el Explorador de soluciones de VS, haga clic con el botón derecho en la entrada Referencias y seleccione **Agregar referencia**</span><span class="sxs-lookup"><span data-stu-id="7b71f-182">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="7b71f-183">en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="7b71f-183">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="7b71f-184">Seleccione **Ensamblados =\> Framework** en el panel izquierdo del cuadro de diálogo Administrador de referencias y, a continuación, compruebe **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-184">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="7b71f-185">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7b71f-185">Click **OK**.</span></span> 
    
4. <span data-ttu-id="7b71f-186">Agregue el espacio de nombres System.Security al archivo. cs:</span><span class="sxs-lookup"><span data-stu-id="7b71f-186">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="7b71f-187">El inicio del archivo. cs debe contener estos espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="7b71f-187">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="7b71f-188">System</span><span class="sxs-lookup"><span data-stu-id="7b71f-188">System</span></span>
    
- <span data-ttu-id="7b71f-189">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="7b71f-189">System.Collections.Generic</span></span>
    
- <span data-ttu-id="7b71f-190">System.Linq</span><span class="sxs-lookup"><span data-stu-id="7b71f-190">System.Linq</span></span>
    
- <span data-ttu-id="7b71f-191">System.Test</span><span class="sxs-lookup"><span data-stu-id="7b71f-191">System.Test</span></span>
    
- <span data-ttu-id="7b71f-192">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="7b71f-192">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="7b71f-193">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="7b71f-193">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="7b71f-194">System.Security</span><span class="sxs-lookup"><span data-stu-id="7b71f-194">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="7b71f-195">Conectarse con el sistema de hospedaje</span><span class="sxs-lookup"><span data-stu-id="7b71f-195">Connect to the host system</span></span>

<span data-ttu-id="7b71f-196">Project Online es una aplicación de SharePoint, por lo que el uso de la autenticación de SharePoint es el enfoque correcto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-196">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="7b71f-197">El siguiente fragmento de código se prepara para obtener acceso al entorno hospedado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-197">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="7b71f-198">Las preparaciones para obtener acceso a un entorno hospedado incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7b71f-198">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="7b71f-199">Cree un objeto de contexto para los proyectos. Esto se incluye en el siguiente código del fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-199">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="7b71f-200">El contexto se hereda de otros componentes, lo que permite que el sistema administre el contexto del modelo de objetos de Project.</span><span class="sxs-lookup"><span data-stu-id="7b71f-200">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="7b71f-201">Identifique el sitio de host. Esto se hace en el siguiente código del fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-201">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="7b71f-202">Al crear instancias del contexto del proyecto, la aplicación debe proporcionar la raíz de la colección de sitios de proyectos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-202">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="7b71f-203">La aplicación usa una subcadena de la dirección URL de la raíz de los proyectos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-203">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="7b71f-204">Una instantánea de esta ubicación se resalta con un rectángulo rojo en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7b71f-204">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="7b71f-205">La autenticación necesita la cadena desde el principio y a lo largo de la subcadena "pwa".</span><span class="sxs-lookup"><span data-stu-id="7b71f-205">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="7b71f-206">En la lista de código, la aplicación usa la cadena "https://XXXXXXXX.sharepoint.com/sites/pwa".</span><span class="sxs-lookup"><span data-stu-id="7b71f-206">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="7b71f-207">![Captura de pantalla de la dirección URL de la colección de sitios de proyectos dentro de un borde rojo.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Captura de pantalla de la dirección URL de la colección de sitios de proyectos dentro de un borde rojo.")</span><span class="sxs-lookup"><span data-stu-id="7b71f-207">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border.")</span></span>
  
3. <span data-ttu-id="7b71f-208">Coloque la contraseña en una cadena segura. Esto se hace en el siguiente código del fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-208">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="7b71f-209">La contraseña y la cuenta de usuario son las credenciales para obtener acceso al sitio de host.</span><span class="sxs-lookup"><span data-stu-id="7b71f-209">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="7b71f-210">Agregue la cuenta de usuario y la contraseña a la parte de las credenciales del objeto de contexto. Esto se hace en el siguiente código desde el fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-210">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="7b71f-211">El contexto del proyecto con instancias está listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="7b71f-211">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="7b71f-212">Lista de todos los proyectos publicados</span><span class="sxs-lookup"><span data-stu-id="7b71f-212">List all published projects</span></span>

<span data-ttu-id="7b71f-213">Project Online y ProjectServer usan servidores proxy para comunicarse con el servidor en relación con la creación, la notificación y la actualización de operaciones (CRUD).</span><span class="sxs-lookup"><span data-stu-id="7b71f-213">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="7b71f-214">El servidor/host administra las solicitudes de manera eficiente y es el cliente el que realiza las siguientes acciones en la comunicación con el servidor:</span><span class="sxs-lookup"><span data-stu-id="7b71f-214">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="7b71f-215">Establezca un contexto de para la comunicación.</span><span class="sxs-lookup"><span data-stu-id="7b71f-215">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="7b71f-216">El contexto se utiliza mediante la colección de proyectos, así como otros objetos y colecciones a través de la herencia, incluida la colección de tareas, la colección de asignaciones, el objeto de fase y los campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7b71f-216">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="7b71f-217">Use el modelo de objetos para especificar un objeto, una colección o datos para recuperar.</span><span class="sxs-lookup"><span data-stu-id="7b71f-217">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="7b71f-218">Este paso utiliza LINQ como consulta o método.</span><span class="sxs-lookup"><span data-stu-id="7b71f-218">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="7b71f-219">La especificación controla lo que usted recibe.</span><span class="sxs-lookup"><span data-stu-id="7b71f-219">The specification controls what you receive.</span></span> <span data-ttu-id="7b71f-220">A menudo, este paso se inserta como el cuerpo del método Load (paso 3).</span><span class="sxs-lookup"><span data-stu-id="7b71f-220">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="7b71f-221">Cargue la especificación de recuperación en el paso anterior con el método Load() o LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="7b71f-221">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="7b71f-222">Para cargar colecciones y objetos, use Load().</span><span class="sxs-lookup"><span data-stu-id="7b71f-222">For loading collections and objects, use Load().</span></span> <span data-ttu-id="7b71f-223">Para las consultas con cláusulas como "where" y "group", use LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="7b71f-223">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="7b71f-224">Ejecute la solicitud mediante el método ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="7b71f-224">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="7b71f-225">El método ExecuteQuery() notifica al host que la consulta o consultas están listas para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="7b71f-225">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="7b71f-226">Cuando el host recibe la notificación, se ejecutan las consultas y envían los resultados al cliente.</span><span class="sxs-lookup"><span data-stu-id="7b71f-226">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="7b71f-227">Con la información en el cliente, la aplicación puede usarla.</span><span class="sxs-lookup"><span data-stu-id="7b71f-227">With the information at the client, the application can use it.</span></span> <span data-ttu-id="7b71f-228">El siguiente fragmento de código recorre los proyectos publicados e imprime el identificador y el nombre de cada proyecto publicado en el host.</span><span class="sxs-lookup"><span data-stu-id="7b71f-228">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="7b71f-229">Resultado:</span><span class="sxs-lookup"><span data-stu-id="7b71f-229">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="7b71f-230">Hacer una solicitud</span><span class="sxs-lookup"><span data-stu-id="7b71f-230">Make a request</span></span>

<span data-ttu-id="7b71f-231">Mediante las acciones del fragmento de código anterior, la aplicación recupera la lista de proyectos en la cuenta especificada del sitio de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="7b71f-231">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="7b71f-232">ProjectContext se especifica para los proyectos de la lista.</span><span class="sxs-lookup"><span data-stu-id="7b71f-232">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="7b71f-233">Especifique el elemento para recuperar.</span><span class="sxs-lookup"><span data-stu-id="7b71f-233">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="7b71f-234">Indicando solamente la colección, el servidor recupera la colección de proyectos, rellenando cada proyecto con los valores para el conjunto de propiedades predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-234">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="7b71f-235">El acceso a las propiedades que forman parte del conjunto de propiedades predeterminado ofrece resultados correctos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-235">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="7b71f-236">El acceso a las propiedades que no forman parte del conjunto predeterminado genera una excepción "No inicializado".</span><span class="sxs-lookup"><span data-stu-id="7b71f-236">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="7b71f-237">Cargue la solicitud (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="7b71f-237">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="7b71f-238">Esto forma parte del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-238">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="7b71f-239">Ejecute la consulta (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="7b71f-239">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="7b71f-240">Recuperar información de alto nivel del proyecto</span><span class="sxs-lookup"><span data-stu-id="7b71f-240">Retrieve high-level project information</span></span>

<span data-ttu-id="7b71f-241">Las propiedades que no son predeterminadas deben especificarse en la solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="7b71f-241">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="7b71f-242">El siguiente fragmento de código carga el contexto de la colección de proyectos como en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-242">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="7b71f-243">A continuación, la especificación solicita propiedades no predeterminadas adicionales para incluir en el resultado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-243">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="7b71f-244">La instrucción de carga especifica el contexto de la colección de proyectos y agrega StartDate, Phase y Stage al resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7b71f-244">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="7b71f-245">Las propiedades adicionales pueden ser escalares, objetos o colecciones.</span><span class="sxs-lookup"><span data-stu-id="7b71f-245">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="7b71f-246">Los elementos escalares se pueden acceder directamente.</span><span class="sxs-lookup"><span data-stu-id="7b71f-246">Scalar items can be accessed directly.</span></span> <span data-ttu-id="7b71f-247">Los objetos y las colecciones requieren procesamiento adicional, como en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="7b71f-247">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="7b71f-248">Resultado de los primeros tres proyectos:</span><span class="sxs-lookup"><span data-stu-id="7b71f-248">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="7b71f-249">Recuperar todas las tareas en un proyecto</span><span class="sxs-lookup"><span data-stu-id="7b71f-249">Retrieve all tasks in a project</span></span>

<span data-ttu-id="7b71f-250">Cada proyecto tiene muchas tareas.</span><span class="sxs-lookup"><span data-stu-id="7b71f-250">Each project has many tasks.</span></span> <span data-ttu-id="7b71f-251">Por lo tanto, la obtención de tareas para un solo proyecto consiste en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7b71f-251">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="7b71f-252">Establezca el contexto de la colección de proyectos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-252">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="7b71f-253">Recupere la información del proyecto, incluidas las propiedades de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7b71f-253">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="7b71f-254">Tenga en cuenta que la aplicación está solucionando proyectos publicados.</span><span class="sxs-lookup"><span data-stu-id="7b71f-254">Note that the application is addressing published projects.</span></span> <span data-ttu-id="7b71f-255">El contexto del proyecto actual publicado es pubProj.</span><span class="sxs-lookup"><span data-stu-id="7b71f-255">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="7b71f-256">Establezca el contexto de la colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="7b71f-256">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="7b71f-257">La propiedad `pubProj.Tasks` hace referencia a las tareas del proyecto actual publicado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-257">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="7b71f-258">Cargue la especificación para recuperar la colección de tareas, incluidas las propiedades no predeterminadas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7b71f-258">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="7b71f-259">Ejecute la consulta para recuperar la colección de tareas con las propiedades adecuadas.</span><span class="sxs-lookup"><span data-stu-id="7b71f-259">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="7b71f-260">La información ahora es local.</span><span class="sxs-lookup"><span data-stu-id="7b71f-260">The information is now local.</span></span> <span data-ttu-id="7b71f-261">El siguiente fragmento de código procesa la colección de tareas publicadas escribiendo la información en la consola.</span><span class="sxs-lookup"><span data-stu-id="7b71f-261">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="7b71f-262">Resultado de tareas para un proyecto:</span><span class="sxs-lookup"><span data-stu-id="7b71f-262">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="7b71f-263">Información de acceso en varios niveles</span><span class="sxs-lookup"><span data-stu-id="7b71f-263">Access information at multiple levels</span></span>

<span data-ttu-id="7b71f-264">Cada tarea puede tener una o varias personas (también llamado</span><span class="sxs-lookup"><span data-stu-id="7b71f-264">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="7b71f-265">recurso) que contribuyen hacia su finalización.</span><span class="sxs-lookup"><span data-stu-id="7b71f-265">resource) contributing toward its completion.</span></span> <span data-ttu-id="7b71f-266">Las colecciones de asignaciones y recursos contienen esta información para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="7b71f-266">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="7b71f-267">El procesamiento consiste en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7b71f-267">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="7b71f-268">Obtener un contexto para la tarea del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-268">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="7b71f-269">Crear una solicitud y cargar la solicitud para las asignaciones vinculadas a la tarea.</span><span class="sxs-lookup"><span data-stu-id="7b71f-269">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="7b71f-270">Ejecutar la consulta para las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="7b71f-270">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="7b71f-271">Crear una solicitud y cargar la solicitud para el recurso asociado a una asignación individual.</span><span class="sxs-lookup"><span data-stu-id="7b71f-271">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="7b71f-272">Ejecutar la consulta para el recurso.</span><span class="sxs-lookup"><span data-stu-id="7b71f-272">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="7b71f-273">La colección de asignaciones se solicita explícitamente en la información del servidor porque no es una propiedad predeterminada de la colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="7b71f-273">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="7b71f-274">Como colección, se realiza una consulta siguiente para obtener la colección desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="7b71f-274">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="7b71f-275">El recurso es un objeto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-275">The Resource is an object.</span></span> <span data-ttu-id="7b71f-276">La consulta para una asignación incluye el nombre del recurso asociado a la asignación.</span><span class="sxs-lookup"><span data-stu-id="7b71f-276">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="7b71f-277">Resultado de las tareas 52, 75 y 76 de un proyecto:</span><span class="sxs-lookup"><span data-stu-id="7b71f-277">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="7b71f-278">Acceso a campos personalizados de nivel empresarial</span><span class="sxs-lookup"><span data-stu-id="7b71f-278">Access custom enterprise-level fields</span></span>

<span data-ttu-id="7b71f-279">Existen campos personalizados para Project Online.</span><span class="sxs-lookup"><span data-stu-id="7b71f-279">Custom fields exist for Project Online.</span></span> <span data-ttu-id="7b71f-280">Se trata de campos de nivel empresarial que pueden estar asociados con el proyecto individual.</span><span class="sxs-lookup"><span data-stu-id="7b71f-280">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="7b71f-281">En esta sección se describe cómo obtener acceso a estos campos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-281">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="7b71f-282">Los campos personalizados no se incluyen en el conjunto predeterminado de propiedades asociadas con un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7b71f-282">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="7b71f-283">Por lo tanto, necesitan una identificación explícita en la especificación de recuperación.</span><span class="sxs-lookup"><span data-stu-id="7b71f-283">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="7b71f-284">La vista de alto nivel del proceso consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7b71f-284">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="7b71f-285">Túnel para el campo personalizado con su nombre común.</span><span class="sxs-lookup"><span data-stu-id="7b71f-285">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="7b71f-286">Recuperar el nombre interno del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-286">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="7b71f-287">Volver al contexto global y consultar el sistema con el nombre interno del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-287">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="7b71f-288">Túnel para el campo personalizado, recuperar su nombre interno y usarlo para consultar el sistema</span><span class="sxs-lookup"><span data-stu-id="7b71f-288">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="7b71f-289">Esta tarea especifica una recuperación que usa una propiedad no predeterminada con un detalle agregado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-289">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="7b71f-290">Empiece usando el contexto de proyectos, tal como se describe al principio de este artículo.</span><span class="sxs-lookup"><span data-stu-id="7b71f-290">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="7b71f-291">Agregue dos elementos a la solicitud de recuperación de colección de proyectos, además de otras propiedades no predeterminadas para recuperar:</span><span class="sxs-lookup"><span data-stu-id="7b71f-291">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="7b71f-292">La cláusula `p => p.IncludeCustomFields` identifica la necesidad de usar un objeto de proyecto que admita campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7b71f-292">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="7b71f-293">La cláusula `p => p.IncludeCustomFields.CustomFields` solicita la inclusión de datos de campos personalizados en el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7b71f-293">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="7b71f-294">Esta información se usa después de que se recupera el nombre interno del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-294">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="7b71f-295">Cargue la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b71f-295">Load the request.</span></span>
    
   <span data-ttu-id="7b71f-296">Esto forma parte del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="7b71f-296">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="7b71f-297">Ejecute la consulta.</span><span class="sxs-lookup"><span data-stu-id="7b71f-297">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="7b71f-298">Con esta información en el cliente, cree una solicitud para recuperar los campos personalizados asociados al proyecto actual.</span><span class="sxs-lookup"><span data-stu-id="7b71f-298">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="7b71f-299">Busque el campo personalizado correspondiente y recupere el nombre interno del campo.</span><span class="sxs-lookup"><span data-stu-id="7b71f-299">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="7b71f-300">El nombre interno del campo personalizado se recupera.</span><span class="sxs-lookup"><span data-stu-id="7b71f-300">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="7b71f-301">Los elementos de alto nivel 1 y 2 ahora están completos.</span><span class="sxs-lookup"><span data-stu-id="7b71f-301">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="7b71f-302">Vuelva al contexto del proyecto y recupere el valor del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-302">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="7b71f-303">El valor del campo personalizado se recupera con el nombre interno como un índice.</span><span class="sxs-lookup"><span data-stu-id="7b71f-303">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="7b71f-304">Resultado de tres proyectos que consisten en id. de proyecto, nombre del proyecto, nombre del campo personalizado, nombre interno del campo personalizado y valor del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b71f-304">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="7b71f-305">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b71f-305">See also</span></span>

<span data-ttu-id="7b71f-306">Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal de desarrollo de Project](https://developer.microsoft.com/project) en el Centro para desarrolladores de Office.</span><span class="sxs-lookup"><span data-stu-id="7b71f-306">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/project).</span></span>
    

