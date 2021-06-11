---
title: Requisitos previos para los ejemplos de código basados en ASMX en Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- ejemplos de código, project server, Project Server, programming,PSI, compilación de ejemplos de código, PSI, programación
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Obtenga información para ayudarle a crear proyectos en Visual Studio mediante los ejemplos de código basados en ASMX que se incluyen en los temas de referencia Project Server Interface (PSI).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357095"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="79410-104">Requisitos previos para los ejemplos de código basados en ASMX en Project</span><span class="sxs-lookup"><span data-stu-id="79410-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="79410-105">Obtenga información para ayudarle a crear proyectos en Visual Studio mediante los ejemplos de código basados en ASMX que se incluyen en los temas de referencia Project Server Interface (PSI).</span><span class="sxs-lookup"><span data-stu-id="79410-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="79410-106">Muchos de los ejemplos de código incluidos en la biblioteca de clases de [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) y la referencia de servicio web se crearon originalmente para el SDK de Office Project 2007 y usan un formato estándar para los servicios web ASMX.</span><span class="sxs-lookup"><span data-stu-id="79410-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="79410-107">Los ejemplos siguen funcionando en Project Server 2013 y están diseñados para copiarse en una aplicación de consola y ejecutarse como una unidad completa.</span><span class="sxs-lookup"><span data-stu-id="79410-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="79410-108">Las excepciones están señaladas en la muestra.</span><span class="sxs-lookup"><span data-stu-id="79410-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="79410-109">Los nuevos ejemplos de PSI en Project SDK de 2013 se ajustan a un formato que usa Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="79410-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="79410-110">Las muestras basadas en ASMX también pueden adaptarse para usar servicios de WCF.</span><span class="sxs-lookup"><span data-stu-id="79410-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="79410-111">Este artículo muestra cómo usar las muestras con servicios web de ASMX.</span><span class="sxs-lookup"><span data-stu-id="79410-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="79410-112">Para obtener información acerca del uso de los ejemplos con servicios WCF, vea [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="79410-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="79410-113">La interfaz de servicios web ASMX de la PSI está en desuso en Project Server 2013, pero aún es compatible.</span><span class="sxs-lookup"><span data-stu-id="79410-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="79410-114">Si el modelo de objeto de cliente (CSOM) incluye los métodos que su aplicación necesita, deberían desarrollarse nuevas aplicaciones con el CSOM.</span><span class="sxs-lookup"><span data-stu-id="79410-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="79410-115">El CSOM permite a las aplicaciones trabajar con Project Online una instalación local de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="79410-116">De lo contrario, si su aplicación usa la PSI, debería usar la interfaz de WCF, que es la tecnología que recomendamos para las comunicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="79410-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="79410-117">Las aplicaciones que usan la interfaz ASMX o la interfaz WCF solo pueden funcionar para instalaciones locales de Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="79410-118">Para obtener más información acerca del CSOM, vea [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="79410-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="79410-119">Antes de usar las muestras de código, asegúrese de configurar el entorno de desarrollo, configurar la aplicación y modificar los valores de constantes genéricas para que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="79410-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="79410-120">Configurar el entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="79410-120">Setting up the development environment</span></span>
<span data-ttu-id="79410-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span></span>

1. <span data-ttu-id="79410-122">**Configurar un sistema de Project Server de prueba**.</span><span class="sxs-lookup"><span data-stu-id="79410-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="79410-p104">Use un sistema de Project Server de prueba siempre que haga un desarrollo o una prueba. Incluso cuando su código funcione perfectamente, las dependencias entre proyectos, los informes u otros factores de entorno pueden generar consecuencias no esperadas.</span><span class="sxs-lookup"><span data-stu-id="79410-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="79410-125">Asegúrese de ser un usuario válido en el servidor y compruebe que posee los permisos suficientes para las llamadas de la PSI que use su aplicación.</span><span class="sxs-lookup"><span data-stu-id="79410-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="79410-126">El tema de la referencia de desarrollador para cada método de PSI incluye una tabla de permisos de Project Server.</span><span class="sxs-lookup"><span data-stu-id="79410-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="79410-127">Por ejemplo, el [Project. El método QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requiere el **permiso global NewProject** y **el permiso SaveProjectTemplate.**</span><span class="sxs-lookup"><span data-stu-id="79410-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="79410-128">En algunos casos, quizás deba hacer una depuración remota en el servidor.</span><span class="sxs-lookup"><span data-stu-id="79410-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="79410-129">También es posible que tenga que configurar un controlador de eventos instalando un ensamblado de controlador de eventos en cada equipo de Project Server en la granja de servidores de SharePoint y, a continuación, configurando el controlador de eventos para la instancia de Project Web App mediante la página Configuración del servidor de Project en el Configuración de aplicación general de Administración central de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="79410-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="79410-130">**Configurar un PC de desarrollo.**</span><span class="sxs-lookup"><span data-stu-id="79410-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="79410-p107">Generalmente obtiene acceso a la PSI a través de una red. Las muestras de código están diseñadas para usarse en un cliente independiente del servidor, excepto cuando se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="79410-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="79410-133">**Instale la versión correcta de Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="79410-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="79410-134">Excepto cuando se lo especifique, las muestras de código se escriben en Visual C#.</span><span class="sxs-lookup"><span data-stu-id="79410-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="79410-135">Se pueden usar con Visual Studio 2010 o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="79410-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="79410-136">Asegúrese de tener instalado el Service Pack más reciente.</span><span class="sxs-lookup"><span data-stu-id="79410-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="79410-137">**Copie los DLL de Project Server en el PC de desarrollo.**</span><span class="sxs-lookup"><span data-stu-id="79410-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="79410-138">Copie los siguientes ensamblados `[Program Files]\Microsoft Office Servers\15.0\Bin` del equipo Project server en el equipo de desarrollo:</span><span class="sxs-lookup"><span data-stu-id="79410-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="79410-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="79410-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="79410-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="79410-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="79410-141">Para obtener información sobre cómo compilar y usar el ensamblado de proxy ProjectServerServices.dll para los servicios web de ASMX en la PSI, vea [Usar un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="79410-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="79410-142">**Instalar los archivos de IntelliSense.**</span><span class="sxs-lookup"><span data-stu-id="79410-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="79410-143">Para usar descripciones de IntelliSense para clases y miembros en ensamblados de Project Server, copie los archivos XML de IntelliSense actualizados de la descarga del SDK de Project 2013 en el mismo directorio donde se encuentran los ensamblados de Project Server.</span><span class="sxs-lookup"><span data-stu-id="79410-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="79410-144">Por ejemplo, copie el archivo Microsoft.Office.Project.Server.Library.xml al directorio donde su aplicación establecerá una referencia al ensamblado Microsoft.Office.Project.Server.Library.dll.</span><span class="sxs-lookup"><span data-stu-id="79410-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="79410-145">IntelliSense descripciones de los servicios web de PSI requieren que cree un ensamblado de proxy de PSI mediante el script CompileASMXProxyAssembly.cmd en el subdirectorio de la descarga del SDK de `Documentation\IntelliSense\WSDL` Project 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="79410-146">El script crea el ensamblado de proxy ProjectServerServices.dll basado en ASMX.</span><span class="sxs-lookup"><span data-stu-id="79410-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="79410-147">Para más información, vea el archivo [ReadMe_IntelliSense] en la descarga de SDK.</span><span class="sxs-lookup"><span data-stu-id="79410-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="79410-148">Crear la aplicación y agregar una referencia de servicio web</span><span class="sxs-lookup"><span data-stu-id="79410-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="79410-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span></span>

1. <span data-ttu-id="79410-150">**Crear una aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="79410-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="79410-p112">Cuando crea una aplicación de consola, en la lista desplegable del cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4**. Puede copiar el código de ejemplo de PSI en la nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="79410-p112">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**. You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="79410-153">**Agregar la referencia necesaria para ASMX.**</span><span class="sxs-lookup"><span data-stu-id="79410-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="79410-154">En el Explorador de soluciones, agregue una referencia a **System.Web.Services** (vea la Figura 1).</span><span class="sxs-lookup"><span data-stu-id="79410-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="79410-155">**Figura 1. Adición de una referencia en Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="79410-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="79410-156">![Agregar una referencia en Visual Studio]Agregar una referencia en(media/pj15_PrerequisitesASMX_AddReference.gif "Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="79410-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="79410-157">**Copiar el código**.</span><span class="sxs-lookup"><span data-stu-id="79410-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="79410-158">Copie el ejemplo de código completo en el archivo Program.cs de la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="79410-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="79410-159">**Establecer el espacio de nombres para la aplicación de muestra**.</span><span class="sxs-lookup"><span data-stu-id="79410-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="79410-p113">Puede cambiar el espacio de nombres que aparece en la parte superior de la muestra por el espacio de nombres predeterminado de la aplicación o bien cambiar el espacio de nombres de la aplicación predeterminado para que coincida con la muestra. Puede cambiar el espacio de nombres de la aplicación predeterminado modificando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79410-p113">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="79410-162">Por ejemplo, el ejemplo de código [de QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) tiene el espacio **de nombres Microsoft.SDK.Project. Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="79410-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="79410-163">Si el nombre del proyecto de Visual Studio es **RenameProject**, copie el espacio de nombres desde el archivo Program.cs y, después, abra el panel **Propiedades** del proyecto (en el menú **Proyecto**, elija **Propiedades de RenameProject**).</span><span class="sxs-lookup"><span data-stu-id="79410-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="79410-164">En la pestaña **Aplicación**, copie el espacio de nombres en el cuadro de texto **Espacio de nombre predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="79410-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="79410-165">**Establecer las referencias web**.</span><span class="sxs-lookup"><span data-stu-id="79410-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="79410-p115">Muchos ejemplos necesitan una referencia a uno o más de los servicios web de la PSI. Estos aparecen en la muestra misma o en comentarios que preceden a la muestra. Para obtener el espacio de nombres correcto de las referencias web, asegúrese de establecer primero el espacio de nombres de la aplicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="79410-p115">Most examples require a reference to one or more of the PSI web services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="79410-169">Existen tres maneras de agregar una referencia de servicio web de ASMX para la PSI:</span><span class="sxs-lookup"><span data-stu-id="79410-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="79410-170">Cree un ensamblado de proxy de PSI llamado ProjectServerServices.dll y, después, establezca una referencia al ensamblado.</span><span class="sxs-lookup"><span data-stu-id="79410-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="79410-171">Para obtener IntelliSense, esta es la manera recomendada de agregar una referencia de PSI.</span><span class="sxs-lookup"><span data-stu-id="79410-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="79410-172">Vea [Usar un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="79410-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="79410-p117">Agregue un archivo de proxy desde la salida wsdl.exe a la solución de Visual Studio. Vea [Agregar un archivo de proxy de PSI](#pj15_PrerequisitesASMX_AddingProxyFile).</span><span class="sxs-lookup"><span data-stu-id="79410-p117">Add a proxy file from the wsdl.exe output to the Visual Studio solution. See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="79410-p118">Agregue una referencia de servicio web usando Virtual Studio. Vea [Agregar una referencia de servicio web](#pj15_PrerequisitesASMX_AddingServiceReference).</span><span class="sxs-lookup"><span data-stu-id="79410-p118">Add a web service reference by using Visual Studio. See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="79410-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="79410-178">Usar un ensamblado de proxy de PSI y descripciones de IntelliSense</span><span class="sxs-lookup"><span data-stu-id="79410-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="79410-179">Puede crear y usar el ensamblado de proxy ProjectServerServices.dll para todos los servicios web basados en ASMX en la PSI, mediante el script CompileASMXProxyAssembly.cmd en la carpeta de la descarga del SDK de `Documentation\IntelliSense\WSDL` Project 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="79410-180">Para obtener un vínculo a la descarga, vea Project documentación para desarrolladores [de 2013](project-2013-developer-documentation.md).</span><span class="sxs-lookup"><span data-stu-id="79410-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="79410-181">Al extraer los archivos de origen de proxy del archivo Source.zip, los archivos de la carpeta están actualizados a partir de la fecha de publicación de la descarga del SDK de `Documentation\IntelliSense\WSDL\Source` Project 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="79410-182">Para generar archivos de origen de proxy de PSI actualizados, use el script GenASMXProxyAssembly.cmd en el PC de Project Server.</span><span class="sxs-lookup"><span data-stu-id="79410-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="79410-183">Los scripts de la  `Documentation\IntelliSense\WCF` carpeta no funcionan para aplicaciones basadas en ASMX.</span><span class="sxs-lookup"><span data-stu-id="79410-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="79410-184">El script GenWCFProxyAssembly.cmd llama a SvcUtil.exe, que genera archivos de código de origen para los servicios de WCF.</span><span class="sxs-lookup"><span data-stu-id="79410-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="79410-185">Los archivos de proxy de WCF incluyen diferentes atributos, la interfaz de canal, y una clase de cliente para cada servicio de PSI.</span><span class="sxs-lookup"><span data-stu-id="79410-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="79410-186">Por ejemplo, el servicio Recurso basado en WCF incluye la interfaz de **ResourceChannel**, la interfaz de **Resource**, y la clase **ResourceClient**.</span><span class="sxs-lookup"><span data-stu-id="79410-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="79410-187">La web de Recurso basado en ASMX incluye la clase **Resource** con algunas propiedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="79410-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="79410-188">A continuación se muestra el script GenASMXProxyAssembly.cmd que genera archivos de salida de WSDL para los servicios web de PSI, y después compila el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="79410-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

<span data-ttu-id="79410-189">El script usa el archivo ClassList_asmx.txt, que contiene la lista de servicios web que están disponibles para otros desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="79410-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

<span data-ttu-id="79410-p121">Los scripts crean un ensamblado con el nombre ProjectServerServices.dll. No lo confunda con ProjectServerServices.dll para el ensamblado basado en WCF. Los nombres de ensamblado son los mismos, para permitir el uso de cualquiera de los ensamblados con el archivo ProjectServerServices.xml de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="79410-p121">The scripts create an assembly named ProjectServerServices.dll. Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly. The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="79410-p122">El espacio de nombres arbitrario creado por los scripts tanto para los servicios web de ASMX como para los servicios de WCF es el mismo, de manera que el archivo ProjectServerServices.xml de IntelliSense funciona con ambos ensamblados. Por ejemplo, el espacio de nombres del servicio Recurso en el ensamblado de proxy basado en WCF y en el ensamblado de proxy basado en ASMX es **SvcResource**. Por supuesto, puede modificar los nombres de los espacios de nombres, si se asegura de que coinciden en el ensamblado de proxy y en el archivo ProjectServerServices.xml de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="79410-p122">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly. For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**. You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="79410-196">Si una muestra de código usa un nombre diferente para un espacio de nombres de servicio web de PSI, por ejemplo **ProjectWebSvc**, para que funcione IntelliSense asegúrese de cambiar la muestra para que use **SvcProject** de manera que el espacio de nombres coincida con el ensamblado de proxy.</span><span class="sxs-lookup"><span data-stu-id="79410-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="79410-197">Una ventaja de usar el ensamblado de proxy basado en ASMX es que incluye todos los nombres de espacio de servicio web de PSI; no tiene que crear varias referencias web.</span><span class="sxs-lookup"><span data-stu-id="79410-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="79410-198">Otra ventaja es que, si agrega el archivo ProjectServerServices.xml al mismo directorio donde estableció una referencia al ensamblado de proxy ProjectServerServices.dll, puede obtener descripciones de IntelliSense para los miembros y las clases de PSI.</span><span class="sxs-lookup"><span data-stu-id="79410-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="79410-199">La Figura 2 muestra el texto de IntelliSense para el método **Project.QueueCreateProject**.</span><span class="sxs-lookup"><span data-stu-id="79410-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="79410-200">Para obtener más información, vea el archivo [ReadMe_IntelliSense] en la carpeta IntelliSense de la descarga del SDK de Project 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="79410-201">**Figura 2. Uso de IntelliSense para un método en el servicio web de Recurso**</span><span class="sxs-lookup"><span data-stu-id="79410-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="79410-202">![Uso de Intellisense para un método en un servicio PSI]Mediante(media/pj15_PrerequisitesASMX_Intellisense.gif "Intellisense para un método en un servicio psi")</span><span class="sxs-lookup"><span data-stu-id="79410-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="79410-p124">Las desventajas de usar el ensamblado de proxy son que la solución es mayor y usted necesita distribuir e instalar el ensamblado de proxy con la solución. También necesita usar los mismos espacios de nombres que se encuentran en el ensamblado de proxy y los archivos de IntelliSense, a menos que cambie el script y el archivo ProjectServerServices.xml de IntelliSense para usar distintos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="79410-p124">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="79410-205">Agregar un archivo de proxy de PSI</span><span class="sxs-lookup"><span data-stu-id="79410-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="79410-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span></span>

<span data-ttu-id="79410-207">La Project SDK de 2013 incluye los archivos de origen generados por el comando Wsdl.exe para el ensamblado proxy.</span><span class="sxs-lookup"><span data-stu-id="79410-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="79410-208">Los archivos de origen se encuentran Source.zip en el  `Documentation\IntelliSense\ASMX` subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="79410-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="79410-209">En lugar de establecer una referencia al ensamblado de proxy, puede agregar uno o más archivos de origen a una solución de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79410-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="79410-210">Por ejemplo, después de usar el script GenASMXProxyAssembly.cmd, agregue el archivo wsdl.Project.cs file a la solución.</span><span class="sxs-lookup"><span data-stu-id="79410-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="79410-211">En vez de usar el script, puede usar los siguientes comandos para generar un solo archivo de origen, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79410-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="79410-p126">Para definir un objeto de **Project** como variable de clase con el nombre **project**, use el siguiente código. El método **AddContextInfo** agrega la información contextual al objeto de **project** para autenticación de Windows y autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="79410-p126">To define a **Project** object as a class variable named **project**, use the following code. The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> <span data-ttu-id="79410-214">Si usa un ensamblado de proxy de PSI o agrega un archivo de proxy para una referencia de servicio de Project llamada **SvcProject**, usaría el mismo código para crear un objeto de **project**.</span><span class="sxs-lookup"><span data-stu-id="79410-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="79410-215">Agregar una referencia de servicio web</span><span class="sxs-lookup"><span data-stu-id="79410-215">Adding a web service reference</span></span>
<span data-ttu-id="79410-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span></span>

<span data-ttu-id="79410-217">Si no usa el ensamblado de proxy basado en ASMX o agrega un archivo de salida de WSDL, puede establecer una o más referencias web individuales.</span><span class="sxs-lookup"><span data-stu-id="79410-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="79410-218">Los pasos siguientes muestran cómo establecer una referencia web mediante Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="79410-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="79410-219">En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** y después seleccione **Agregar referencia de servicio**.</span><span class="sxs-lookup"><span data-stu-id="79410-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="79410-220">En el cuadro de diálogo **Agregar referencia de servicio**, elija **Avanzada**.</span><span class="sxs-lookup"><span data-stu-id="79410-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="79410-221">En el cuadro de diálogo **Configuración de referencia de servicio**, elija **Agregar referencia web**.</span><span class="sxs-lookup"><span data-stu-id="79410-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="79410-222">En el cuadro de texto **Dirección URL,** escriba `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` y, a continuación, **presione Entrar** o elija el **icono Ir.**</span><span class="sxs-lookup"><span data-stu-id="79410-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="79410-223">Si tiene instalada la Capa de sockets seguros (SSL), asegúrese de usar el protocolo HTTPS en lugar del protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="79410-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="79410-224">Por ejemplo, use la siguiente dirección URL para el servicio Project en el `https://MyServer/pwa` sitio para Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="79410-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="79410-225">O bien, abra el explorador web y vaya a `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` .</span><span class="sxs-lookup"><span data-stu-id="79410-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="79410-226">Guarde el archivo en un directorio local, como `C:\Project\WebServices\ServiceName.wsdl` .</span><span class="sxs-lookup"><span data-stu-id="79410-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="79410-227">En el cuadro de diálogo **Agregar referencia web**, para **Dirección URL**, escriba el protocolo de archivo y la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="79410-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="79410-228">Por ejemplo, escriba `file://C:\Project\WebServices\Project.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="79410-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="79410-229">Una vez que se resuelve la referencia, escriba el nombre de la referencia en el cuadro de texto **Nombre de referencia web**.</span><span class="sxs-lookup"><span data-stu-id="79410-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="79410-230">Los ejemplos de código de Project documentación para desarrolladores de 2013 usan el nombre de referencia estándar arbitrario **Svc _ServiceName_**.</span><span class="sxs-lookup"><span data-stu-id="79410-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="79410-231">Por ejemplo, el servicio web de Proyecto tiene el nombre **SvcProject** (vea la Figura 3).</span><span class="sxs-lookup"><span data-stu-id="79410-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="79410-232">**Figura 3. Adición de una referencia de servicio web de ASMX**</span><span class="sxs-lookup"><span data-stu-id="79410-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="79410-233">![Adición de una referencia de servicio web ASMX](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adición de una referencia de servicio web ASMX")</span><span class="sxs-lookup"><span data-stu-id="79410-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="79410-234">Para los componentes de aplicación que deben usarse en el PC de Project Server, use suplantación, o tenga permisos elevados, use una referencia de servicio de WCF en lugar de una referencia web de ASMX.</span><span class="sxs-lookup"><span data-stu-id="79410-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="79410-235">Para obtener más información, vea [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="79410-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="79410-236">Estableciendo otras referencias</span><span class="sxs-lookup"><span data-stu-id="79410-236">Setting other references</span></span>
<span data-ttu-id="79410-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span></span>

<span data-ttu-id="79410-238">Project Las aplicaciones de servidor a menudo usan otros servicios, como SharePoint servicios web de Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="79410-239">Si se necesitan otros servicios, se lo señala en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="79410-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="79410-240">Las referencias locales para la muestra de código aparecen en las instrucciones de **using** en la parte superior de la muestra:</span><span class="sxs-lookup"><span data-stu-id="79410-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="79410-241">En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** y después seleccione **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="79410-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="79410-p133">Seleccione **Examinar** y después diríjase a la ubicación donde ha almacenado los DLL de Project Server que copió previamente. Elija los DLL que necesite y luego seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="79410-p133">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously. Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="79410-244">Asegúrese de que las versiones de ensamblado en su PC de desarrollo coincidan exactamente con aquellas del PC de Project Server de destino.</span><span class="sxs-lookup"><span data-stu-id="79410-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="79410-245">Usar autenticación múltiple</span><span class="sxs-lookup"><span data-stu-id="79410-245">Using multiple authentication</span></span>
<span data-ttu-id="79410-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span></span>

<span data-ttu-id="79410-247">La autenticación de usuarios Project servidor local, ya sea mediante autenticación Windows o autenticación de formularios, se realiza mediante el procesamiento de notificaciones en SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79410-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="79410-248">La autenticación múltiple significa que la aplicación web en la que se aprovisiona Project web app admite tanto la autenticación Windows como la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="79410-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="79410-249">Si ese es el caso, cualquier llamada a un servicio web de ASMX que use la autenticación de Windows fallará con el siguiente error, porque el proceso de notificaciones no puede determinar qué tipo de usuario autenticar:</span><span class="sxs-lookup"><span data-stu-id="79410-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="79410-p135">Para solucionar el problema para ASMX, todas las llamadas a los métodos de PSI deberían hacerse a una clase derivada que se define para cada servicio web de PSI. La clase derivada también debe usar la clase **SvcLoginWindows.LoginWindows** para obtener una cookie para la clase de servicio de PSI derivada. En el siguiente ejemplo, la clase **ProjectDerived** deriva de la clase **SvcProject.Project**. La clase derivada agrega la propiedad **EnforceWindowsAuth** y sobrescribe el encabezado de solicitud web para todas las llamadas a un método en la clase **Project**. Si la propiedad **EnforceWindowsAuth** es **true**, el método **GetWebRequest** agrega un encabezado que deshabilita la autenticación de formularios. Si **EnforceWindowsAuth** es **false**, se puede continuar con la autenticación de formularios.</span><span class="sxs-lookup"><span data-stu-id="79410-p135">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service. The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class. In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class. The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class. If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication. If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="79410-p136">Para usar la siguiente muestra **ASMXLogon_MultiAuth**, cree una aplicación de consola, siga los pasos en [Crear la aplicación y agregar una referencia de servicio web](#pj15_PrerequisitesASMX_Configure), y después agregue el archivo de proxy wsdl.LoginWindows.cs y el archivo de proxy wsdl.Project.cs. El método **Main** crea la instancia **project** de la clase **ProjectDerived**. La muestra debe usar la clase derivada **LoginWindowsDerived** para obtener un objeto **CookieContainer** para la propiedad **project.CookieContainer**, que distingue la autenticación de formularios y la autenticación de Windows. El objeto **project** puede usarse después para hacer llamadas a cualquier método en la clase **SvcProject.Project**.</span><span class="sxs-lookup"><span data-stu-id="79410-p136">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file. The **Main** method creates the **project** instance of the **ProjectDerived** class. The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication. The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="79410-p137">El servicio **LoginWindows** es necesario solo para aplicaciones de ASMX en un entorno de autenticación múltiple. En la muestra **ASMXLogon_MultiAuth**, el método **GetLogonCookie** obtiene una cookie para el objeto **loginWindows**. La propiedad **project.CookieContainer** se establece en el valor **loginWindows.CookieContainer**.</span><span class="sxs-lookup"><span data-stu-id="79410-p137">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment. In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object. The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

<span data-ttu-id="79410-p138">Las aplicaciones que se inician en un entorno de autenticación múltiple necesitan el uso de la clase derivada **LoginWindows** y la realización de llamadas de PSI con un encabezado de solicitud web que deshabilita la autenticación de formularios. Si Project Server usa solo autenticación de notificaciones, no es necesario derivar un clase que agrega un encabezado de solicitud web. El ejemplo anterior se usa en ambos entornos.</span><span class="sxs-lookup"><span data-stu-id="79410-p138">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment. If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header. The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="79410-266">La solución de una aplicación basada en WCF es diferente.</span><span class="sxs-lookup"><span data-stu-id="79410-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="79410-267">Para obtener más información, vea la sección *Using multiple authentication* en [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="79410-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="79410-268">Modificar los valores de constantes genéricas</span><span class="sxs-lookup"><span data-stu-id="79410-268">Changing the values of generic constants</span></span>
<span data-ttu-id="79410-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span></span>

<span data-ttu-id="79410-270">La mayoría de las muestras tienen una o más variables que necesita actualizar para que la muestra funcione adecuadamente en el entorno.</span><span class="sxs-lookup"><span data-stu-id="79410-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="79410-271">En el siguiente ejemplo, si tiene SSL instalado, use el protocolo HTTPS en lugar del protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="79410-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="79410-272">Reemplace  _ServerName_ por el nombre del servidor que está usando.</span><span class="sxs-lookup"><span data-stu-id="79410-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="79410-273">Reemplace _ProjectServerName por_ el nombre del directorio virtual del sitio Project servidor, como PWA.</span><span class="sxs-lookup"><span data-stu-id="79410-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="79410-274">Cualquier otra variable que deba cambiar o cualquier otro requisito previo se indica en la parte superior del ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="79410-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="79410-275">Comprobar los resultados</span><span class="sxs-lookup"><span data-stu-id="79410-275">Verifying the results</span></span>
<span data-ttu-id="79410-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span></span>

<span data-ttu-id="79410-277">Obtener e interpretar los resultados de una muestra de código no es siempre sencillo.</span><span class="sxs-lookup"><span data-stu-id="79410-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="79410-278">Por ejemplo, si crea un proyecto, debe publicar el proyecto antes de que pueda aparecer en la página del Centro de Project en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="79410-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="79410-279">Puede verificar los resultados de muestra de código de varias formas, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79410-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="79410-280">Use el Project Profesional 2013 para abrir el proyecto desde el equipo Project Server y ver los elementos que desee.</span><span class="sxs-lookup"><span data-stu-id="79410-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="79410-281">Ver proyectos publicados en la página Project centro de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="79410-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="79410-282">Ver el registro de cola en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="79410-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="79410-283">Abra la página Servidor Configuración (elija el icono Configuración en la esquina superior derecha) y, **a** continuación, elija **Mis** trabajos en cola en la sección **Personal Configuración** ( `https://ServerName/ProjectServerName/MyJobs.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="79410-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="79410-284">En la lista desplegable **Vista**, puede ordenar por el estado de trabajo.</span><span class="sxs-lookup"><span data-stu-id="79410-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="79410-285">El estado predeterminado **Trabajos fallidos y en progreso en la última semana**.</span><span class="sxs-lookup"><span data-stu-id="79410-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="79410-286">Use la página Servidor Configuración en Project Web App ( ) para administrar todos los trabajos en cola y eliminar o forzar la `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` entrada de objetos empresariales.</span><span class="sxs-lookup"><span data-stu-id="79410-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="79410-287">Asegúrese de tener los permisos administrativos para obtener acceso a aquellos enlaces de la página Configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="79410-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="79410-p144">Use **Microsoft SQL Server Management Studio** para usar una consulta en una tabla de una base de datos de Project. Por ejemplo, use la siguiente consulta para seleccionar las 200 filas superiores de la tabla pub.MSP_WORKFLOW_STAGE_PDPS para mostrar información sobre las páginas de detalles de proyectos (PDP) en etapas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="79410-p144">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database. For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a><span data-ttu-id="79410-290">Limpieza</span><span class="sxs-lookup"><span data-stu-id="79410-290">Cleaning up</span></span>
<span data-ttu-id="79410-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span></span>

<span data-ttu-id="79410-292">Después de probar algunas muestras de código, existen configuraciones y objetos de empresa que deberían eliminarse o restablecerse.</span><span class="sxs-lookup"><span data-stu-id="79410-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="79410-293">Puede usar la página Server Configuración en Project Web App para administrar datos de empresa ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ).</span><span class="sxs-lookup"><span data-stu-id="79410-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="79410-294">Los vínculos en la página Configuración de servidor le permiten eliminar elementos viejos, forzar la protección de proyectos, administrar la cola de trabajo para todos los usuarios y hacer otras tareas administrativas.</span><span class="sxs-lookup"><span data-stu-id="79410-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="79410-295">A continuación aparecen algunos de los vínculos de la página Configuración de servidor que puede usar para actividades típicas de limpieza después de usar muestras de código:</span><span class="sxs-lookup"><span data-stu-id="79410-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="79410-296">**Campos personalizados de empresa y tablas de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="79410-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="79410-297">**Administrar trabajos en cola**</span><span class="sxs-lookup"><span data-stu-id="79410-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="79410-298">**Eliminación de objetos de empresa**</span><span class="sxs-lookup"><span data-stu-id="79410-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="79410-299">**Forzar protección de objetos de la empresa**</span><span class="sxs-lookup"><span data-stu-id="79410-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="79410-300">**Tipos de proyecto empresarial**</span><span class="sxs-lookup"><span data-stu-id="79410-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="79410-301">**Fases de flujo de trabajo**</span><span class="sxs-lookup"><span data-stu-id="79410-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="79410-302">**Etapas de flujo de trabajo**</span><span class="sxs-lookup"><span data-stu-id="79410-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="79410-303">**Páginas de detalles del proyecto**</span><span class="sxs-lookup"><span data-stu-id="79410-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="79410-304">**Períodos de presentación de informes de horas**</span><span class="sxs-lookup"><span data-stu-id="79410-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="79410-305">**Configuración y valores predeterminados del parte de horas**</span><span class="sxs-lookup"><span data-stu-id="79410-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="79410-306">**Clasificaciones de línea**</span><span class="sxs-lookup"><span data-stu-id="79410-306">**Line Classifications**</span></span>
    
<span data-ttu-id="79410-307">SharePoint Server 2013 administra la configuración adicional para cada instancia de Project Web App, en lugar de una página Project web app server Configuración específico.</span><span class="sxs-lookup"><span data-stu-id="79410-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="79410-308">En la aplicación de Administración central de SharePoint, elija  **Aplicación general Configuración**, elija Administrar en Project **Server Configuración** y, a continuación, elija la instancia de Project Web App en la lista desplegable de la página Servidor Configuración.</span><span class="sxs-lookup"><span data-stu-id="79410-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="79410-309">Por ejemplo, elija Controladores de eventos **del** lado servidor para agregar o eliminar controladores de eventos para la instancia Project Web App seleccionada.</span><span class="sxs-lookup"><span data-stu-id="79410-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79410-310">Vea también</span><span class="sxs-lookup"><span data-stu-id="79410-310">See also</span></span>
<span data-ttu-id="79410-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="79410-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span></span>

- [<span data-ttu-id="79410-312">Requisitos previos de muestras de código basadas en WCF en Project</span><span class="sxs-lookup"><span data-stu-id="79410-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="79410-313">Usar suplantación con WCF</span><span class="sxs-lookup"><span data-stu-id="79410-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="79410-314">Descripción general de referencia de PSI de Project</span><span class="sxs-lookup"><span data-stu-id="79410-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="79410-315">Centro para desarrolladores de SharePoint</span><span class="sxs-lookup"><span data-stu-id="79410-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

