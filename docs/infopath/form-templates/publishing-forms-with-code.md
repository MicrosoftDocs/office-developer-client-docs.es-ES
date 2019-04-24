---
title: Publicar formularios con código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Cualquier administrador de la colección de sitios puede publicar formularios con código directamente desde el Asistente para la publicación de InfoPath Designer en una biblioteca de formularios de SharePoint. El código se ejecuta en un entorno de espacio aislado para que los códigos malintencionados no puedan dañar el servidor. Esto se denomina publicación de una solución de espacio aislado o publicación en la infraestructura de espacio aislado de SharePoint.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303510"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="38aca-105">Publicar formularios con código</span><span class="sxs-lookup"><span data-stu-id="38aca-105">Publishing Forms with Code</span></span>

<span data-ttu-id="38aca-106">Cualquier administrador de la colección de sitios puede publicar formularios con código directamente desde el Asistente para la publicación de InfoPath Designer en una biblioteca de formularios de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="38aca-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="38aca-107">El código se ejecuta en un entorno de espacio aislado para que los códigos malintencionados no puedan dañar el servidor.</span><span class="sxs-lookup"><span data-stu-id="38aca-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="38aca-108">Esto se denomina publicación de una solución de espacio aislado o publicación en la infraestructura de espacio aislado de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="38aca-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="38aca-109">InfoPath 2010 y SharePoint Server 2010 también admiten soluciones implementadas por el administrador.</span><span class="sxs-lookup"><span data-stu-id="38aca-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="38aca-110">Un diseñador de formularios publica formularios con código en un almacén local y después un administrador de la granja de SharePoint los revisa y carga.</span><span class="sxs-lookup"><span data-stu-id="38aca-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="38aca-111">El código es de plena confianza y puede incorporar funcionalidad que requiere privilegios elevados como E/S de archivo.</span><span class="sxs-lookup"><span data-stu-id="38aca-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="38aca-112">Comparar soluciones de espacio aislado y aprobadas por administrador</span><span class="sxs-lookup"><span data-stu-id="38aca-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="38aca-113">La tabla siguiente resume las diferencias entre la publicación de soluciones de espacio aislado y aprobadas por el administrador.</span><span class="sxs-lookup"><span data-stu-id="38aca-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="38aca-114">**Soluciones de espacio aislado**</span><span class="sxs-lookup"><span data-stu-id="38aca-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="38aca-115">**Soluciones aprobadas por el administrador**</span><span class="sxs-lookup"><span data-stu-id="38aca-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38aca-116">**Permisos requeridos**</span><span class="sxs-lookup"><span data-stu-id="38aca-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="38aca-117">Pueden ser publicadas por cualquier administrador de colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="38aca-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="38aca-118">Pueden ser implementadas por un administrador de granjas.</span><span class="sxs-lookup"><span data-stu-id="38aca-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="38aca-119">**Publicación**</span><span class="sxs-lookup"><span data-stu-id="38aca-119">**Publishing**</span></span> <br/> |<span data-ttu-id="38aca-120">Se puede publicar directamente desde InfoPath.</span><span class="sxs-lookup"><span data-stu-id="38aca-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="38aca-121">Pueden ser implementadas con una herramienta de Administración central o de línea de comandos stsadm.</span><span class="sxs-lookup"><span data-stu-id="38aca-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="38aca-122">**Protection**</span><span class="sxs-lookup"><span data-stu-id="38aca-122">**Protection**</span></span> <br/> |<span data-ttu-id="38aca-123">El código se ejecuta en un entorno de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="38aca-123">Code is run in a sandboxed environment.</span></span> <span data-ttu-id="38aca-124">Esto ayuda a proteger el servidor contra códigos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="38aca-124">This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="38aca-125">El código puede ejecutarse con plena confianza y tener acceso a cualquier recurso del servidor.</span><span class="sxs-lookup"><span data-stu-id="38aca-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="38aca-126">**Uso recomendado**</span><span class="sxs-lookup"><span data-stu-id="38aca-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="38aca-127">Formularios que solo requieren una pequeña cantidad de códigos.</span><span class="sxs-lookup"><span data-stu-id="38aca-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="38aca-128">Formularios que contienen varias líneas de código.</span><span class="sxs-lookup"><span data-stu-id="38aca-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="38aca-129">Publicación desde plantillas de formulario como soluciones de espacio aislado</span><span class="sxs-lookup"><span data-stu-id="38aca-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="38aca-p105">La publicación de un formulario con código como una solución de espacio aislado no difiere de la publicación de cualquier otro formulario en una biblioteca de documentos. Simplemente se debe usar al asistente para publicación como se hace habitualmente y el formulario se cargará en el servidor y funcionará en el espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="38aca-p105">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library. Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="38aca-132">Tenga en cuenta que existen algunas restricciones para la implementación del formulario como una solución de espacio aislado:</span><span class="sxs-lookup"><span data-stu-id="38aca-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="38aca-133">Debe ser un formulario de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="38aca-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="38aca-134">Debe usarse C# o Visual Basic como lenguaje de programación.</span><span class="sxs-lookup"><span data-stu-id="38aca-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="38aca-135">No se puede enviar a conexiones de datos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="38aca-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="38aca-136">No puede tener propiedades promovidas por conexiones parte a parte.</span><span class="sxs-lookup"><span data-stu-id="38aca-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="38aca-137">No se debe tener ningún control de metadatos ni conexiones de datos administrados.</span><span class="sxs-lookup"><span data-stu-id="38aca-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="38aca-138">Para habilitar estos administradores de colección de sitios para el uso de soluciones de espacio aislado en Microsoft SharePoint Server 2010 o un servidor que ejecute Microsoft SharePoint Foundation 2010, el administrador de la granja debe iniciar el servicio de código del usuario de Windows SharePoint.</span><span class="sxs-lookup"><span data-stu-id="38aca-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="38aca-139">Para iniciar el servicio de código del usuario de Windows SharePoint</span><span class="sxs-lookup"><span data-stu-id="38aca-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="38aca-140">Abra Administración central.</span><span class="sxs-lookup"><span data-stu-id="38aca-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="38aca-141">En **Servicios del sistema**, haga clic en **Administrar servicios en el servidor**.</span><span class="sxs-lookup"><span data-stu-id="38aca-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="38aca-142">Inicie el **Servicio de código del usuario de Microsoft SharePoint Foundation**.</span><span class="sxs-lookup"><span data-stu-id="38aca-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="38aca-143">Para publicar una solución de espacio aislado</span><span class="sxs-lookup"><span data-stu-id="38aca-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="38aca-144">Abra la plantilla de formulario en el diseñador de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="38aca-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="38aca-145">Haga clic en la pestaña **Archivo** y, a continuación, haga clic en **SharePoint Server** en la ficha **Publicar** en Backstage.</span><span class="sxs-lookup"><span data-stu-id="38aca-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="38aca-146">Escriba la dirección URL del sitio de SharePoint donde se realizará la publicación y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="38aca-147">[!IMPORTANTE] Debe ser administrador de una colección de sitios en este sitio para publicar esta plantilla de formulario como un solución de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="38aca-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="38aca-148">Seleccione **Biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="38aca-149">Seleccione **Crear una nueva biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="38aca-150">Escriba el nombre y las descripciones de la biblioteca de formularios y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="38aca-151">Haga clic en **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="38aca-151">Click **Publish**.</span></span>
    
<span data-ttu-id="38aca-152">Por ejemplo, soluciones que reflejan escenarios adecuados para plantillas de formularios publicadas como soluciones de espacio aislado, vea [Soluciones de espacio aislado de ejemplo](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="38aca-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="38aca-153">Publicar plantillas de formularios como soluciones implementadas por el administrador</span><span class="sxs-lookup"><span data-stu-id="38aca-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="38aca-154">La publicación de formularios como plantilla aprobada por el administrador es una opción recomendada si el formulario tiene varias conexiones de datos, si requiere seguridad de plena confianza o si requiere una plantilla para toda la granja.</span><span class="sxs-lookup"><span data-stu-id="38aca-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="38aca-155">Existen varios pasos que un administrador de granja debe realizar para que la solución implementada por el administrador esté disponible en SharePoint; y como programador, se debe preparar la solución antes de que participe el administrador.</span><span class="sxs-lookup"><span data-stu-id="38aca-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="38aca-156">En primer lugar, si el formulario se va a implementar como de plena confianza, debe definir el nivel de seguridad tal como se describe en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="38aca-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="38aca-157">Para definir el nivel de seguridad de una plantilla de formulario en plena confianza</span><span class="sxs-lookup"><span data-stu-id="38aca-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="38aca-158">Abra la plantilla de formulario en el diseñador de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="38aca-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="38aca-159">Haga clic en la pestaña **Archivo**, en la ficha **Información** haga clic en **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="38aca-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="38aca-160">Haga clic en la categoría **Seguridad y confianza** y después desactive la casilla **Determinar automáticamente el nivel de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="38aca-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="38aca-161">Seleccione **Plena confianza**.</span><span class="sxs-lookup"><span data-stu-id="38aca-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="38aca-162">A continuación, publique el formulario mediante el siguiente procedimiento, pero tenga en cuenta que existen algunas diferencias con un procedimiento de publicación estándar.</span><span class="sxs-lookup"><span data-stu-id="38aca-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="38aca-163">Para publicar una solución implementada por el administrador</span><span class="sxs-lookup"><span data-stu-id="38aca-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="38aca-164">En la primera página del **Asistente para publicación**, especifique la ubicación del sitio de SharePoint Server 2010 o SharePoint Foundation 2010 y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="38aca-p106">InfoPath seleccionará automáticamente la casilla **Plantilla de formulario aprobada por el administrador** en la segunda página del asistente. Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="38aca-p106">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard. Click **Next**.</span></span>
    
3. <span data-ttu-id="38aca-p107">La tercera página es única para escenarios de implementación del administrador. En lugar de seleccionar un SharePoint Server, publique el formulario en un almacén local. El administrador de SharePoint cargará el archivo desde esta ubicación durante el proceso de implementación del administrador.</span><span class="sxs-lookup"><span data-stu-id="38aca-p107">The third page is unique to administrator-deployed scenarios. Instead of selecting a SharePoint Server, publish the form to a local store. The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="38aca-170">Complete las páginas restantes del **Asistente para publicación**.</span><span class="sxs-lookup"><span data-stu-id="38aca-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

