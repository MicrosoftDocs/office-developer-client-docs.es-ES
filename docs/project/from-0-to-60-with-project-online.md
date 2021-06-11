---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un Project Online web (SharePoint hospedado) mediante aplicaciones independientes o Project complementos. Es posible una gran cantidad de aplicaciones que van desde satisfacer las necesidades de los participantes en un proyecto hasta las funciones de soporte técnico de PMO, como cualquiera de las siguientes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344411"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="20342-103">De 0 a 60 con Project Online</span><span class="sxs-lookup"><span data-stu-id="20342-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="20342-104">Un desarrollador de aplicaciones puede personalizar un Project Online web (SharePoint hospedado) mediante aplicaciones independientes o Project complementos. Es posible una gran cantidad de aplicaciones que van desde satisfacer las necesidades de los participantes en un proyecto hasta las funciones de soporte técnico de PMO, como cualquiera de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="20342-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="20342-105">Entrada de datos de tarjeta de tiempo optimizada para los trabajadores</span><span class="sxs-lookup"><span data-stu-id="20342-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="20342-106">Aprobación eficiente de tarjetas de tiempo para supervisores</span><span class="sxs-lookup"><span data-stu-id="20342-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="20342-107">Supervisión de permisos (adquisición y estado) necesarios para un proyecto</span><span class="sxs-lookup"><span data-stu-id="20342-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="20342-108">Comprobación de estado/estado de los proyectos activos</span><span class="sxs-lookup"><span data-stu-id="20342-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="20342-109">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="20342-109">Issues report</span></span>
- <span data-ttu-id="20342-110">Informe de estado de administración de cambios</span><span class="sxs-lookup"><span data-stu-id="20342-110">Change Management Status report</span></span>
    
<span data-ttu-id="20342-111">Project Online incluye compatibilidad con api para dar cabida a los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="20342-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="20342-112">Para un complemento Project (SharePoint) hospedado:</span><span class="sxs-lookup"><span data-stu-id="20342-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="20342-113">Código (JavaScript, HTML, CSS) hospedado en SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="20342-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="20342-114">Activos que se descargan en el explorador y se ejecutan en SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="20342-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="20342-115">Lógica empresarial que está en JavaScript</span><span class="sxs-lookup"><span data-stu-id="20342-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="20342-116">Acceder a los datos que se almacenan en Project Online o SharePoint como (pero no se limita a):</span><span class="sxs-lookup"><span data-stu-id="20342-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="20342-117">Campos personalizados</span><span class="sxs-lookup"><span data-stu-id="20342-117">Custom fields</span></span>  
  - <span data-ttu-id="20342-118">Listas</span><span class="sxs-lookup"><span data-stu-id="20342-118">Lists</span></span>
    
- <span data-ttu-id="20342-119">Para un complemento Project (SharePoint) hospedado por el proveedor:</span><span class="sxs-lookup"><span data-stu-id="20342-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="20342-120">Código que existe en un sitio externo al sitio Project Online sitio</span><span class="sxs-lookup"><span data-stu-id="20342-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="20342-121">Un sitio externo, que puede ser (pero no está limitado a):</span><span class="sxs-lookup"><span data-stu-id="20342-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="20342-122">Otro SharePoint web</span><span class="sxs-lookup"><span data-stu-id="20342-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="20342-123">Aplicación web/servicio integrado en cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="20342-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="20342-124">El sitio externo contiene lógica empresarial</span><span class="sxs-lookup"><span data-stu-id="20342-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="20342-125">El explorador se redirige desde Project Online al sitio externo con tokens de acceso a Project Online</span><span class="sxs-lookup"><span data-stu-id="20342-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="20342-126">El sitio externo puede realizar llamadas a SharePoint y Project Online</span><span class="sxs-lookup"><span data-stu-id="20342-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="20342-127">Para un complemento externo/independiente:</span><span class="sxs-lookup"><span data-stu-id="20342-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="20342-128">El usuario ejecuta una aplicación en su dispositivo</span><span class="sxs-lookup"><span data-stu-id="20342-128">User executes an application on their device</span></span>
  - <span data-ttu-id="20342-129">La aplicación autentica y llama a Project Online API directamente</span><span class="sxs-lookup"><span data-stu-id="20342-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="20342-130">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="20342-130">Type of application</span></span>|<span data-ttu-id="20342-131">Implementación de API</span><span class="sxs-lookup"><span data-stu-id="20342-131">API implementation</span></span>|<span data-ttu-id="20342-132">Entorno de destino</span><span class="sxs-lookup"><span data-stu-id="20342-132">Target environment</span></span>|<span data-ttu-id="20342-133">Ejemplos de aplicación</span><span class="sxs-lookup"><span data-stu-id="20342-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20342-134">Project hospedado</span><span class="sxs-lookup"><span data-stu-id="20342-134">Project hosted</span></span>  <br/> |<span data-ttu-id="20342-135">JSOM (Java de objetos script)</span><span class="sxs-lookup"><span data-stu-id="20342-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="20342-136">REST</span><span class="sxs-lookup"><span data-stu-id="20342-136">REST</span></span>  <br/> |<span data-ttu-id="20342-137">Explorador</span><span class="sxs-lookup"><span data-stu-id="20342-137">Browser</span></span>  <br/> |<span data-ttu-id="20342-138">Entrada de tarjeta de tiempo</span><span class="sxs-lookup"><span data-stu-id="20342-138">Timecard entry</span></span>  <br/> <span data-ttu-id="20342-139">Aprobación de tarjetas de tiempo</span><span class="sxs-lookup"><span data-stu-id="20342-139">Timecard approval</span></span>  <br/> <span data-ttu-id="20342-140">Estado de proyecto</span><span class="sxs-lookup"><span data-stu-id="20342-140">Project Status</span></span>  <br/> <span data-ttu-id="20342-141">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="20342-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="20342-142">Project Proveedor hospedado</span><span class="sxs-lookup"><span data-stu-id="20342-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="20342-143">Biblioteca de cliente CSOM</span><span class="sxs-lookup"><span data-stu-id="20342-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="20342-144">Sitio web/aplicación de Azure</span><span class="sxs-lookup"><span data-stu-id="20342-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="20342-145">Entorno no Windows (LAMP, etc.)</span><span class="sxs-lookup"><span data-stu-id="20342-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="20342-146">Validador de partes de horas externo</span><span class="sxs-lookup"><span data-stu-id="20342-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="20342-147">Project Importador</span><span class="sxs-lookup"><span data-stu-id="20342-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="20342-148">Externo/Independiente</span><span class="sxs-lookup"><span data-stu-id="20342-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="20342-149">REST</span><span class="sxs-lookup"><span data-stu-id="20342-149">REST</span></span>  <br/> <span data-ttu-id="20342-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="20342-150">CSOM</span></span>  <br/> |<span data-ttu-id="20342-151">REST: cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="20342-151">REST - any platform</span></span>  <br/> <span data-ttu-id="20342-152">CSOM: cualquier plataforma compatible con .NET</span><span class="sxs-lookup"><span data-stu-id="20342-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="20342-153">Entrada de tarjeta de tiempo</span><span class="sxs-lookup"><span data-stu-id="20342-153">Timecard entry</span></span>  <br/> <span data-ttu-id="20342-154">Migración de proyectos a un nuevo sitio</span><span class="sxs-lookup"><span data-stu-id="20342-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="20342-155">Cambiar estado de administración.</span><span class="sxs-lookup"><span data-stu-id="20342-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="20342-156">¿Qué se necesita para empezar a desarrollar aplicaciones para Project Online?</span><span class="sxs-lookup"><span data-stu-id="20342-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="20342-157">Los elementos comunes necesarios para desarrollar aplicaciones Project Online son una cuenta de Project Online y datos de prueba, proyectos e información relacionada con proyectos que incluyen asignaciones, tareas, recursos y campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="20342-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="20342-158">También se necesita un entorno de desarrollo, pero los detalles del entorno de desarrollo dependen del tipo de aplicación y de la interfaz api necesaria para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20342-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="20342-159">En las siguientes secciones se describen las necesidades de desarrollo de las tres interfaces de API.</span><span class="sxs-lookup"><span data-stu-id="20342-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="20342-160">La documentación de referencia describe el modelo de objetos que es común para las tres interfaces, así como un mapa de entidades que muestra las relaciones entre los componentes del modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="20342-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="20342-161">Project de desarrollo de complementos hospedados</span><span class="sxs-lookup"><span data-stu-id="20342-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="20342-162">Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para la ejecución en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="20342-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="20342-163">Los complementos hospedados pueden usar las interfaces JSOM o REST y se escriben en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="20342-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="20342-164">Project Online proporciona referencias a la biblioteca JSOM para la ejecución en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="20342-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="20342-165">Suponiendo que el desarrollo se encuentra en Windows plataforma, los recursos necesarios son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="20342-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="20342-166">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="20342-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="20342-167">Office de desarrollo para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="20342-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="20342-168">Lenguaje JavaScript</span><span class="sxs-lookup"><span data-stu-id="20342-168">JavaScript language</span></span>
    
<span data-ttu-id="20342-169">Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20342-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="20342-170">Puede descargar y ejecutar el ejemplo en unos sencillos pasos:</span><span class="sxs-lookup"><span data-stu-id="20342-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="20342-171">Descargar y abrir la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20342-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="20342-172">Actualizar SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="20342-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="20342-173">Project Online examina el ámbito de aplicación del complemento y los permisos de usuario para administrar el acceso a la información en el host Project Online usuario.</span><span class="sxs-lookup"><span data-stu-id="20342-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="20342-174">Si el acceso se deniega explícitamente en cualquiera de las dos opciones de configuración, Project Online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="20342-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="20342-175">De lo contrario, se concede acceso.</span><span class="sxs-lookup"><span data-stu-id="20342-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="20342-176">Habilitar [la instalación local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en el sitio.</span><span class="sxs-lookup"><span data-stu-id="20342-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="20342-177">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-177">Build the project.</span></span>
    
5. <span data-ttu-id="20342-178">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="20342-179">Project de desarrollo de complementos hospedados por el proveedor</span><span class="sxs-lookup"><span data-stu-id="20342-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="20342-180">Los complementos hospedados por el proveedor son aplicaciones escritas y que residen en cualquier plataforma web.</span><span class="sxs-lookup"><span data-stu-id="20342-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="20342-181">Pueden conectarse y realizar operaciones de datos mediante la API de REST (o CSOM para plataformas Microsoft).</span><span class="sxs-lookup"><span data-stu-id="20342-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="20342-182">Cualquier idioma y entorno que admita la interfaz REST se puede usar para el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="20342-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="20342-183">Un ejemplo del entorno Windows desarrollo de este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="20342-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="20342-184">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="20342-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="20342-185">Microsoft Office Herramientas de desarrollo para Visual Studio (suministradas con Visual Studio ediciones Professional y Enterprise 2015)</span><span class="sxs-lookup"><span data-stu-id="20342-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="20342-186">.NET Framework 4.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="20342-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="20342-187">[Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="20342-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="20342-188">Un lenguaje de programación, como C #</span><span class="sxs-lookup"><span data-stu-id="20342-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="20342-189">Visita https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para ver scripts de ejemplo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="20342-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="20342-190">Puede ejecutar el ejemplo en unos pocos pasos:</span><span class="sxs-lookup"><span data-stu-id="20342-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="20342-191">Descargar y abrir la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20342-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="20342-192">Actualizar SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="20342-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="20342-193">Project Online examina el ámbito de aplicación del complemento y los permisos de usuario para administrar el acceso a la información en el host Project Online usuario.</span><span class="sxs-lookup"><span data-stu-id="20342-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="20342-194">Si el acceso se deniega explícitamente en cualquiera de las dos opciones de configuración, Project Online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="20342-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="20342-195">De lo contrario, se concede acceso.</span><span class="sxs-lookup"><span data-stu-id="20342-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="20342-196">Habilitar [la instalación local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en el sitio.</span><span class="sxs-lookup"><span data-stu-id="20342-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="20342-197">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-197">Build the project.</span></span>
    
5. <span data-ttu-id="20342-198">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="20342-199">Entorno de desarrollo de aplicaciones externo/independiente</span><span class="sxs-lookup"><span data-stu-id="20342-199">External/standalone application development environment</span></span>

<span data-ttu-id="20342-200">Una aplicación independiente puede llamar a Project Online mediante el Modelo de objetos del lado cliente (CSOM) o REST para comunicarse con Project Online para crear, recuperar, actualizar y eliminar información que reside en el servidor.</span><span class="sxs-lookup"><span data-stu-id="20342-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="20342-201">Se trata de una aplicación cliente independiente que depende del nivel de acceso de usuario que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="20342-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="20342-202">Un ejemplo del entorno Windows desarrollo de este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="20342-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="20342-203">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="20342-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="20342-204">Microsoft Office Herramientas de desarrollo para Visual Studio (suministradas con Visual Studio ediciones Professional y Enterprise 2015)</span><span class="sxs-lookup"><span data-stu-id="20342-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="20342-205">.NET Framework 4.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="20342-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="20342-206">[Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="20342-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="20342-207">Un lenguaje de programación, como C #</span><span class="sxs-lookup"><span data-stu-id="20342-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="20342-208">Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20342-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="20342-209">Puede ejecutar el ejemplo en unos pocos pasos:</span><span class="sxs-lookup"><span data-stu-id="20342-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="20342-210">Descargar la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="20342-210">Download the sample application</span></span>
    
2. <span data-ttu-id="20342-211">Realice un par de cambios para obtener acceso a Project Online sitio: el nombre del sitio, la cuenta de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="20342-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="20342-212">Asegúrese de que el usuario tiene acceso a todos los proyectos.</span><span class="sxs-lookup"><span data-stu-id="20342-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="20342-213">Project Online los permisos de usuario para administrar el acceso a la información en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="20342-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="20342-214">Agregue el ensamblado SharePoint a las referencias mediante la Consola de nuget Administrador de paquetes, disponible en el menú Herramientas escribiendo lo siguiente en la consola de Nuget:</span><span class="sxs-lookup"><span data-stu-id="20342-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="20342-215">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-215">Build the project.</span></span>
    
5. <span data-ttu-id="20342-216">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20342-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="20342-217">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="20342-217">Next steps</span></span>

<span data-ttu-id="20342-218">Cada aplicación de ejemplo tiene un artículo para explicar los aspectos más destacados de trabajar con la API Project individual.</span><span class="sxs-lookup"><span data-stu-id="20342-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="20342-219">Los artículos aparecen en la siguiente lista, junto con algunos artículos que describen las relaciones de entidad, la información sobre el sistema de consultas y el acceso a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="20342-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="20342-220">Desarrollo de una aplicación Project Online con el modelo de objetos del lado cliente</span><span class="sxs-lookup"><span data-stu-id="20342-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="20342-221">Desarrollar un complemento Project Online con el modelo de objetos de JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="20342-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="20342-222">Obtener acceso a campos personalizados de empresa de Project Online</span><span class="sxs-lookup"><span data-stu-id="20342-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="20342-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="20342-223">See also</span></span>

<span data-ttu-id="20342-224">Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="20342-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

