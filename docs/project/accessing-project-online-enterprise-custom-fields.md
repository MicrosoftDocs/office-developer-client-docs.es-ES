---
title: Obtener acceso a campos personalizados de empresa de Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es Campos personalizados de empresa (ECF). Los ECF son campos de valor de tipo que pueden agregarse a los proyectos, recursos y tareas. La siguiente tabla enumera ECF que se asocian con proyectos, recursos y tareas, y proporciona un ejemplo de un valor para una instancia de ese ECF:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708308"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="82d56-106">Obtener acceso a campos personalizados de empresa de Project Online</span><span class="sxs-lookup"><span data-stu-id="82d56-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="82d56-107">Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales.</span><span class="sxs-lookup"><span data-stu-id="82d56-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="82d56-108">Un área de extensión es Campos personalizados de empresa (ECF).</span><span class="sxs-lookup"><span data-stu-id="82d56-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="82d56-109">Los ECF son campos de valor de tipo que pueden agregarse a los proyectos, recursos y tareas.</span><span class="sxs-lookup"><span data-stu-id="82d56-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="82d56-110">La siguiente tabla enumera ECF que se asocian con proyectos, recursos y tareas, y proporciona un ejemplo de un valor para una instancia de ese ECF:</span><span class="sxs-lookup"><span data-stu-id="82d56-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="82d56-111">Nombre del ECF</span><span class="sxs-lookup"><span data-stu-id="82d56-111">ECF Name</span></span>|<span data-ttu-id="82d56-112">Tipo de ECF</span><span class="sxs-lookup"><span data-stu-id="82d56-112">ECF Type</span></span>|<span data-ttu-id="82d56-113">Asociación</span><span class="sxs-lookup"><span data-stu-id="82d56-113">Association</span></span>|<span data-ttu-id="82d56-114">Valor de ejemplo</span><span class="sxs-lookup"><span data-stu-id="82d56-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82d56-115">Justificación</span><span class="sxs-lookup"><span data-stu-id="82d56-115">Justification</span></span>  <br/> |<span data-ttu-id="82d56-116">TEXTO</span><span class="sxs-lookup"><span data-stu-id="82d56-116">TEXT</span></span>  <br/> |<span data-ttu-id="82d56-117">Proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-117">Project</span></span>  <br/> |<span data-ttu-id="82d56-118">Un usuario final puede registrar estadísticas vitales y datos de mantenimiento, con resultados que incluyan una evaluación de mantenimiento y un plan de acción individualizado para mejorar el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="82d56-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="82d56-119">Clasificación de riesgos</span><span class="sxs-lookup"><span data-stu-id="82d56-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="82d56-120">TEXTO</span><span class="sxs-lookup"><span data-stu-id="82d56-120">TEXT</span></span>  <br/> |<span data-ttu-id="82d56-121">Proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-121">Project</span></span>  <br/> |<span data-ttu-id="82d56-122">Bajo</span><span class="sxs-lookup"><span data-stu-id="82d56-122">Low</span></span>  <br/> |
|<span data-ttu-id="82d56-123">RENTABILIDAD DE LA INVERSIÓN</span><span class="sxs-lookup"><span data-stu-id="82d56-123">ROI</span></span>  <br/> |<span data-ttu-id="82d56-124">NÚMERO</span><span class="sxs-lookup"><span data-stu-id="82d56-124">Number()</span></span>  <br/> |<span data-ttu-id="82d56-125">Proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-125">Project</span></span>  <br/> |<span data-ttu-id="82d56-126">2.10</span><span class="sxs-lookup"><span data-stu-id="82d56-126">2.10</span></span>  <br/> |
|<span data-ttu-id="82d56-127">Costo total</span><span class="sxs-lookup"><span data-stu-id="82d56-127">Total Cost</span></span>  <br/> |<span data-ttu-id="82d56-128">COSTO</span><span class="sxs-lookup"><span data-stu-id="82d56-128">Cost</span></span>  <br/> |<span data-ttu-id="82d56-129">Proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-129">Project</span></span>  <br/> |<span data-ttu-id="82d56-130">$1,031,514</span><span class="sxs-lookup"><span data-stu-id="82d56-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="82d56-131">Equipo de lanzamiento</span><span class="sxs-lookup"><span data-stu-id="82d56-131">Launch Team</span></span>  <br/> |<span data-ttu-id="82d56-132">TEXTO</span><span class="sxs-lookup"><span data-stu-id="82d56-132">TEXT</span></span>  <br/> |<span data-ttu-id="82d56-133">Recursos</span><span class="sxs-lookup"><span data-stu-id="82d56-133">Resources</span></span>  <br/> |<span data-ttu-id="82d56-134">Sí</span><span class="sxs-lookup"><span data-stu-id="82d56-134">Yes</span></span>  <br/> |
|<span data-ttu-id="82d56-135">Rol del puesto</span><span class="sxs-lookup"><span data-stu-id="82d56-135">Position Role</span></span>  <br/> |<span data-ttu-id="82d56-136">TEXTO</span><span class="sxs-lookup"><span data-stu-id="82d56-136">TEXT</span></span>  <br/> |<span data-ttu-id="82d56-137">Recursos</span><span class="sxs-lookup"><span data-stu-id="82d56-137">Resources</span></span>  <br/> |<span data-ttu-id="82d56-138">Herramienta de comprobación</span><span class="sxs-lookup"><span data-stu-id="82d56-138">Tester</span></span>  <br/> |
|<span data-ttu-id="82d56-139">Estado de marca</span><span class="sxs-lookup"><span data-stu-id="82d56-139">Flag Status</span></span>  <br/> |<span data-ttu-id="82d56-140">MARCA</span><span class="sxs-lookup"><span data-stu-id="82d56-140">Flag</span></span>  <br/> |<span data-ttu-id="82d56-141">Tarea</span><span class="sxs-lookup"><span data-stu-id="82d56-141">Task</span></span>  <br/> |<span data-ttu-id="82d56-142">No</span><span class="sxs-lookup"><span data-stu-id="82d56-142">No</span></span>  <br/> |
|<span data-ttu-id="82d56-143">Mantenimiento</span><span class="sxs-lookup"><span data-stu-id="82d56-143">Health</span></span>  <br/> |<span data-ttu-id="82d56-144">TEXTO</span><span class="sxs-lookup"><span data-stu-id="82d56-144">TEXT</span></span>  <br/> |<span data-ttu-id="82d56-145">Tarea</span><span class="sxs-lookup"><span data-stu-id="82d56-145">Task</span></span>  <br/> |<span data-ttu-id="82d56-146">No especificado</span><span class="sxs-lookup"><span data-stu-id="82d56-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="82d56-147">Los ECF se definen en la instancia de Project Web Application (PWA), como ajenos a cualquier proyecto, recurso o tarea.</span><span class="sxs-lookup"><span data-stu-id="82d56-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="82d56-148">Sin embargo, pueden asociarse con un proyecto, tarea o recurso.</span><span class="sxs-lookup"><span data-stu-id="82d56-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="82d56-149">Este artículo proporciona una introducción a los campos personalizados usando una aplicación de ejemplo y se centra en cómo recuperar los valores de ECF.</span><span class="sxs-lookup"><span data-stu-id="82d56-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="82d56-150">Puedes descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="82d56-150">You can download the completed sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="82d56-151">Además, Project Online es compatible con campos personalizados locales como entidades de solo lectura específicas del proyecto, el recurso o la tarea.</span><span class="sxs-lookup"><span data-stu-id="82d56-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="82d56-152">Para obtener más información sobre los campos personalizados locales, consulta el ejemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="82d56-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="82d56-153">Materiales del contexto</span><span class="sxs-lookup"><span data-stu-id="82d56-153">Background materials</span></span>

<span data-ttu-id="82d56-154">Un artículo anterior, [Desarrollo de una aplicación de Project Online con el modelo de objetos de cliente](developing-a-project-online-application-using-the-client-side-object-model.md), proporciona el contexto y la orientación inicial para desarrollar aplicaciones con CSOM.</span><span class="sxs-lookup"><span data-stu-id="82d56-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="82d56-155">Consulta este artículo para los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="82d56-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="82d56-156">Información de contexto sobre Project, ediciones independientes y en la nube</span><span class="sxs-lookup"><span data-stu-id="82d56-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="82d56-157">Entorno de desarrollo (ediciones de Visual Studio y bibliotecas de software)</span><span class="sxs-lookup"><span data-stu-id="82d56-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="82d56-158">Configuración de proyecto de Visual Studio para una aplicación de .NET con la biblioteca de CSOM</span><span class="sxs-lookup"><span data-stu-id="82d56-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="82d56-159">Cómo conectarse al servicio de Project Online</span><span class="sxs-lookup"><span data-stu-id="82d56-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="82d56-160">Preliminares (declaraciones de clase)</span><span class="sxs-lookup"><span data-stu-id="82d56-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="82d56-161">La clase para esta aplicación define dos elementos de datos: el contexto del proyecto y el diccionario pwaECF.</span><span class="sxs-lookup"><span data-stu-id="82d56-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="82d56-162">El objeto de contexto del proyecto forma parte del CSOM de Project y conecta la aplicación y la instancia de PWA.</span><span class="sxs-lookup"><span data-stu-id="82d56-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="82d56-163">Todas las solicitudes de servicio usan el contexto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="82d56-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="82d56-164">El contexto necesita que el extremo de la conexión cree una instancia en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="82d56-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="82d56-165">El extremo de conexión es la dirección URL de tu instancia de PWA.</span><span class="sxs-lookup"><span data-stu-id="82d56-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="82d56-166">El diccionario pwaECF almacena los ECF del proyecto definidos en el nivel de PWA.</span><span class="sxs-lookup"><span data-stu-id="82d56-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="82d56-167">El diccionario usa ECF. InternalName como la clave y el objeto CustomField como el valor.</span><span class="sxs-lookup"><span data-stu-id="82d56-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="82d56-168">El diccionario se completa en el método ListPWACustomFields y, a continuación, se usa como referencia del método Main.</span><span class="sxs-lookup"><span data-stu-id="82d56-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="82d56-169">Método Main</span><span class="sxs-lookup"><span data-stu-id="82d56-169">Main method</span></span>

<span data-ttu-id="82d56-170">El método Main administra el flujo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82d56-170">The Main method manages the application flow.</span></span> <span data-ttu-id="82d56-171">Como sucede con otras aplicaciones que utilizan el CSOM de Project Online, Main inicializa el contexto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="82d56-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="82d56-172">Recupera y enumera los ECF en la PWA de Project Online.</span><span class="sxs-lookup"><span data-stu-id="82d56-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="82d56-173">Esta funcionalidad se implementa en el método ListPWACustomFields.</span><span class="sxs-lookup"><span data-stu-id="82d56-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="82d56-174">Recuperar proyectos con campos personalizados y campos no personalizados.</span><span class="sxs-lookup"><span data-stu-id="82d56-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="82d56-175">Cuando se recuperan proyectos con los ECF, la solicitud de consulta al servicio de Project Online debe incluir los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="82d56-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="82d56-176">**IncludeCustomFields** &ndash;Este elemento solicita que el servicio devuelva una recopilación de PublishedProjects donde cada proyecto publicado incluye una extensión que admite campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="82d56-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="82d56-177">A menos que se especifique este elemento, Project Online devuelve objetos de PublishedProject que no incluyen datos de Campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="82d56-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="82d56-178">**IncludeCustomFields.CustomFields** &ndash; Este elemento solicita al servicio rellenar los objetos de PublishedProject con datos de CustomFields.</span><span class="sxs-lookup"><span data-stu-id="82d56-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="82d56-179">La solicitud siguiente especifica la Id. y el nombre de proyecto, así como la extensión del objeto de campos personalizados y los valores del campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="82d56-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="82d56-180">Examina cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="82d56-180">Examine each project.</span></span>
    
   <span data-ttu-id="82d56-181">Los objetos del proyecto utilizados en esta aplicación son del tipo PublishedProject porque se recuperan y se muestran los valores.</span><span class="sxs-lookup"><span data-stu-id="82d56-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="82d56-182">Si necesitas actualizar los valores de datos de uno o varios proyectos, el proyecto que se somete a la actualización se retira y la aplicación usa un objeto DraftProject para recuperar los valores y actualizar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="82d56-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="82d56-183">Acceso a las entradas de ECF para un proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="82d56-184">Cada instancia de ECF separa el valor del campo del resto de la información de ECF.</span><span class="sxs-lookup"><span data-stu-id="82d56-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="82d56-185">El valor del campo se almacena como parte de un par clave/valor.</span><span class="sxs-lookup"><span data-stu-id="82d56-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="82d56-186">El resto de la información se almacena en un objeto CustomField.</span><span class="sxs-lookup"><span data-stu-id="82d56-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="82d56-187">La obtención de acceso a los valores de ECF consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="82d56-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="82d56-188">Movimiento cíclico a través de una recopilación de CustomFields</span><span class="sxs-lookup"><span data-stu-id="82d56-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="82d56-189">Acceso a la entrada correcta utilizando dos construcciones.</span><span class="sxs-lookup"><span data-stu-id="82d56-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="82d56-190">Cada proyecto almacena entradas de ECF asociadas en dos lugares, una recopilación de CustomFields que se puede enumerar y valores de campo como parte de los pares clave/valor.</span><span class="sxs-lookup"><span data-stu-id="82d56-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="82d56-191">En los pares clave/valor, internalName es la clave y el valor del campo es el valor.</span><span class="sxs-lookup"><span data-stu-id="82d56-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="82d56-192">Utiliza un diccionario para mantener los valores de campo y acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="82d56-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="82d56-193">Las propiedades de ECF, a excepción de los valores de campo, se almacenan en objetos CustomField, a razón de un objeto por proyecto.</span><span class="sxs-lookup"><span data-stu-id="82d56-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="82d56-194">Usa una recopilación de CustomFields para acceder a los ECF asociados a un proyecto individual.</span><span class="sxs-lookup"><span data-stu-id="82d56-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="82d56-195">Cada proyecto almacena los ECF asociados en una recopilación en donde cada entrada de ECF se compone de una clave (el nombre interno del ECF) y un objeto que contiene el valor del ECF.</span><span class="sxs-lookup"><span data-stu-id="82d56-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="82d56-196">Transferir la recopilación a un diccionario para tener acceso a las entradas individuales.</span><span class="sxs-lookup"><span data-stu-id="82d56-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="82d56-197">Luego, sigue la declaración.</span><span class="sxs-lookup"><span data-stu-id="82d56-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="82d56-198">El valor de una entrada de diccionario corresponde al tipo de datos del ECF.</span><span class="sxs-lookup"><span data-stu-id="82d56-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="82d56-199">El objeto para cada ECF se asigna a uno de los distintos tipos.</span><span class="sxs-lookup"><span data-stu-id="82d56-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="82d56-200">La mayoría de los ECF usan tipos simples que se ajustan a variables estándar.</span><span class="sxs-lookup"><span data-stu-id="82d56-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="82d56-201">El siguiente fragmento muestra que interviene un procesamiento mínimo para varios tipos:</span><span class="sxs-lookup"><span data-stu-id="82d56-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   <span data-ttu-id="82d56-202">Sin embargo, la tabla de búsqueda de valores TEXT requiere un procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="82d56-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="82d56-203">La aplicación recupera la tabla de búsqueda adecuada del servicio y genera la instancia de ECF (con uno o varios valores), mediante un recorrido por la tabla de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="82d56-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="82d56-204">El siguiente fragmento de código muestra el procesamiento de ECF TEXT, incluidos aquellos con valores simples y aquellos que usan tablas de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="82d56-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   <span data-ttu-id="82d56-205">Esta aplicación simplemente genera los valores; sin embargo, es posible obtener más significado de los valores de datos.</span><span class="sxs-lookup"><span data-stu-id="82d56-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="82d56-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="82d56-206">ListPWACustomFields</span></span>

<span data-ttu-id="82d56-207">El método ListPWACustomFields recupera y enumera los ECF asociados con los proyectos.</span><span class="sxs-lookup"><span data-stu-id="82d56-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="82d56-208">Este método enumera los ECF registrados en la instancia de PWA que pueden asociarse con proyectos individuales.</span><span class="sxs-lookup"><span data-stu-id="82d56-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="82d56-209">El punto de entrada para tener acceso a los ECF usa el elemento CustomFields del contexto del proyecto, como en la siguiente petición de consulta:</span><span class="sxs-lookup"><span data-stu-id="82d56-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="82d56-210">El método no comprueba si un proyecto utiliza un ECF específico.</span><span class="sxs-lookup"><span data-stu-id="82d56-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82d56-211">Ver también</span><span class="sxs-lookup"><span data-stu-id="82d56-211">See also</span></span>

- [<span data-ttu-id="82d56-212">Portal de desarrollo del proyecto</span><span class="sxs-lookup"><span data-stu-id="82d56-212">Project Development Portal</span></span>](https://developer.microsoft.com/es-ES/project)
- <span data-ttu-id="82d56-213">
  [Información general: campos personalizados de empresa y tablas de búsqueda](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span><span class="sxs-lookup"><span data-stu-id="82d56-213">[Overview: Enterprise custom fields and lookup tables](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span></span>
- <span data-ttu-id="82d56-214">[Campos personalizados locales y de empresa](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="82d56-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="82d56-215">Adición o modificación de campos personalizados de empresa en Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="82d56-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

