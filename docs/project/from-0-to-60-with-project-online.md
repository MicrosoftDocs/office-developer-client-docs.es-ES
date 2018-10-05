---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un sitio de Project Online (SharePoint hospedado), uso de aplicaciones independientes o complementos en el proyecto. Una gran cantidad de aplicaciones es posible que van desde hacer frente a las necesidades de los implicados en un proyecto a las funciones de soporte PMO, por ejemplo, cualquiera de las siguientes opciones:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392588"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="a1287-103">De 0 a 60 con Project Online</span><span class="sxs-lookup"><span data-stu-id="a1287-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="a1287-104">Un desarrollador de aplicaciones puede personalizar un sitio de Project Online (SharePoint hospedado), uso de aplicaciones independientes o complementos en el proyecto. Una gran cantidad de aplicaciones es posible que van desde hacer frente a las necesidades de los implicados en un proyecto a las funciones de soporte PMO, por ejemplo, cualquiera de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="a1287-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="a1287-105">Entrada de datos de tarjetas de horas trabajadas simplificadas para los trabajadores</span><span class="sxs-lookup"><span data-stu-id="a1287-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="a1287-106">Aprobación de tarjetas de horas trabajadas eficaz para supervisores</span><span class="sxs-lookup"><span data-stu-id="a1287-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="a1287-107">Supervisión de los permisos necesarios para un proyecto (compras y estado)</span><span class="sxs-lookup"><span data-stu-id="a1287-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="a1287-108">Comprobación de estado y mantenimiento de los proyectos activos</span><span class="sxs-lookup"><span data-stu-id="a1287-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="a1287-109">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="a1287-109">Issues report</span></span>
- <span data-ttu-id="a1287-110">Cambiar el informe de estado de administración</span><span class="sxs-lookup"><span data-stu-id="a1287-110">Change Management Status report</span></span>
    
<span data-ttu-id="a1287-111">Project Online incluye compatibilidad con la API para dar cabida a los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="a1287-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="a1287-112">Para un complemento de Project (SharePoint) hospedado:</span><span class="sxs-lookup"><span data-stu-id="a1287-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="a1287-113">Código (JavaScript, HTML, CSS) que se hospeda en SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a1287-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="a1287-114">Activos que se descarga en el explorador y se ejecutan en SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a1287-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="a1287-115">Lógica de negocios que se encuentra en JavaScript</span><span class="sxs-lookup"><span data-stu-id="a1287-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="a1287-116">Obtenga acceso a datos es en/almacena en Project Online o SharePoint como (pero no está limitado a):</span><span class="sxs-lookup"><span data-stu-id="a1287-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="a1287-117">Campos personalizados</span><span class="sxs-lookup"><span data-stu-id="a1287-117">Custom fields</span></span>  
  - <span data-ttu-id="a1287-118">Listas</span><span class="sxs-lookup"><span data-stu-id="a1287-118">Lists</span></span>
    
- <span data-ttu-id="a1287-119">Para un proyecto (SharePoint) hospedada en proveedor complemento:</span><span class="sxs-lookup"><span data-stu-id="a1287-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="a1287-120">Código que se encuentra en un sitio externo para el sitio de Project Online</span><span class="sxs-lookup"><span data-stu-id="a1287-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="a1287-121">Un sitio externo, que puede ser (pero no está limitado a):</span><span class="sxs-lookup"><span data-stu-id="a1287-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="a1287-122">Otro sitio de SharePoint</span><span class="sxs-lookup"><span data-stu-id="a1287-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="a1287-123">Servicio de la aplicaciones Web creadas en cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="a1287-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="a1287-124">El sitio externo contiene lógica empresarial</span><span class="sxs-lookup"><span data-stu-id="a1287-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="a1287-125">El explorador se redirige desde Project Online a sitios externos con tokens de acceso a Project Online</span><span class="sxs-lookup"><span data-stu-id="a1287-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="a1287-126">El sitio externo puede realizar llamadas a SharePoint y Project Online</span><span class="sxs-lookup"><span data-stu-id="a1287-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="a1287-127">Para un complemento en independiente o externo:</span><span class="sxs-lookup"><span data-stu-id="a1287-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="a1287-128">Usuario ejecuta una aplicación en su dispositivo</span><span class="sxs-lookup"><span data-stu-id="a1287-128">User executes an application on their device</span></span>
  - <span data-ttu-id="a1287-129">Aplicación autentica y llama directamente a las API de proyecto en línea</span><span class="sxs-lookup"><span data-stu-id="a1287-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="a1287-130">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="a1287-130">Type of application</span></span>|<span data-ttu-id="a1287-131">Implementación de la API</span><span class="sxs-lookup"><span data-stu-id="a1287-131">API implementation</span></span>|<span data-ttu-id="a1287-132">Entorno de destino</span><span class="sxs-lookup"><span data-stu-id="a1287-132">Target environment</span></span>|<span data-ttu-id="a1287-133">Ejemplos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a1287-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a1287-134">Proyecto hospedado</span><span class="sxs-lookup"><span data-stu-id="a1287-134">Project hosted</span></span>  <br/> |<span data-ttu-id="a1287-135">JSOM (modelo de objetos de secuencia de comandos de Java)</span><span class="sxs-lookup"><span data-stu-id="a1287-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="a1287-136">REST</span><span class="sxs-lookup"><span data-stu-id="a1287-136">REST</span></span>  <br/> |<span data-ttu-id="a1287-137">Explorador</span><span class="sxs-lookup"><span data-stu-id="a1287-137">Browser</span></span>  <br/> |<span data-ttu-id="a1287-138">Entrada de tarjetas de horas trabajadas</span><span class="sxs-lookup"><span data-stu-id="a1287-138">Timecard entry</span></span>  <br/> <span data-ttu-id="a1287-139">Aprobación de tarjetas de horas trabajadas</span><span class="sxs-lookup"><span data-stu-id="a1287-139">Timecard approval</span></span>  <br/> <span data-ttu-id="a1287-140">Estado de proyecto</span><span class="sxs-lookup"><span data-stu-id="a1287-140">Project Status</span></span>  <br/> <span data-ttu-id="a1287-141">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="a1287-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="a1287-142">Hospedada de proveedor de proyecto</span><span class="sxs-lookup"><span data-stu-id="a1287-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="a1287-143">Biblioteca de cliente de CSOM</span><span class="sxs-lookup"><span data-stu-id="a1287-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="a1287-144">Sitio Web de Azure/aplicación</span><span class="sxs-lookup"><span data-stu-id="a1287-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="a1287-145">Entorno de que no son de Windows (LAMP, etcetera).</span><span class="sxs-lookup"><span data-stu-id="a1287-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="a1287-146">Validador de partes de horas externos</span><span class="sxs-lookup"><span data-stu-id="a1287-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="a1287-147">Importador de Project</span><span class="sxs-lookup"><span data-stu-id="a1287-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="a1287-148">Independiente o externo</span><span class="sxs-lookup"><span data-stu-id="a1287-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="a1287-149">REST</span><span class="sxs-lookup"><span data-stu-id="a1287-149">REST</span></span>  <br/> <span data-ttu-id="a1287-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="a1287-150">CSOM</span></span>  <br/> |<span data-ttu-id="a1287-151">REST - cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="a1287-151">REST - any platform</span></span>  <br/> <span data-ttu-id="a1287-152">CSOM - cualquier plataforma .NET compatibles</span><span class="sxs-lookup"><span data-stu-id="a1287-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="a1287-153">Entrada de tarjetas de horas trabajadas</span><span class="sxs-lookup"><span data-stu-id="a1287-153">Timecard entry</span></span>  <br/> <span data-ttu-id="a1287-154">Migración de proyectos a un sitio nuevo</span><span class="sxs-lookup"><span data-stu-id="a1287-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="a1287-155">Cambiar el estado de la administración.</span><span class="sxs-lookup"><span data-stu-id="a1287-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="a1287-156">¿Qué necesita para comenzar a desarrollar aplicaciones para Project Online?</span><span class="sxs-lookup"><span data-stu-id="a1287-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="a1287-157">Los elementos comunes necesarios para el desarrollo de aplicaciones de Project Online son una cuenta de Project Online y probar datos--proyectos e información relacionados con los proyectos que incluyen las asignaciones, tareas, recursos y campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a1287-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="a1287-158">Un entorno de desarrollo se necesita también, pero elementos específicos del entorno de desarrollo dependen del tipo de aplicación y la interfaz de API necesarios para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1287-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="a1287-159">En las secciones siguientes se describen las necesidades de desarrollo de las tres interfaces API.</span><span class="sxs-lookup"><span data-stu-id="a1287-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="a1287-160">La documentación de referencia describe el modelo de objetos que es común para las tres interfaces, así como una asignación de entidad que se muestra las relaciones entre los componentes del modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="a1287-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="a1287-161">Entorno de desarrollo de complementos de proyecto hospedado</span><span class="sxs-lookup"><span data-stu-id="a1287-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="a1287-162">Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a1287-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="a1287-163">Complementos hospedados pueden usar las interfaces JSOM o REST y se escriben en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a1287-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="a1287-164">Project Online proporciona referencias a la biblioteca JSOM de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a1287-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="a1287-165">Desarrollo se supone que está en una plataforma de Windows, el seguimiento de los recursos necesarios:</span><span class="sxs-lookup"><span data-stu-id="a1287-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="a1287-166">Visual Studio de 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="a1287-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="a1287-167">Herramientas de desarrollo de Office para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a1287-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="a1287-168">Idioma de JavaScript</span><span class="sxs-lookup"><span data-stu-id="a1287-168">JavaScript language</span></span>
    
<span data-ttu-id="a1287-169">Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a1287-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="a1287-170">Puede descargar y ejecutar el ejemplo en unos cuantos pasos sencillos:</span><span class="sxs-lookup"><span data-stu-id="a1287-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="a1287-171">Descargue y abra la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1287-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="a1287-172">Actualice SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1287-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="a1287-173">Project Online examina del ámbito de aplicación del complemento y los permisos de usuario para controlar el acceso a la información en el host de Project Online.</span><span class="sxs-lookup"><span data-stu-id="a1287-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="a1287-174">Si el acceso se deniega explícitamente en la configuración de uno o ambos, Project Online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="a1287-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="a1287-175">De lo contrario, se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="a1287-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="a1287-176">Habilitar [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio.</span><span class="sxs-lookup"><span data-stu-id="a1287-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="a1287-177">Genere el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-177">Build the project.</span></span>
    
5. <span data-ttu-id="a1287-178">Ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="a1287-179">Entorno hospedado por el proveedor de desarrollo de complementos del proyecto</span><span class="sxs-lookup"><span data-stu-id="a1287-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="a1287-180">Complementos de proveedor hospedado son aplicaciones escritas y que residen en cualquier plataforma web.</span><span class="sxs-lookup"><span data-stu-id="a1287-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="a1287-181">Puede conectarse y realizar operaciones de datos con el resto (o CSOM para plataformas de Microsoft) API.</span><span class="sxs-lookup"><span data-stu-id="a1287-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="a1287-182">Para el desarrollo se pueden usar cualquier lenguaje y el entorno que admite la interfaz REST.</span><span class="sxs-lookup"><span data-stu-id="a1287-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="a1287-183">Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a1287-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="a1287-184">Visual Studio de 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="a1287-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="a1287-185">Herramientas de desarrollo de Microsoft Office para Visual Studio (suministrado con las ediciones de Visual Studio 2015 Professional y Enterprise)</span><span class="sxs-lookup"><span data-stu-id="a1287-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="a1287-186">.NET framework 4.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a1287-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="a1287-187">[Paquete de CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para las llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="a1287-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="a1287-188">Un lenguaje de programación, como C#</span><span class="sxs-lookup"><span data-stu-id="a1287-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="a1287-189">Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabajar scripts de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a1287-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="a1287-190">Puede ejecutar el ejemplo en unos cuantos pasos:</span><span class="sxs-lookup"><span data-stu-id="a1287-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="a1287-191">Descargue y abra la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1287-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="a1287-192">Actualice SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1287-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="a1287-193">Project Online examina del ámbito de aplicación del complemento y los permisos de usuario para controlar el acceso a la información en el host de Project Online.</span><span class="sxs-lookup"><span data-stu-id="a1287-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="a1287-194">Si el acceso se deniega explícitamente en la configuración de uno o ambos, Project Online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="a1287-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="a1287-195">De lo contrario, se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="a1287-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="a1287-196">Habilitar [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio.</span><span class="sxs-lookup"><span data-stu-id="a1287-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="a1287-197">Genere el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-197">Build the project.</span></span>
    
5. <span data-ttu-id="a1287-198">Ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="a1287-199">Entorno de desarrollo de la aplicación externa o independiente</span><span class="sxs-lookup"><span data-stu-id="a1287-199">External/standalone application development environment</span></span>

<span data-ttu-id="a1287-200">Una aplicación independiente puede llamar a Project Online mediante el modelo de objetos de lado cliente (COM) o REST para comunicarse con Project Online para crear, recuperar, actualizar y eliminar la información que reside en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a1287-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="a1287-201">Esto es una aplicación de cliente independiente que depende del nivel de acceso de usuario para que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="a1287-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="a1287-202">Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a1287-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="a1287-203">Visual Studio de 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="a1287-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="a1287-204">Herramientas de desarrollo de Microsoft Office para Visual Studio (suministrado con las ediciones de Visual Studio 2015 Professional y Enterprise)</span><span class="sxs-lookup"><span data-stu-id="a1287-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="a1287-205">.NET framework 4.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a1287-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="a1287-206">[Paquete de CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para las llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="a1287-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="a1287-207">Un lenguaje de programación, como C#</span><span class="sxs-lookup"><span data-stu-id="a1287-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="a1287-208">Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a1287-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="a1287-209">Puede ejecutar el ejemplo en unos cuantos pasos:</span><span class="sxs-lookup"><span data-stu-id="a1287-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="a1287-210">Descargar la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1287-210">Download the sample application</span></span>
    
2. <span data-ttu-id="a1287-211">Hacer un par de cambios para tener acceso a su sitio Project Online: el nombre del sitio, la cuenta de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="a1287-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="a1287-212">Asegúrese de que el usuario tiene acceso a todos los proyectos.</span><span class="sxs-lookup"><span data-stu-id="a1287-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="a1287-213">Project Online usa los permisos de usuario para controlar el acceso a la información en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="a1287-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="a1287-214">Agregue el ensamblado de SharePoint a las referencias del uso de la consola de administrador de paquetes de Nuget, disponible en el menú Herramientas escribiendo lo siguiente en la consola de Nuget:</span><span class="sxs-lookup"><span data-stu-id="a1287-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="a1287-215">Genere el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-215">Build the project.</span></span>
    
5. <span data-ttu-id="a1287-216">Ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1287-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="a1287-217">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="a1287-217">Next steps</span></span>

<span data-ttu-id="a1287-218">Cada aplicación de ejemplo tiene un artículo para explicar los aspectos de trabajar con la API de proyecto individuales.</span><span class="sxs-lookup"><span data-stu-id="a1287-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="a1287-219">Los artículos aparecen en la lista siguiente, junto con algunos artículos que describen las relaciones entre entidades, información sobre el sistema de consulta y obtener acceso a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a1287-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="a1287-220">Desarrollar una aplicación de Project Online con el modelo de objetos de cliente</span><span class="sxs-lookup"><span data-stu-id="a1287-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="a1287-221">Desarrollo de un complemento Project Online mediante el modelo de objetos de JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="a1287-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="a1287-222">Obtener acceso a campos personalizados de empresa de Project Online</span><span class="sxs-lookup"><span data-stu-id="a1287-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="a1287-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1287-223">See also</span></span>

<span data-ttu-id="a1287-224">Para obtener documentación y ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal del proyecto de desarrollo](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="a1287-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

