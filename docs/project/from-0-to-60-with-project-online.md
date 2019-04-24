---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un sitio de Project online (SharePoint hospedado) mediante el uso de aplicaciones independientes o de complementos de Project. Una gran cantidad de aplicaciones es posible que van desde necesidades de direccionamiento de las personas involucradas en un proyecto a funciones de soporte de PMO, como una de las siguientes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344411"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="73cc9-103">De 0 a 60 con Project Online</span><span class="sxs-lookup"><span data-stu-id="73cc9-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="73cc9-104">Un desarrollador de aplicaciones puede personalizar un sitio de Project online (SharePoint hospedado) mediante el uso de aplicaciones independientes o de complementos de Project. Una gran cantidad de aplicaciones es posible que van desde necesidades de direccionamiento de las personas involucradas en un proyecto a funciones de soporte de PMO, como una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="73cc9-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="73cc9-105">Entrada de datos de tarjetas de registro simplificadas para trabajadores</span><span class="sxs-lookup"><span data-stu-id="73cc9-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="73cc9-106">Aprobación eficaz de la tarjeta de horas para supervisores</span><span class="sxs-lookup"><span data-stu-id="73cc9-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="73cc9-107">Supervisión de los permisos (adquisición y estado) necesarios para un proyecto</span><span class="sxs-lookup"><span data-stu-id="73cc9-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="73cc9-108">Estado/comprobación de estado de los proyectos activos</span><span class="sxs-lookup"><span data-stu-id="73cc9-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="73cc9-109">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="73cc9-109">Issues report</span></span>
- <span data-ttu-id="73cc9-110">Informe de estado de administración de cambios</span><span class="sxs-lookup"><span data-stu-id="73cc9-110">Change Management Status report</span></span>
    
<span data-ttu-id="73cc9-111">Project online incluye compatibilidad con la API para acomodar los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="73cc9-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="73cc9-112">Para un complemento hospedado de Project (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="73cc9-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="73cc9-113">Código (JavaScript, HTML, CSS) que se hospeda en SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="73cc9-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="73cc9-114">Activos que se descargan en el explorador y se ejecutan con SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="73cc9-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="73cc9-115">Lógica empresarial en JavaScript</span><span class="sxs-lookup"><span data-stu-id="73cc9-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="73cc9-116">Obtener acceso a los datos que se encuentran en Project online o en SharePoint (pero no se limita a ellos):</span><span class="sxs-lookup"><span data-stu-id="73cc9-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="73cc9-117">Custom fields</span><span class="sxs-lookup"><span data-stu-id="73cc9-117">Custom fields</span></span>  
  - <span data-ttu-id="73cc9-118">Listas</span><span class="sxs-lookup"><span data-stu-id="73cc9-118">Lists</span></span>
    
- <span data-ttu-id="73cc9-119">Para un complemento hospedado por el proveedor de Project (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="73cc9-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="73cc9-120">Código que existe en un sitio externo al sitio de Project online</span><span class="sxs-lookup"><span data-stu-id="73cc9-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="73cc9-121">Un sitio externo, que puede estar (sin limitarse a):</span><span class="sxs-lookup"><span data-stu-id="73cc9-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="73cc9-122">Otro sitio de SharePoint</span><span class="sxs-lookup"><span data-stu-id="73cc9-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="73cc9-123">Aplicación o servicio web creado en cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="73cc9-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="73cc9-124">El sitio externo contiene lógica empresarial</span><span class="sxs-lookup"><span data-stu-id="73cc9-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="73cc9-125">El explorador se redirige desde Project online al sitio externo con tokens de acceso a Project online.</span><span class="sxs-lookup"><span data-stu-id="73cc9-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="73cc9-126">El sitio externo puede realizar llamadas a SharePoint y Project online</span><span class="sxs-lookup"><span data-stu-id="73cc9-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="73cc9-127">Para un complemento externo/independiente:</span><span class="sxs-lookup"><span data-stu-id="73cc9-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="73cc9-128">El usuario ejecuta una aplicación en su dispositivo</span><span class="sxs-lookup"><span data-stu-id="73cc9-128">User executes an application on their device</span></span>
  - <span data-ttu-id="73cc9-129">La aplicación autentica y llama a las API de Project online directamente</span><span class="sxs-lookup"><span data-stu-id="73cc9-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="73cc9-130">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="73cc9-130">Type of application</span></span>|<span data-ttu-id="73cc9-131">Implementación de la API</span><span class="sxs-lookup"><span data-stu-id="73cc9-131">API implementation</span></span>|<span data-ttu-id="73cc9-132">Entorno de destino</span><span class="sxs-lookup"><span data-stu-id="73cc9-132">Target environment</span></span>|<span data-ttu-id="73cc9-133">Ejemplos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="73cc9-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73cc9-134">Proyecto hospedado</span><span class="sxs-lookup"><span data-stu-id="73cc9-134">Project hosted</span></span>  <br/> |<span data-ttu-id="73cc9-135">JSOM (modelo de objetos de Java Script)</span><span class="sxs-lookup"><span data-stu-id="73cc9-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="73cc9-136">REST</span><span class="sxs-lookup"><span data-stu-id="73cc9-136">REST</span></span>  <br/> |<span data-ttu-id="73cc9-137">Explorador</span><span class="sxs-lookup"><span data-stu-id="73cc9-137">Browser</span></span>  <br/> |<span data-ttu-id="73cc9-138">Entrada de tarjeta de registro</span><span class="sxs-lookup"><span data-stu-id="73cc9-138">Timecard entry</span></span>  <br/> <span data-ttu-id="73cc9-139">Aprobación de la tarjeta de horas</span><span class="sxs-lookup"><span data-stu-id="73cc9-139">Timecard approval</span></span>  <br/> <span data-ttu-id="73cc9-140">Estado de proyecto</span><span class="sxs-lookup"><span data-stu-id="73cc9-140">Project Status</span></span>  <br/> <span data-ttu-id="73cc9-141">Informe de problemas</span><span class="sxs-lookup"><span data-stu-id="73cc9-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="73cc9-142">Proveedor de proyecto hospedado</span><span class="sxs-lookup"><span data-stu-id="73cc9-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="73cc9-143">Biblioteca cliente de CSOM</span><span class="sxs-lookup"><span data-stu-id="73cc9-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="73cc9-144">Sitio web/aplicación de Azure</span><span class="sxs-lookup"><span data-stu-id="73cc9-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="73cc9-145">Entorno que no es de Windows (lámpara, etc.)</span><span class="sxs-lookup"><span data-stu-id="73cc9-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="73cc9-146">Validador de parte de horas externo</span><span class="sxs-lookup"><span data-stu-id="73cc9-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="73cc9-147">Importador de Project</span><span class="sxs-lookup"><span data-stu-id="73cc9-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="73cc9-148">Externa/independiente</span><span class="sxs-lookup"><span data-stu-id="73cc9-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="73cc9-149">REST</span><span class="sxs-lookup"><span data-stu-id="73cc9-149">REST</span></span>  <br/> <span data-ttu-id="73cc9-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="73cc9-150">CSOM</span></span>  <br/> |<span data-ttu-id="73cc9-151">REST: cualquier plataforma</span><span class="sxs-lookup"><span data-stu-id="73cc9-151">REST - any platform</span></span>  <br/> <span data-ttu-id="73cc9-152">CSOM: cualquier plataforma compatible con .NET</span><span class="sxs-lookup"><span data-stu-id="73cc9-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="73cc9-153">Entrada de tarjeta de registro</span><span class="sxs-lookup"><span data-stu-id="73cc9-153">Timecard entry</span></span>  <br/> <span data-ttu-id="73cc9-154">Migración de proyectos a un sitio nuevo</span><span class="sxs-lookup"><span data-stu-id="73cc9-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="73cc9-155">Cambiar el estado de administración.</span><span class="sxs-lookup"><span data-stu-id="73cc9-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="73cc9-156">¿Qué se debe hacer para empezar a desarrollar aplicaciones para Project online?</span><span class="sxs-lookup"><span data-stu-id="73cc9-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="73cc9-157">Los elementos comunes necesarios para desarrollar aplicaciones de Project online son una cuenta de Project online y datos de prueba, así como proyectos e información relacionada con el proyecto, que incluyen asignaciones, tareas, recursos y campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="73cc9-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="73cc9-158">También se necesita un entorno de desarrollo, pero las características específicas del entorno de desarrollo dependen del tipo de aplicación y de la interfaz de la API necesaria para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73cc9-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="73cc9-159">En las siguientes secciones se describen las necesidades de desarrollo de las tres interfaces API.</span><span class="sxs-lookup"><span data-stu-id="73cc9-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="73cc9-160">En la documentación de referencia se describe el modelo de objetos que es común para las tres interfaces, así como una asignación de entidad que muestra las relaciones entre los componentes del modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="73cc9-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="73cc9-161">Entorno de desarrollo de complementos hospedados en Project</span><span class="sxs-lookup"><span data-stu-id="73cc9-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="73cc9-162">Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para la ejecución en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="73cc9-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="73cc9-163">Los complementos hospedados pueden usar las interfaces de JSOM o REST y están escritos en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73cc9-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="73cc9-164">Project online proporciona referencias a la biblioteca JSOM para la ejecución en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="73cc9-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="73cc9-165">SuPoniendo que el desarrollo se encuentra en una plataforma Windows, los recursos necesarios siguen estos pasos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="73cc9-166">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="73cc9-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="73cc9-167">Herramientas de desarrollo de Office para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73cc9-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="73cc9-168">Lenguaje JavaScript</span><span class="sxs-lookup"><span data-stu-id="73cc9-168">JavaScript language</span></span>
    
<span data-ttu-id="73cc9-169">Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para obtener una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73cc9-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="73cc9-170">Puede descargar y ejecutar el ejemplo en unos sencillos pasos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="73cc9-171">Descarga y apertura de la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="73cc9-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="73cc9-172">Actualizar SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="73cc9-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="73cc9-173">Project online examina tanto el ámbito de aplicación del complemento como los permisos de usuario para controlar el acceso a la información en el host de Project online.</span><span class="sxs-lookup"><span data-stu-id="73cc9-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="73cc9-174">Si se deniega explícitamente el acceso en una o ambas configuraciones, Project online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="73cc9-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="73cc9-175">De lo contrario, se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="73cc9-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="73cc9-176">Habilite la [transferencia local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio.</span><span class="sxs-lookup"><span data-stu-id="73cc9-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="73cc9-177">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-177">Build the project.</span></span>
    
5. <span data-ttu-id="73cc9-178">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="73cc9-179">Entorno de desarrollo de complementos hospedados por el proveedor de Project</span><span class="sxs-lookup"><span data-stu-id="73cc9-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="73cc9-180">Los complementos hospedados por el proveedor son aplicaciones escritas y que residen en cualquier plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="73cc9-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="73cc9-181">Pueden conectar y realizar operaciones de datos con la API de REST (u CSOM para plataformas de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="73cc9-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="73cc9-182">Cualquier lenguaje y entorno que admita la interfaz de REST puede usarse para el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="73cc9-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="73cc9-183">Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="73cc9-184">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="73cc9-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="73cc9-185">Herramientas de desarrollo de Microsoft Office para Visual Studio (incluidas con Visual Studio 2015 Professional y Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="73cc9-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="73cc9-186">.NET Framework 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="73cc9-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="73cc9-187">[Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="73cc9-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="73cc9-188">Un lenguaje de programación, como C#</span><span class="sxs-lookup"><span data-stu-id="73cc9-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="73cc9-189">Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabajar con scripts de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73cc9-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="73cc9-190">Puede ejecutar el ejemplo en unos pocos pasos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="73cc9-191">Descarga y apertura de la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="73cc9-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="73cc9-192">Actualizar SiteURL en la ventana Propiedades</span><span class="sxs-lookup"><span data-stu-id="73cc9-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="73cc9-193">Project online examina tanto el ámbito de aplicación del complemento como los permisos de usuario para controlar el acceso a la información en el host de Project online.</span><span class="sxs-lookup"><span data-stu-id="73cc9-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="73cc9-194">Si se deniega explícitamente el acceso en una o ambas configuraciones, Project online deniega el acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="73cc9-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="73cc9-195">De lo contrario, se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="73cc9-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="73cc9-196">Habilite la [transferencia local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio.</span><span class="sxs-lookup"><span data-stu-id="73cc9-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="73cc9-197">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-197">Build the project.</span></span>
    
5. <span data-ttu-id="73cc9-198">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="73cc9-199">Entorno de desarrollo de aplicaciones externas/independientes</span><span class="sxs-lookup"><span data-stu-id="73cc9-199">External/standalone application development environment</span></span>

<span data-ttu-id="73cc9-200">Una aplicación independiente puede llamar a Project online mediante el modelo de objetos del lado cliente (CSOM) o REST para comunicarse con Project online para crear, recuperar, actualizar y eliminar información residente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="73cc9-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="73cc9-201">Se trata de una aplicación cliente independiente que depende del nivel de acceso de usuario que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="73cc9-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="73cc9-202">Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="73cc9-203">Visual Studio 2015 (preferido) o Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="73cc9-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="73cc9-204">Herramientas de desarrollo de Microsoft Office para Visual Studio (incluidas con Visual Studio 2015 Professional y Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="73cc9-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="73cc9-205">.NET Framework 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="73cc9-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="73cc9-206">[Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="73cc9-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="73cc9-207">Un lenguaje de programación, como C#</span><span class="sxs-lookup"><span data-stu-id="73cc9-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="73cc9-208">Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para obtener una aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73cc9-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="73cc9-209">Puede ejecutar el ejemplo en unos pocos pasos:</span><span class="sxs-lookup"><span data-stu-id="73cc9-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="73cc9-210">Descargar la aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="73cc9-210">Download the sample application</span></span>
    
2. <span data-ttu-id="73cc9-211">Realice un par de cambios para obtener acceso al sitio de Project online: el nombre del sitio, la cuenta de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="73cc9-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="73cc9-212">Asegúrese de que el usuario tiene acceso a todos los proyectos.</span><span class="sxs-lookup"><span data-stu-id="73cc9-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="73cc9-213">Project online usa permisos de usuario para regir el acceso a la información en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="73cc9-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="73cc9-214">Agregue el ensamblado de SharePoint a las referencias mediante la consola del administrador de paquetes de Nuget, disponible en el menú herramientas; para ello, escriba lo siguiente en la consola de Nuget:</span><span class="sxs-lookup"><span data-stu-id="73cc9-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="73cc9-215">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-215">Build the project.</span></span>
    
5. <span data-ttu-id="73cc9-216">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73cc9-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="73cc9-217">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="73cc9-217">Next steps</span></span>

<span data-ttu-id="73cc9-218">Cada aplicación de ejemplo tiene un artículo para explicar los aspectos destacados del trabajo con la API de proyecto individual.</span><span class="sxs-lookup"><span data-stu-id="73cc9-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="73cc9-219">Los artículos aparecen en la lista siguiente, junto con algunos artículos que describen las relaciones entre las entidades, la información sobre el sistema de consultas y el acceso a los campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="73cc9-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="73cc9-220">Desarrollo de una aplicación de Project online con el modelo de objetos del lado cliente</span><span class="sxs-lookup"><span data-stu-id="73cc9-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="73cc9-221">Desarrollar un complemento de Project online con el modelo de objetos de JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="73cc9-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="73cc9-222">Obtener acceso a campos personalizados de empresa de Project Online</span><span class="sxs-lookup"><span data-stu-id="73cc9-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="73cc9-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="73cc9-223">See also</span></span>

<span data-ttu-id="73cc9-224">Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="73cc9-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

