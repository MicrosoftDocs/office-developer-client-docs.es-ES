---
title: Desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: En este artículo se describe el desarrollo de aplicaciones Microsoft Project Online para aplicaciones de escritorio con .NET Framework 4.0. La aplicación que se describen en este artículo, recupera información desde el servidor de hospedaje.
ms.openlocfilehash: b6e7260fd2337d2b156f97605fdd201f5e0d4edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385266"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="864f1-104">Desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente</span><span class="sxs-lookup"><span data-stu-id="864f1-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="864f1-105">En este artículo se describe el desarrollo de aplicaciones Microsoft Project Online para aplicaciones de escritorio con .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="864f1-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="864f1-106">La aplicación que se describen en este artículo, recupera información desde el servidor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="864f1-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="864f1-107">Fondo</span><span class="sxs-lookup"><span data-stu-id="864f1-107">Background</span></span>

<span data-ttu-id="864f1-108">Microsoft Project inicia como aplicación de escritorio de principios de los 90.</span><span class="sxs-lookup"><span data-stu-id="864f1-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="864f1-109">En la actualidad, Project es mucho más, como sus diversas variedades confirmar:</span><span class="sxs-lookup"><span data-stu-id="864f1-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="864f1-110">Project standard edition es una aplicación de escritorio que se ejecuta como una aplicación independiente.</span><span class="sxs-lookup"><span data-stu-id="864f1-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="864f1-111">Professional, edición de proyecto es una aplicación de escritorio que puede interactuar y compartir datos con un servidor en una escala mayor, así como realizar la funcionalidad de edición estándar de Project.</span><span class="sxs-lookup"><span data-stu-id="864f1-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="864f1-112">Project Online es un servicio hospedado por Microsoft que proporciona a las empresas con una solución de nivel de PMO para coordinar y administrar proyectos, programas y carteras de proyectos.</span><span class="sxs-lookup"><span data-stu-id="864f1-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="864f1-113">Una oferta de diferente que las ediciones de escritorio, Project Online puede mantener y realizar un seguimiento de los detalles del proyecto a lo largo de la vida de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="864f1-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="864f1-114">Project Server es un servicio hospedado de empresa en la que la empresa administra y protege el servidor que contiene información de la cartera de proyectos, programa y proyecto.</span><span class="sxs-lookup"><span data-stu-id="864f1-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="864f1-115">Project Server, debe proteger el servidor interno, ofrece el proyecto, programa y las características de cartera de proyectos orientados a de hospedado externamente Project Online con una mayor capacidad de personalización.</span><span class="sxs-lookup"><span data-stu-id="864f1-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="864f1-116">Project Online tiene tres conjuntos de API en línea: modelo de objetos de cliente (COM), modelo de objetos de JavaScript (JSOM) y Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="864f1-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="864f1-117">La implementación de CSOM de .NET es la interfaz preferida al desarrollar aplicaciones de Windows que interactúan con los inquilinos de Project Online.</span><span class="sxs-lookup"><span data-stu-id="864f1-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="864f1-118">Los entornos típicos para aplicaciones centradas en el usuario incluyen los escritorios de Windows y dispositivos de Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="864f1-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="864f1-119">Aplicaciones de back-end escritas con CSOM de .NET pueden conectarse a otros servidores para los orígenes de datos y lógica empresarial que son externos a Project Online.</span><span class="sxs-lookup"><span data-stu-id="864f1-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="864f1-120">Las solicitudes de recuperación para Project Online use un sistema de consulta similar a LINQ que ofrece varias mejoras sobre las funciones de recuperación básica.</span><span class="sxs-lookup"><span data-stu-id="864f1-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="864f1-121">La interfaz de modelo de objetos de JavaScript (JSOM) proporciona compatibilidad entre exploradores para Project Online Add-ins. Un complemento es una aplicación web que se almacena en el inquilino Project Online.</span><span class="sxs-lookup"><span data-stu-id="864f1-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="864f1-122">Cuando un usuario desea ejecutar un complemento, el código para el complemento se descarga y se ejecuta en el explorador en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="864f1-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="864f1-123">El modelo de REST/Odata proporciona comunicación basadas en HTTP, se recomienda esta interfaz para aplicaciones en entornos que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="864f1-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="864f1-124">Los extremos de comunicación son los objetos en el sitio de Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="864f1-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="864f1-125">Los resultados proporcionan códigos de estado HTTP normales.</span><span class="sxs-lookup"><span data-stu-id="864f1-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="864f1-126">En este artículo se centra en una aplicación que usa la interfaz de .NET CSOM.</span><span class="sxs-lookup"><span data-stu-id="864f1-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="864f1-127">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="864f1-127">Prerequisites</span></span>

<span data-ttu-id="864f1-128">Empezar con una base del sistema que ejecuta Windows 10 y agregue los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="864f1-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="864f1-129">.NET framework 4.0 o posterior--usar el marco de trabajo completo.</span><span class="sxs-lookup"><span data-stu-id="864f1-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="864f1-130">El sitio de descarga es https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="864f1-130">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="864f1-131">Visual Studio 2013 o posterior--cualquier edición es aceptable.</span><span class="sxs-lookup"><span data-stu-id="864f1-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="864f1-132">Se usó la edición de la Comunidad de 2015 de Visual Studio para desarrollar la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="864f1-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="864f1-133">La edición de la Comunidad está disponible en https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="864f1-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="864f1-134">Componentes de cliente de SharePoint SDK--Project Online y Project Server coloca encima de SharePoint y SharePoint ensamblados.</span><span class="sxs-lookup"><span data-stu-id="864f1-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="864f1-135">Los componentes de cliente de SharePoint se incluyen en las ediciones de Visual Studio Professional y Enterprise.</span><span class="sxs-lookup"><span data-stu-id="864f1-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="864f1-136">Si utiliza la edición de la Comunidad de Visual Studio, la versión más reciente del SDK de herramientas para desarrolladores de Office está disponible en el siguiente sitio: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="864f1-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="864f1-137">Una cuenta de Project Online--Esto proporciona acceso al sitio de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="864f1-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="864f1-138">Para obtener más información acerca de cómo obtener una cuenta de Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="864f1-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="864f1-139">Proyectos en el sitio de hospedaje que se rellenan con información</span><span class="sxs-lookup"><span data-stu-id="864f1-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="864f1-140">El estándar de .NET Framework (4.0 o posterior) es el marco de trabajo correcto para usar.</span><span class="sxs-lookup"><span data-stu-id="864f1-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="864f1-141">No use el perfil de cliente de .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="864f1-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="864f1-142">Desarrollar la aplicación</span><span class="sxs-lookup"><span data-stu-id="864f1-142">Develop the application</span></span>

<span data-ttu-id="864f1-143">En el desarrollo de una aplicación de escritorio para SharePoint, la interfaz preferida es el modelo de objetos del lado de cliente de Project (COM).</span><span class="sxs-lookup"><span data-stu-id="864f1-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="864f1-144">Puede descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="864f1-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="864f1-145">Los dos primeros temas tratan problemas básicos: creación de un proyecto de Visual Studio con ensamblados y espacios de nombres adecuados y obtener acceso al servidor de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="864f1-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="864f1-146">Los temas restantes abordar los problemas con la recuperación de información a través de CSOM, de uno y varios objetos.</span><span class="sxs-lookup"><span data-stu-id="864f1-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="864f1-147">Recuperar información desde el host es un proceso de dos acción desde aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="864f1-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="864f1-148">En primer lugar, la aplicación especifica y envía una o varias de las solicitudes de recuperación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="864f1-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="864f1-149">En segundo lugar, la aplicación emite una notificación al servidor para ejecutar las consultas enviadas.</span><span class="sxs-lookup"><span data-stu-id="864f1-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="864f1-150">El servidor responde con el envío de los resultados de consulta al cliente.</span><span class="sxs-lookup"><span data-stu-id="864f1-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="864f1-151">Configurar el proyecto de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="864f1-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="864f1-152">El programa de instalación de la aplicación consiste en crear un nuevo proyecto, vinculación los ensamblados correspondientes y declarar los espacios de nombres necesarios.</span><span class="sxs-lookup"><span data-stu-id="864f1-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="864f1-153">Visual Studio presenta varios tipos de proyectos de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="864f1-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="864f1-154">Seleccione un proyecto de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="864f1-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="864f1-155">Inicie Visual Studio y seleccione **Iniciar un nuevo proyecto** en la página de inicio.</span><span class="sxs-lookup"><span data-stu-id="864f1-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="864f1-156">El cuadro de diálogo nuevo proyecto muestra plantillas de aplicación disponibles y los campos de datos para cualquier plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="864f1-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="864f1-157">Para esta aplicación, especifique los elementos siguientes.</span><span class="sxs-lookup"><span data-stu-id="864f1-157">For this application, specify the following items.</span></span> <span data-ttu-id="864f1-158">Palabras clave que se encuentra en la pantalla tienen un atributo negrita:</span><span class="sxs-lookup"><span data-stu-id="864f1-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="864f1-159">En las plantillas instaladas en el panel izquierdo, seleccione **C#** => **Windows** => **escritorio clásico**.</span><span class="sxs-lookup"><span data-stu-id="864f1-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="864f1-160">En la parte superior del panel central, seleccione **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="864f1-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="864f1-161">En los tipos de aplicación en el panel central, seleccione **Aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="864f1-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="864f1-162">En la sección inferior, especifique un nombre y una ubicación para el proyecto y un nombre de la solución.</span><span class="sxs-lookup"><span data-stu-id="864f1-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="864f1-163">También en la sección inferior, active la casilla **Crear directorio para la solución** .</span><span class="sxs-lookup"><span data-stu-id="864f1-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="864f1-164">Haga clic en **Aceptar** para crear el proyecto inicial.</span><span class="sxs-lookup"><span data-stu-id="864f1-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="864f1-165">Agregar ensamblados</span><span class="sxs-lookup"><span data-stu-id="864f1-165">Add assemblies</span></span>

<span data-ttu-id="864f1-166">La solución de VS necesita el ensamblado ProjectServerClient desde Project 2103 SDK, un par de ensamblados desde el SDK de SharePoint y el ensamblado de .NET Framework System.Security.</span><span class="sxs-lookup"><span data-stu-id="864f1-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="864f1-167">En el Explorador de soluciones frente a, haga clic en la entrada de referencias y seleccione **Agregar referencia**</span><span class="sxs-lookup"><span data-stu-id="864f1-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="864f1-168">en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="864f1-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="864f1-169">Comprobar la **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="864f1-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="864f1-170">Si es necesario, haga clic en **Examinar...**</span><span class="sxs-lookup"><span data-stu-id="864f1-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="864f1-171">botón en la parte inferior del cuadro de diálogo y navegue hasta el directorio de instalación de SDK de Project 2013 para buscar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="864f1-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="864f1-172">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="864f1-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="864f1-173">Agregue el espacio de nombres de cliente de PrjoctServer al archivo. cs.</span><span class="sxs-lookup"><span data-stu-id="864f1-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="864f1-174">Agregue los ensamblados SDK de SharePoint 2013 mediante la consola de administrador de paquetes de NuGet.</span><span class="sxs-lookup"><span data-stu-id="864f1-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="864f1-175">En el menú Herramientas de VS, haga clic en los menús siguientes: **herramientas =\> Administrador de paquetes de NuGet =\> consola de administrador de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="864f1-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="864f1-176">En la consola de administrador de paquetes, escriba el siguiente comando y presione \<ENTRAR\>:</span><span class="sxs-lookup"><span data-stu-id="864f1-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="864f1-177">La **Consola de administrador de paquetes** proporciona una descripción de los resultados del comando; y, en el Explorador de soluciones de VS muestra los ensamblados de SharePoint en las referencias del proyecto.</span><span class="sxs-lookup"><span data-stu-id="864f1-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="864f1-178">Agregue los espacios de nombres en el archivo .cs:</span><span class="sxs-lookup"><span data-stu-id="864f1-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="864f1-179">El ensamblado System.Security forma parte de .NET Framework y se ha instalado con el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="864f1-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="864f1-180">La aplicación de ejemplo, necesita un espacio de nombres más que proporciona una cadena cifrada para el sistema de hospedaje para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="864f1-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="864f1-181">Una vez autenticado, la aplicación puede tener acceso a los proyectos en el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="864f1-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="864f1-182">Agregue el espacio de nombres System.Security al archivo .cs de esta manera:</span><span class="sxs-lookup"><span data-stu-id="864f1-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="864f1-183">En el Explorador de soluciones frente a, haga clic en la entrada de referencias y seleccione **Agregar referencia**</span><span class="sxs-lookup"><span data-stu-id="864f1-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="864f1-184">en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="864f1-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="864f1-185">Seleccione **ensamblados =\> Framework** en el panel izquierdo del cuadro de diálogo Administrador de referencias, a continuación, comprobar **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="864f1-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="864f1-186">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="864f1-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="864f1-187">Agregue el espacio de nombres System.Security al archivo .cs:</span><span class="sxs-lookup"><span data-stu-id="864f1-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="864f1-188">El inicio del archivo .cs debe contener los espacios de nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="864f1-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="864f1-189">Sistema</span><span class="sxs-lookup"><span data-stu-id="864f1-189">System</span></span>
    
- <span data-ttu-id="864f1-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="864f1-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="864f1-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="864f1-191">System.Linq</span></span>
    
- <span data-ttu-id="864f1-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="864f1-192">System.Test</span></span>
    
- <span data-ttu-id="864f1-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="864f1-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="864f1-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="864f1-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="864f1-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="864f1-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="864f1-196">Conectarse al sistema de host</span><span class="sxs-lookup"><span data-stu-id="864f1-196">Connect to the host system</span></span>

<span data-ttu-id="864f1-197">Project Online es una aplicación de SharePoint, por lo que usa la autenticación de SharePoint es el enfoque correcto.</span><span class="sxs-lookup"><span data-stu-id="864f1-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="864f1-198">El siguiente fragmento de código se prepara para tener acceso a un entorno hospedado.</span><span class="sxs-lookup"><span data-stu-id="864f1-198">The following code fragment prepares to access the hosted environment.</span></span>
  
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

<span data-ttu-id="864f1-199">Preparativos para tener acceso a un entorno hospedado incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="864f1-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="864f1-200">Crear un objeto de contexto para los proyectos: Esto se encuentra en el siguiente código del fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="864f1-201">El contexto es heredado por otros componentes, lo que permite el sistema administrar el contexto del modelo de objetos de Project.</span><span class="sxs-lookup"><span data-stu-id="864f1-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="864f1-202">Identificar el sitio host: Esto se hace en el siguiente código desde el fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="864f1-203">Al crear una instancia del contexto de proyectos, la aplicación debe proporcionar la raíz de la colección de sitios de proyectos.</span><span class="sxs-lookup"><span data-stu-id="864f1-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="864f1-204">La aplicación usa una subcadena de la dirección URL de la raíz de los proyectos.</span><span class="sxs-lookup"><span data-stu-id="864f1-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="864f1-205">Una instantánea de esta ubicación se resalta con un rectángulo rojo en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="864f1-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="864f1-206">La autenticación necesita la cadena desde su inicio a través de la subcadena "pwa".</span><span class="sxs-lookup"><span data-stu-id="864f1-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="864f1-207">En el listado de código, la aplicación utiliza la cadena "https://XXXXXXXX.sharepoint.com/sites/pwa".</span><span class="sxs-lookup"><span data-stu-id="864f1-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="864f1-208">![Captura de pantalla de la dirección URL de la colección de sitios de proyectos dentro de un borde rojo.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Captura de pantalla de la dirección URL de los proyectos colección dentro de un borde rojo de sitios")</span><span class="sxs-lookup"><span data-stu-id="864f1-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="864f1-209">Colocar la contraseña en una cadena segura: Esto se hace en el siguiente código desde el fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="864f1-210">La cuenta de usuario y contraseña son las credenciales para tener acceso al sitio host.</span><span class="sxs-lookup"><span data-stu-id="864f1-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="864f1-211">Agregue la cuenta de usuario y la contraseña a la parte de las credenciales del objeto context: Esto se hace en el siguiente código desde el fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="864f1-212">El contexto del proyecto instancias está listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="864f1-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="864f1-213">Lista de proyectos publicados todo</span><span class="sxs-lookup"><span data-stu-id="864f1-213">List all published projects</span></span>

<span data-ttu-id="864f1-214">Project Online y ProjectServer usan a servidores proxy para comunicarse con el servidor para crear, informe, actualizar y eliminación operaciones (CRUD).</span><span class="sxs-lookup"><span data-stu-id="864f1-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="864f1-215">El servidor de host controla las solicitudes de una manera eficaz y tiene el cliente de realizar las siguientes acciones en la comunicación con el servidor:</span><span class="sxs-lookup"><span data-stu-id="864f1-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="864f1-216">Establecer un contexto para la comunicación.</span><span class="sxs-lookup"><span data-stu-id="864f1-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="864f1-217">El contexto se usa en la colección de proyectos, así como otros objetos y colecciones a través de herencia, incluida la colección tasks, colección de asignaciones, el objeto stage y campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="864f1-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="864f1-218">Use el modelo de objetos para especificar un objeto, colección o datos que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="864f1-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="864f1-219">Este paso usa LINQ como una consulta o como un método.</span><span class="sxs-lookup"><span data-stu-id="864f1-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="864f1-220">La especificación controla lo que reciba.</span><span class="sxs-lookup"><span data-stu-id="864f1-220">The specification controls what you receive.</span></span> <span data-ttu-id="864f1-221">A menudo, este paso se incrusta como el cuerpo del método Load (paso 3).</span><span class="sxs-lookup"><span data-stu-id="864f1-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="864f1-222">Cargar la especificación de recuperación desde el paso anterior con el método Load() o LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="864f1-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="864f1-223">Para cargar objetos y colecciones, use Load().</span><span class="sxs-lookup"><span data-stu-id="864f1-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="864f1-224">Para las consultas con cláusulas como "where" y "grupo", use LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="864f1-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="864f1-225">Ejecutar la solicitud mediante el método ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="864f1-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="864f1-226">El método ExecuteQuery() notifica al host que la consulta o consultas están listos para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="864f1-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="864f1-227">Una vez que el host recibe la notificación, ejecuta las consultas y envía los resultados al cliente.</span><span class="sxs-lookup"><span data-stu-id="864f1-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="864f1-228">Con la información en el cliente, la aplicación puede usarla.</span><span class="sxs-lookup"><span data-stu-id="864f1-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="864f1-229">El siguiente fragmento de código recorre en iteración los proyectos publicados e imprime el identificador y el nombre para cada proyecto publicado en el host.</span><span class="sxs-lookup"><span data-stu-id="864f1-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
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

<span data-ttu-id="864f1-230">Salida:</span><span class="sxs-lookup"><span data-stu-id="864f1-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="864f1-231">Realizar una solicitud</span><span class="sxs-lookup"><span data-stu-id="864f1-231">Make a request</span></span>

<span data-ttu-id="864f1-232">Uso de las acciones desde el fragmento de código anterior, la aplicación recupera la lista de proyectos en la cuenta especificada en el sitio de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="864f1-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="864f1-233">El ProjectContext especificado para que los proyectos para obtener una lista.</span><span class="sxs-lookup"><span data-stu-id="864f1-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="864f1-234">Especificar el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="864f1-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="864f1-235">Sólo que indica la colección, el servidor recupera la colección de proyectos, rellenar cada proyecto con los valores para el conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="864f1-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="864f1-236">Obtener acceso a las propiedades que forman parte del conjunto de propiedades predeterminado proporciona buenos resultados.</span><span class="sxs-lookup"><span data-stu-id="864f1-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="864f1-237">Obtener acceso a las propiedades que no forman parte de la predeterminada establecer los resultados de una excepción "No inicializado".</span><span class="sxs-lookup"><span data-stu-id="864f1-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="864f1-238">Carga de la solicitud (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="864f1-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="864f1-239">Esto es parte del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="864f1-240">Ejecutar la consulta (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="864f1-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="864f1-241">Recuperar información de alto nivel del proyecto</span><span class="sxs-lookup"><span data-stu-id="864f1-241">Retrieve high-level project information</span></span>

<span data-ttu-id="864f1-242">Propiedades que no son propiedades predeterminadas deben especificarse en la solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="864f1-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="864f1-243">El siguiente fragmento de código carga el contexto de la colección de proyectos como en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="864f1-244">A continuación, la especificación solicita propiedades no predeterminados adicionales para incluir en el resultado.</span><span class="sxs-lookup"><span data-stu-id="864f1-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="864f1-245">La instrucción load especifica el contexto de la colección de proyectos y agrega la StartDate, fase y región para el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="864f1-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="864f1-246">Las propiedades adicionales que pueden ser escalares, objetos o colecciones.</span><span class="sxs-lookup"><span data-stu-id="864f1-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="864f1-247">Elementos escalares pueden tener acceso directamente.</span><span class="sxs-lookup"><span data-stu-id="864f1-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="864f1-248">Objetos y colecciones requieren un procesamiento adicional, como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="864f1-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
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

<span data-ttu-id="864f1-249">Salida de los tres primeros proyectos:</span><span class="sxs-lookup"><span data-stu-id="864f1-249">Output of the first three projects:</span></span>
  
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

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="864f1-250">Recuperar todas las tareas en un proyecto</span><span class="sxs-lookup"><span data-stu-id="864f1-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="864f1-251">Cada proyecto tiene muchas de las tareas.</span><span class="sxs-lookup"><span data-stu-id="864f1-251">Each project has many tasks.</span></span> <span data-ttu-id="864f1-252">Por lo tanto, la inclusión de las tareas de un único proyecto consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="864f1-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="864f1-253">Establecer el contexto de la colección de proyectos.</span><span class="sxs-lookup"><span data-stu-id="864f1-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="864f1-254">Recuperar la información del proyecto, incluidas las propiedades de la tarea.</span><span class="sxs-lookup"><span data-stu-id="864f1-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="864f1-255">Tenga en cuenta que la aplicación es hacer frente a los proyectos publicados.</span><span class="sxs-lookup"><span data-stu-id="864f1-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="864f1-256">El contexto para el proyecto publicado actual es pubProj.</span><span class="sxs-lookup"><span data-stu-id="864f1-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="864f1-257">Establecer el contexto de la colección Tasks.</span><span class="sxs-lookup"><span data-stu-id="864f1-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="864f1-258">El `pubProj.Tasks` (propiedad) hace referencia a las tareas del proyecto publicado actual.</span><span class="sxs-lookup"><span data-stu-id="864f1-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="864f1-259">Carga de la especificación para recuperar la colección de tareas, incluidas las propiedades que no sean predeterminados adecuadas.</span><span class="sxs-lookup"><span data-stu-id="864f1-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="864f1-260">Ejecutar la consulta para recuperar la colección de tareas con las propiedades adecuadas.</span><span class="sxs-lookup"><span data-stu-id="864f1-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="864f1-261">La información ahora es local.</span><span class="sxs-lookup"><span data-stu-id="864f1-261">The information is now local.</span></span> <span data-ttu-id="864f1-262">El siguiente fragmento de código procesa la colección tasks publicados mediante la escritura de la información en la consola.</span><span class="sxs-lookup"><span data-stu-id="864f1-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
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

<span data-ttu-id="864f1-263">Salida de tareas para un proyecto:</span><span class="sxs-lookup"><span data-stu-id="864f1-263">Output of tasks for one project:</span></span>
  
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

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="864f1-264">Información de acceso en varios niveles</span><span class="sxs-lookup"><span data-stu-id="864f1-264">Access information at multiple levels</span></span>

<span data-ttu-id="864f1-265">Cada tarea puede tener una o más personas (también conocido como</span><span class="sxs-lookup"><span data-stu-id="864f1-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="864f1-266">recursos) contribuya a su finalización.</span><span class="sxs-lookup"><span data-stu-id="864f1-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="864f1-267">Las colecciones de asignaciones y recursos que contienen esta información para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="864f1-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="864f1-268">El procesamiento consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="864f1-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="864f1-269">Obtención de un contexto para la tarea del proyecto.</span><span class="sxs-lookup"><span data-stu-id="864f1-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="864f1-270">Generar una solicitud y cargar la solicitud para las asignaciones de vinculadas a la tarea.</span><span class="sxs-lookup"><span data-stu-id="864f1-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="864f1-271">Ejecutar la consulta para las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="864f1-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="864f1-272">Generar una solicitud y cargar la solicitud para el recurso asociado a una asignación individual.</span><span class="sxs-lookup"><span data-stu-id="864f1-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="864f1-273">Ejecutar la consulta para el recurso.</span><span class="sxs-lookup"><span data-stu-id="864f1-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="864f1-274">La colección de asignaciones se solicita explícitamente en la información desde el servidor porque no es una propiedad predeterminada de la colección Tasks.</span><span class="sxs-lookup"><span data-stu-id="864f1-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="864f1-275">Como una colección, se realiza una consulta subsiguiente se van a extraer la colección desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="864f1-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="864f1-276">El recurso es un objeto.</span><span class="sxs-lookup"><span data-stu-id="864f1-276">The Resource is an object.</span></span> <span data-ttu-id="864f1-277">La consulta para una asignación incluye el nombre de recurso asociado con la asignación.</span><span class="sxs-lookup"><span data-stu-id="864f1-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
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

<span data-ttu-id="864f1-278">Salida para tareas 52, 75 y 76 de un proyecto:</span><span class="sxs-lookup"><span data-stu-id="864f1-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
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

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="864f1-279">Campos personalizados de empresa-nivel de acceso</span><span class="sxs-lookup"><span data-stu-id="864f1-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="864f1-280">Existen campos personalizados para Project Online.</span><span class="sxs-lookup"><span data-stu-id="864f1-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="864f1-281">Estos son los campos de nivel de empresa que se pueden asociados a un proyecto individual.</span><span class="sxs-lookup"><span data-stu-id="864f1-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="864f1-282">En esta sección se describe cómo tener acceso a estos campos.</span><span class="sxs-lookup"><span data-stu-id="864f1-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="864f1-283">Los campos personalizados no se incluyen en el conjunto predeterminado de propiedades asociadas con un proyecto.</span><span class="sxs-lookup"><span data-stu-id="864f1-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="864f1-284">Por lo tanto, necesitan identificación explícita en la especificación de recuperación.</span><span class="sxs-lookup"><span data-stu-id="864f1-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="864f1-285">La vista de alto nivel del proceso consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="864f1-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="864f1-286">Túnel para el campo personalizado mediante su nombre común.</span><span class="sxs-lookup"><span data-stu-id="864f1-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="864f1-287">Recuperar el nombre interno del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="864f1-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="864f1-288">Vuelva al contexto global y el sistema con el nombre interno del campo personalizado de consulta.</span><span class="sxs-lookup"><span data-stu-id="864f1-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="864f1-289">Túnel para el campo personalizado, recuperar su nombre interno y utiliza para consultar el sistema</span><span class="sxs-lookup"><span data-stu-id="864f1-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="864f1-290">Esta tarea, especifica un sistema de recuperación que utiliza una propiedad no predeterminada con un nivel de detalle se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="864f1-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="864f1-291">Para empezar, utilizando el contexto de proyectos, tal como se describe al principio de este artículo.</span><span class="sxs-lookup"><span data-stu-id="864f1-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="864f1-292">Agregue dos elementos a la solicitud de recuperación de colección de proyectos además de otras propiedades que no sean predeterminados para recuperar:</span><span class="sxs-lookup"><span data-stu-id="864f1-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="864f1-293">El `p => p.IncludeCustomFields` cláusula identifica la necesidad de usar un objeto de proyecto que es compatible con los campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="864f1-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="864f1-294">El `p => p.IncludeCustomFields.CustomFields` cláusula solicita la inclusión de datos de campo personalizado en el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="864f1-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="864f1-295">Esta información se utiliza después de recupera el nombre interno de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="864f1-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="864f1-296">La solicitud de carga.</span><span class="sxs-lookup"><span data-stu-id="864f1-296">Load the request.</span></span>
    
   <span data-ttu-id="864f1-297">Esto es parte del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="864f1-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="864f1-298">Ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="864f1-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="864f1-299">Con esta información en el cliente, crear una solicitud para recuperar los campos personalizados asociados al proyecto actual.</span><span class="sxs-lookup"><span data-stu-id="864f1-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="864f1-300">Busque la apropiada del campo personalizado y recuperar el nombre interno del campo.</span><span class="sxs-lookup"><span data-stu-id="864f1-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="864f1-301">Se recupera el nombre interno del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="864f1-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="864f1-302">Los elementos de alto nivel 1 y 2 ahora están completados.</span><span class="sxs-lookup"><span data-stu-id="864f1-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="864f1-303">Volver al contexto del proyecto y recuperar el valor del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="864f1-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="864f1-304">Se recupera el valor del campo personalizado con el nombre interno como un índice.</span><span class="sxs-lookup"><span data-stu-id="864f1-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="864f1-305">Salida de tres proyectos formado por identificador de proyecto, nombre del proyecto, nombre de campo personalizado, nombre interno de campo personalizado y valor de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="864f1-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="864f1-306">Vea también</span><span class="sxs-lookup"><span data-stu-id="864f1-306">See also</span></span>

<span data-ttu-id="864f1-307">Para obtener documentación y ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal del proyecto de desarrollo](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="864f1-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

