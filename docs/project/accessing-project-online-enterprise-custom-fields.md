---
title: Obtener acceso a campos personalizados de empresa de Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es campos personalizados de empresa (ECFs). ECFs son campos de valor de tipo que se pueden agregar a proyectos, recursos y tareas. En la siguiente tabla se enumera ECFs que asocian con proyectos, recursos y tareas y proporciona un ejemplo de un valor de una instancia de ese ECF:'
ms.openlocfilehash: d560b258f2c9873844009cb6bc6e698abec029a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584607"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="11226-106">Obtener acceso a campos personalizados de empresa de Project Online</span><span class="sxs-lookup"><span data-stu-id="11226-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="11226-107">Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales.</span><span class="sxs-lookup"><span data-stu-id="11226-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="11226-108">Un área de extensión es campos personalizados de empresa (ECFs).</span><span class="sxs-lookup"><span data-stu-id="11226-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="11226-109">ECFs son campos de valor de tipo que se pueden agregar a proyectos, recursos y tareas.</span><span class="sxs-lookup"><span data-stu-id="11226-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="11226-110">En la siguiente tabla se enumera ECFs que asocian con proyectos, recursos y tareas y proporciona un ejemplo de un valor de una instancia de ese ECF:</span><span class="sxs-lookup"><span data-stu-id="11226-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="11226-111">Nombre ECF</span><span class="sxs-lookup"><span data-stu-id="11226-111">ECF Name</span></span>|<span data-ttu-id="11226-112">Tipo ECF</span><span class="sxs-lookup"><span data-stu-id="11226-112">ECF Type</span></span>|<span data-ttu-id="11226-113">Association</span><span class="sxs-lookup"><span data-stu-id="11226-113">Association</span></span>|<span data-ttu-id="11226-114">Valor de ejemplo</span><span class="sxs-lookup"><span data-stu-id="11226-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11226-115">Justificación</span><span class="sxs-lookup"><span data-stu-id="11226-115">Justification</span></span>  <br/> |<span data-ttu-id="11226-116">TEXT</span><span class="sxs-lookup"><span data-stu-id="11226-116">TEXT</span></span>  <br/> |<span data-ttu-id="11226-117">Project</span><span class="sxs-lookup"><span data-stu-id="11226-117">Project</span></span>  <br/> |<span data-ttu-id="11226-118">Un usuario final puede registrar estadísticas vitales y datos de mantenimiento, con los resultados que incluyen una evaluación de mantenimiento y una acción individual plan hacia la salud mejor.</span><span class="sxs-lookup"><span data-stu-id="11226-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="11226-119">Clasificación de riesgos</span><span class="sxs-lookup"><span data-stu-id="11226-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="11226-120">TEXT</span><span class="sxs-lookup"><span data-stu-id="11226-120">TEXT</span></span>  <br/> |<span data-ttu-id="11226-121">Project</span><span class="sxs-lookup"><span data-stu-id="11226-121">Project</span></span>  <br/> |<span data-ttu-id="11226-122">Low</span><span class="sxs-lookup"><span data-stu-id="11226-122">Low</span></span>  <br/> |
|<span data-ttu-id="11226-123">RENDIMIENTO DE LA INVERSIÓN</span><span class="sxs-lookup"><span data-stu-id="11226-123">ROI</span></span>  <br/> |<span data-ttu-id="11226-124">NÚMERO</span><span class="sxs-lookup"><span data-stu-id="11226-124">NUMBER</span></span>  <br/> |<span data-ttu-id="11226-125">Project</span><span class="sxs-lookup"><span data-stu-id="11226-125">Project</span></span>  <br/> |<span data-ttu-id="11226-126">2,10</span><span class="sxs-lookup"><span data-stu-id="11226-126">2.10</span></span>  <br/> |
|<span data-ttu-id="11226-127">Costo total</span><span class="sxs-lookup"><span data-stu-id="11226-127">Total Cost</span></span>  <br/> |<span data-ttu-id="11226-128">COSTO</span><span class="sxs-lookup"><span data-stu-id="11226-128">COST</span></span>  <br/> |<span data-ttu-id="11226-129">Project</span><span class="sxs-lookup"><span data-stu-id="11226-129">Project</span></span>  <br/> |<span data-ttu-id="11226-130">$1,031,514</span><span class="sxs-lookup"><span data-stu-id="11226-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="11226-131">Inicio del equipo</span><span class="sxs-lookup"><span data-stu-id="11226-131">Launch Team</span></span>  <br/> |<span data-ttu-id="11226-132">TEXT</span><span class="sxs-lookup"><span data-stu-id="11226-132">TEXT</span></span>  <br/> |<span data-ttu-id="11226-133">Resources</span><span class="sxs-lookup"><span data-stu-id="11226-133">Resources</span></span>  <br/> |<span data-ttu-id="11226-134">Sí</span><span class="sxs-lookup"><span data-stu-id="11226-134">Yes</span></span>  <br/> |
|<span data-ttu-id="11226-135">Rol de posición</span><span class="sxs-lookup"><span data-stu-id="11226-135">Position Role</span></span>  <br/> |<span data-ttu-id="11226-136">TEXT</span><span class="sxs-lookup"><span data-stu-id="11226-136">TEXT</span></span>  <br/> |<span data-ttu-id="11226-137">Resources</span><span class="sxs-lookup"><span data-stu-id="11226-137">Resources</span></span>  <br/> |<span data-ttu-id="11226-138">Evaluador</span><span class="sxs-lookup"><span data-stu-id="11226-138">Tester</span></span>  <br/> |
|<span data-ttu-id="11226-139">Estado de marca</span><span class="sxs-lookup"><span data-stu-id="11226-139">Flag Status</span></span>  <br/> |<span data-ttu-id="11226-140">MARCA</span><span class="sxs-lookup"><span data-stu-id="11226-140">FLAG</span></span>  <br/> |<span data-ttu-id="11226-141">Task</span><span class="sxs-lookup"><span data-stu-id="11226-141">Task</span></span>  <br/> |<span data-ttu-id="11226-142">No</span><span class="sxs-lookup"><span data-stu-id="11226-142">No</span></span>  <br/> |
|<span data-ttu-id="11226-143">Mantenimiento</span><span class="sxs-lookup"><span data-stu-id="11226-143">Health</span></span>  <br/> |<span data-ttu-id="11226-144">TEXT</span><span class="sxs-lookup"><span data-stu-id="11226-144">TEXT</span></span>  <br/> |<span data-ttu-id="11226-145">Task</span><span class="sxs-lookup"><span data-stu-id="11226-145">Task</span></span>  <br/> |<span data-ttu-id="11226-146">No se ha especificado</span><span class="sxs-lookup"><span data-stu-id="11226-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="11226-147">ECFs se definen en la instancia de Project Web Application (PWA), externa desde cualquier proyecto, recurso o tarea.</span><span class="sxs-lookup"><span data-stu-id="11226-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="11226-148">Sin embargo, pueden resultar asociados a un proyecto, recurso o tarea.</span><span class="sxs-lookup"><span data-stu-id="11226-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="11226-149">En este artículo se proporciona una introducción a los campos personalizados con una aplicación de ejemplo y se centra en la recuperación de valores de ECF.</span><span class="sxs-lookup"><span data-stu-id="11226-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="11226-150">Puede descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="11226-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="11226-151">Además, Project Online admite los campos personalizados locales como de sólo lectura entidades específicas para el proyecto específico, recurso o tarea.</span><span class="sxs-lookup"><span data-stu-id="11226-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="11226-152">Para obtener más información en los campos personalizados locales, vea el ejemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="11226-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="11226-153">Material de fondo</span><span class="sxs-lookup"><span data-stu-id="11226-153">Background materials</span></span>

<span data-ttu-id="11226-154">Un artículo anterior, [desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente](developing-a-project-online-application-using-the-client-side-object-model.md), proporciona información y la orientación inicial para el desarrollo de aplicaciones con CSOM.</span><span class="sxs-lookup"><span data-stu-id="11226-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="11226-155">Consulte este artículo para los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="11226-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="11226-156">Información general acerca de Project, ediciones independientes y basada en la nube</span><span class="sxs-lookup"><span data-stu-id="11226-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="11226-157">Entorno de desarrollo (ediciones de Visual Studio y bibliotecas de software)</span><span class="sxs-lookup"><span data-stu-id="11226-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="11226-158">Instalación de proyecto de Visual Studio para una aplicación de .NET mediante la biblioteca de CSOM</span><span class="sxs-lookup"><span data-stu-id="11226-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="11226-159">Conectar con el servicio de Project Online</span><span class="sxs-lookup"><span data-stu-id="11226-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="11226-160">Preliminar (declaraciones de nivel de clase)</span><span class="sxs-lookup"><span data-stu-id="11226-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="11226-161">La clase para esta aplicación define dos elementos de datos: el contexto del proyecto y el diccionario pwaECF.</span><span class="sxs-lookup"><span data-stu-id="11226-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="11226-162">El objeto de contexto de proyecto es parte del proyecto CSOM y conecta a la aplicación y la instancia de PWA.</span><span class="sxs-lookup"><span data-stu-id="11226-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="11226-163">Todas las solicitudes al servicio de utilizan el contexto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="11226-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="11226-164">El contexto necesita que el extremo de conexión para crear una instancia de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="11226-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="11226-165">El extremo de la conexión es la dirección URL de la instancia de PWA.</span><span class="sxs-lookup"><span data-stu-id="11226-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="11226-166">El diccionario pwaECF almacena el proyecto ECFs definidos en el nivel de PWA.</span><span class="sxs-lookup"><span data-stu-id="11226-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="11226-167">El diccionario usa la ECF. InternalName como la clave y el objeto CustomField como el valor.</span><span class="sxs-lookup"><span data-stu-id="11226-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="11226-168">El diccionario se rellenó en el método ListPWACustomFields y, a continuación, se utiliza como referencia en el método Main.</span><span class="sxs-lookup"><span data-stu-id="11226-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="11226-169">Principal (método)</span><span class="sxs-lookup"><span data-stu-id="11226-169">Main method</span></span>

<span data-ttu-id="11226-170">El método Main administra el flujo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11226-170">The Main method manages the application flow.</span></span> <span data-ttu-id="11226-171">Como con otras aplicaciones que usan el CSOM de Project Online, Main inicializa el contexto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="11226-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="11226-172">Recuperar y la ECFs en el Project Online PWA de la lista.</span><span class="sxs-lookup"><span data-stu-id="11226-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="11226-173">Esta funcionalidad se implementa en el método ListPWACustomFields.</span><span class="sxs-lookup"><span data-stu-id="11226-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="11226-174">Recuperar proyectos con campos personalizados y campos no personalizados.</span><span class="sxs-lookup"><span data-stu-id="11226-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="11226-175">Al recuperar proyectos con ECFs, las necesidades de la solicitud de consulta al servicio de Project Online incluir los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="11226-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="11226-176">**IncludeCustomFields** &ndash; Este elemento solicita el servicio para devolver una colección de PublishedProjects donde cada proyecto publicado incluye una extensión que es compatible con los campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="11226-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="11226-177">A menos que se especifica este elemento, Project Online devuelve objetos PublishedProject que no incluyen datos de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="11226-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="11226-178">**IncludeCustomFields.CustomFields** &ndash; este elemento solicita el servicio para rellenar los objetos PublishedProject con datos de CustomFields.</span><span class="sxs-lookup"><span data-stu-id="11226-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="11226-179">La siguiente solicitud especifica el identificador de proyecto y nombre, así como la extensión del objeto de campos personalizados y los valores de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="11226-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="11226-180">Se examinan en cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="11226-180">Examine each project.</span></span>
    
   <span data-ttu-id="11226-181">Los objetos de proyecto utilizados en esta aplicación son el tipo de PublishedProject debido a que los valores se recuperan y se muestran.</span><span class="sxs-lookup"><span data-stu-id="11226-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="11226-182">Si necesita actualizar los valores de datos en uno o más proyectos, ¿puede desproteger el proyecto llevando a cabo la actualización y la aplicación usaría un objeto DraftProject para recuperar los valores y actualizar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="11226-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="11226-183">Obtener acceso a las entradas de ECF para un proyecto</span><span class="sxs-lookup"><span data-stu-id="11226-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="11226-184">Cada instancia ECF separa el valor del campo del resto de la información de ECF.</span><span class="sxs-lookup"><span data-stu-id="11226-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="11226-185">El valor del campo se almacena como parte de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="11226-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="11226-186">El resto de la información se almacena en un objeto CustomField.</span><span class="sxs-lookup"><span data-stu-id="11226-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="11226-187">Obtener acceso a los valores ECF en un proyecto consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="11226-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="11226-188">Recorrer en iteración la colección de CustomFields</span><span class="sxs-lookup"><span data-stu-id="11226-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="11226-189">Obtener acceso a la entrada correcta mediante dos construcciones.</span><span class="sxs-lookup"><span data-stu-id="11226-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="11226-190">Cada proyecto almacena entradas ECF asociadas en dos lugares, una colección de CustomFields es enumerable y y los valores de campo como parte de pares clave/valor.</span><span class="sxs-lookup"><span data-stu-id="11226-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="11226-191">En los pares clave/valor, el valor de internalName es la clave y el valor del campo es el valor.</span><span class="sxs-lookup"><span data-stu-id="11226-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="11226-192">Utilizar un diccionario para mantener y obtener acceso a los valores de campo.</span><span class="sxs-lookup"><span data-stu-id="11226-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="11226-193">Las propiedades ECF, que no sean los valores de campo, se almacenan en objetos CustomField, un objeto por proyecto.</span><span class="sxs-lookup"><span data-stu-id="11226-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="11226-194">Usar una colección CustomFields para tener acceso a la ECFs asociados con un proyecto individual.</span><span class="sxs-lookup"><span data-stu-id="11226-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="11226-195">Cada proyecto almacena el ECFs asociados en una colección donde cada entrada ECF consta de una clave--el nombre interno de la ECF--y un objeto que contiene el valor de la ECF.</span><span class="sxs-lookup"><span data-stu-id="11226-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="11226-196">Transferir un diccionario para tener acceso a las entradas individuales a la colección.</span><span class="sxs-lookup"><span data-stu-id="11226-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="11226-197">Sigue la declaración.</span><span class="sxs-lookup"><span data-stu-id="11226-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="11226-198">El valor de una entrada de diccionario corresponde al tipo de datos de la ECF.</span><span class="sxs-lookup"><span data-stu-id="11226-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="11226-199">El objeto para cada ECF se asigna a uno de los diversos tipos.</span><span class="sxs-lookup"><span data-stu-id="11226-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="11226-200">ECFs mayoría usan tipos simples que se ajustan a las variables estándares.</span><span class="sxs-lookup"><span data-stu-id="11226-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="11226-201">El siguiente fragmento muestra que está implicado un procesamiento mínimo para varios tipos:</span><span class="sxs-lookup"><span data-stu-id="11226-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
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

   <span data-ttu-id="11226-202">La tabla de búsqueda de valores de texto, sin embargo, requiere procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="11226-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="11226-203">La aplicación recupera la tabla de consulta adecuados desde el servicio y envía la instancia ECF (con uno o varios valores) recorriendo la tabla de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="11226-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="11226-204">El siguiente fragmento de código muestra el procesamiento de texto ECFs, incluidas las con valores simples y aquellas utilizando tablas de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="11226-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
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

   <span data-ttu-id="11226-205">Esta aplicación simplemente genera los valores; Sin embargo, es posible obtener más significado de los valores de datos.</span><span class="sxs-lookup"><span data-stu-id="11226-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="11226-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="11226-206">ListPWACustomFields</span></span>

<span data-ttu-id="11226-207">El método ListPWACustomFields recupera y enumera los ECFs asociados con los proyectos.</span><span class="sxs-lookup"><span data-stu-id="11226-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="11226-208">Este método muestra el ECFs registrados en la instancia de PWA que puede asociarse con proyectos individuales.</span><span class="sxs-lookup"><span data-stu-id="11226-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="11226-209">El punto de entrada para obtener acceso a la ECFs usa el elemento CustomFields del contexto de proyecto, como se muestra en la siguiente solicitud de consulta:</span><span class="sxs-lookup"><span data-stu-id="11226-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="11226-210">El método no se comprueba para ver si un proyecto utiliza un ECF específico.</span><span class="sxs-lookup"><span data-stu-id="11226-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11226-211">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="11226-211">See also</span></span>

- [<span data-ttu-id="11226-212">Portal del proyecto de desarrollo</span><span class="sxs-lookup"><span data-stu-id="11226-212">Project Development Portal</span></span>](https://developer.microsoft.com/en-us/project)
- [<span data-ttu-id="11226-213">Información general: Los campos personalizados de empresa y tablas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="11226-213">Overview: Enterprise custom fields and lookup tables</span></span>](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- <span data-ttu-id="11226-214">[Local y campos personalizados de empresa](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="11226-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="11226-215">Agregar o editar campos personalizados de empresa en Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="11226-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/en-us/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

