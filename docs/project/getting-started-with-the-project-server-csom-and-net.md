---
title: Comenzar con CSOM y .NET de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Puede usar el modelo de objetos de cliente (COM) de Project Server 2013 para desarrollar soluciones de Project Online y local con .NET Framework 4. En este artículo se describe cómo crear una aplicación de consola que usa el CSOM para crear y publicar proyectos. Después de publicar un proyecto, la aplicación espera a que el servicio de cola de Project Server a fin con la acción de publicación y, a continuación, enumera los proyectos publicados.
ms.openlocfilehash: 1815122ce824fcd2f9b8c9119346ca02c720ae89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821327"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a><span data-ttu-id="0c5e3-105">Comenzar con CSOM y .NET de Project Server</span><span class="sxs-lookup"><span data-stu-id="0c5e3-105">Getting started with the Project Server CSOM and .NET</span></span>

<span data-ttu-id="0c5e3-106">Puede usar el modelo de objetos de cliente (COM) de Project Server 2013 para desarrollar soluciones de Project Online y local con .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-106">You can use the Project Server 2013 client-side object model (CSOM) to develop Project Online and on-premises solutions with the .NET Framework 4.</span></span> <span data-ttu-id="0c5e3-107">En este artículo se describe cómo crear una aplicación de consola que usa el CSOM para crear y publicar proyectos.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-107">This article describes how to create a console application that uses the CSOM to create and publish projects.</span></span> <span data-ttu-id="0c5e3-108">Después de publicar un proyecto, la aplicación espera a que el servicio de cola de Project Server a fin con la acción de publicación y, a continuación, enumera los proyectos publicados.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-108">After publishing a project, the application waits for the Project Server Queue Service to finish with the publish action, and then lists the published projects.</span></span>
  
<span data-ttu-id="0c5e3-109">Para obtener una introducción general a CSOM de Project Server, vea [actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="0c5e3-109">For a general introduction to the Project Server CSOM, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span> <span data-ttu-id="0c5e3-110">Para los temas de referencia en el espacio de nombres CSOM, vea [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-110">For reference topics in the CSOM namespace, see [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
## <a name="creating-a-csom-project-in-visual-studio"></a><span data-ttu-id="0c5e3-111">Crear un proyecto CSOM en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c5e3-111">Creating a CSOM project in Visual Studio</span></span>
<span data-ttu-id="0c5e3-112"><a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-112"></span></span>

<span data-ttu-id="0c5e3-113">Puede usar Visual Studio 2010 o Visual Studio 2012 para desarrollar soluciones que usen el CSOM de Project Server.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-113">You can use Visual Studio 2010 or Visual Studio 2012 to develop solutions that use the Project Server CSOM.</span></span> <span data-ttu-id="0c5e3-114">CSOM de Project Server incluye tres ensamblados para el desarrollo de aplicaciones cliente, aplicaciones de Microsoft Silverlight y Windows Phone 8 aplicaciones mediante el uso de .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-114">The Project Server CSOM includes three assemblies for development of client applications, Microsoft Silverlight applications, and Windows Phone 8 applications by using the .NET Framework 4.</span></span> <span data-ttu-id="0c5e3-115">El CSOM también incluye un archivo JavaScript para el desarrollo de aplicaciones web, tal como se describe en [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-115">The CSOM also includes a JavaScript file for development of web applications, as described in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
<span data-ttu-id="0c5e3-116">Puede copiar el ensamblado CSOM que necesita desde el equipo de Project Server o desde la descarga del SDK de Project 2013 en un equipo de desarrollo remoto.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-116">You can copy the CSOM assembly that you need from the Project Server computer or from the Project 2013 SDK download to a remote development computer.</span></span> <span data-ttu-id="0c5e3-117">La aplicación de consola **QueueCreateProject** que se describe en este tema no es una aplicación de Silverlight o una aplicación de Windows Phone 8, por lo que necesita el ensamblado Microsoft.ProjectServer.Client.dll.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-117">The **QueueCreateProject** console application that is described in this topic is not a Silverlight application or a Windows Phone 8 application, so you need the Microsoft.ProjectServer.Client.dll assembly.</span></span> <span data-ttu-id="0c5e3-118">Debido a que el CSOM es independiente de la basados en ASMX o WCF Project Server Interface (PSI), no es necesario que establecer referencias de servicio de la PSI o usar el espacio de nombres **Microsoft.Office.Project.Server.Library** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-118">Because the CSOM is independent of the WCF-based or ASMX-based Project Server Interface (PSI), you do not have to set service references for the PSI or use the **Microsoft.Office.Project.Server.Library** namespace.</span></span> 
  
<span data-ttu-id="0c5e3-119">La aplicación **QueueCreateProject** utiliza los argumentos de línea de comandos para el nombre del proyecto para crear y para el límite de tiempo de espera de cola.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-119">The **QueueCreateProject** application uses command-line arguments for the name of the project to create and for the queue timeout limit.</span></span> <span data-ttu-id="0c5e3-120">En el procedimiento 1, cree la aplicación de consola básica, agregar una rutina para analizar la línea de comandos y agregar un mensaje de uso si hay errores en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-120">In Procedure 1, you create the basic console application, add a routine to parse the command line, and add a usage message if there are errors in the command line.</span></span> 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a><span data-ttu-id="0c5e3-p107">Procedimiento 1. Para crear un proyecto CSOM en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p107">Procedure 1. To create a CSOM project in Visual Studio</span></span>

1. <span data-ttu-id="0c5e3-123">Copie el ensamblado Microsoft.ProjectServer.Client.dll desde el `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` carpeta al equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-123">Copy the Microsoft.ProjectServer.Client.dll assembly from the  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` folder to your development computer.</span></span> <span data-ttu-id="0c5e3-124">Copie el ensamblado en una carpeta conveniente para otros Project Server y los ensamblados de referencia de SharePoint que va a usar, tales como `C:\Project\Assemblies`.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-124">Copy the assembly to a convenient folder for other Project Server and SharePoint reference assemblies that you will use, such as  `C:\Project\Assemblies`.</span></span>
    
2. <span data-ttu-id="0c5e3-p109">Copie el ensamblado de Microsoft.SharePoint.Client.dll y el de Microsoft.SharePoint.Client.Runtime.dll de la misma carpeta de origen hasta su equipo de desarrollo. El ensamblado de Microsoft.ProjectServer.Client.dll tiene dependencias en los ensamblados de SharePoint relacionados.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p109">Copy the Microsoft.SharePoint.Client.dll assembly and the Microsoft.SharePoint.Client.Runtime.dll assembly from the same source folder to your development computer. The Microsoft.ProjectServer.Client.dll assembly has dependencies on the related SharePoint assemblies.</span></span>
    
3. <span data-ttu-id="0c5e3-127">En Visual Studio, cree una aplicación de consola de Windows y establece el marco de destino en .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-127">In Visual Studio, create a Windows console application, and set the target framework to .NET Framework 4.</span></span> <span data-ttu-id="0c5e3-128">Por ejemplo, nombre de la aplicación QueueCreateProject.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-128">For example, name the application QueueCreateProject.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="0c5e3-129">En caso de olvidar establecer el destino correcto, una vez que Visual Studio crea el proyecto, abra **Las propiedades de QueueCreateProject** en el menú **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-129">If you forget to set the correct target, after Visual Studio creates the project, open **QueueCreateProject Properties** in the **Project** menu.</span></span> <span data-ttu-id="0c5e3-130">En la ficha **aplicación** , en la lista desplegable de **.NET framework de destino** , elija **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-130">On the **Application** tab, in the **Target framework** drop-down list, choose **.NET Framework 4**.</span></span> <span data-ttu-id="0c5e3-131">No use el **Perfil de cliente de .NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-131">Do not use the **.NET Framework 4 Client Profile**.</span></span> 
  
4. <span data-ttu-id="0c5e3-132">En Solution Explorer, defina las referencias para los siguientes ensamblados:</span><span class="sxs-lookup"><span data-stu-id="0c5e3-132">In Solution Explorer, set references to the following assemblies:</span></span>
    
   - <span data-ttu-id="0c5e3-133">Microsoft.Project.Server.Client.dll</span><span class="sxs-lookup"><span data-stu-id="0c5e3-133">Microsoft.ProjectServer.Client.dll</span></span>
   - <span data-ttu-id="0c5e3-134">Microsoft.SharePoint.Client.dll</span><span class="sxs-lookup"><span data-stu-id="0c5e3-134">Microsoft.SharePoint.Client.dll</span></span>
   - <span data-ttu-id="0c5e3-135">Microsoft.SharePoint.Client.Runtime.dll</span><span class="sxs-lookup"><span data-stu-id="0c5e3-135">Microsoft.SharePoint.Client.Runtime.dll</span></span>
    
5. <span data-ttu-id="0c5e3-136">En el archivo Program.cs, modifique la `using` instrucciones, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-136">In the Program.cs file, edit the  `using` statements, as follows.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. <span data-ttu-id="0c5e3-p112">Agregue métodos para analizar los argumentos de la línea de comandos y el número de segundos del tiempo de espera de la cola, muestre la información de uso y salga de la aplicación. Reemplace el cuerpo principal del código del archivo Program.cs con el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p112">Add methods to parse the command-line arguments for the project name and the number of seconds for queue timeout, show usage information, and exit the application. Replace the main body of code in the Program.cs file with the following code.</span></span>
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a><span data-ttu-id="0c5e3-139">Obtener el contexto del proyecto</span><span class="sxs-lookup"><span data-stu-id="0c5e3-139">Getting the project context</span></span>
<span data-ttu-id="0c5e3-140"><a name="pj15_GettingStartedCSOM_GettingContext"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-140"></span></span>

<span data-ttu-id="0c5e3-141">Desarrollo de CSOM requiere el objeto de **ProjectContext** que se inicialice con la dirección URL de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-141">CSOM development requires the **ProjectContext** object to be initialized with the Project Web App URL.</span></span> <span data-ttu-id="0c5e3-142">El código en el procedimiento 2 usa la constante **pwaPath** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-142">The code in Procedure 2 uses the **pwaPath** constant.</span></span> <span data-ttu-id="0c5e3-143">Si piensa usar la aplicación para varias instancias de Project Web App, podría hacer que **pwaPath** una variable y agregar otro argumento de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-143">If you plan to use the application for multiple instances of Project Web App, you could make **pwaPath** a variable and add another command-line argument.</span></span> 
  
### <a name="procedure-2-to-get-the-project-context"></a><span data-ttu-id="0c5e3-p114">Procedimiento 2. Para obtener el contexto del proyecto</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p114">Procedure 2. To get the project context</span></span>

1. <span data-ttu-id="0c5e3-146">Agregar variables que va a usar la aplicación **QueueCreateProject** y constantes de clase de **programa** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-146">Add **Program** class constants and variables that the **QueueCreateProject** application will use.</span></span> <span data-ttu-id="0c5e3-147">Además de la dirección URL de Project Web App, la aplicación usa el nombre del tipo de proyecto de empresa (EPT) de forma predeterminada, el nombre del proyecto que se va a crear y un tiempo de espera máximo de la cola en segundos.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-147">In addition to the Project Web App URL, the application uses the name of the default enterprise project type (EPT), the name of the project to create, and a maximum queue timeout in seconds.</span></span> <span data-ttu-id="0c5e3-148">En este caso, la variable **timeoutSeconds** permite probar cómo distintos valores para el tiempo de espera afectan a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-148">In this case, the **timeoutSeconds** variable enables you to test how various values for the timeout affect the application.</span></span> <span data-ttu-id="0c5e3-149">El objeto de **ProjectContext** es el objeto principal para obtener acceso a la CSOM.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-149">The **ProjectContext** object is the primary object for access to the CSOM.</span></span> 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. <span data-ttu-id="0c5e3-150">Reemplace el `/* Add calls to methods here to get the project context and create a project. */` comentario con el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-150">Replace the  `/* Add calls to methods here to get the project context and create a project. */` comment with the following code.</span></span> <span data-ttu-id="0c5e3-151">El objeto **Microsoft.ProjectServer.Client.ProjectContext** se inicializa con la dirección URL de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-151">The **Microsoft.ProjectServer.Client.ProjectContext** object is initialized with the Project Web App URL.</span></span> <span data-ttu-id="0c5e3-152">El método **CreateTestProject** y el método **ListPublishedProjects** se muestran en el procedimiento 4 y 5 del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-152">The **CreateTestProject** method and the **ListPublishedProjects** method are shown in Procedure 4 and Procedure 5.</span></span> 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a><span data-ttu-id="0c5e3-153">Obtener un tipo de proyecto empresarial</span><span class="sxs-lookup"><span data-stu-id="0c5e3-153">Getting an enterprise project type</span></span>
<span data-ttu-id="0c5e3-154"><a name="pj15_GettingStartedCSOM_GettingEPT"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-154"></span></span>

<span data-ttu-id="0c5e3-155">La aplicación de ejemplo **QueueCreateProject** selecciona explícitamente el EPT del proyecto de empresa, para mostrar cómo una aplicación puede seleccionar la plantilla EPT para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-155">The **QueueCreateProject** sample application explicitly selects the Enterprise Project EPT, to show how an application can select the EPT for a project.</span></span> <span data-ttu-id="0c5e3-156">Si la información de creación del proyecto no especifica el GUID EPT, una aplicación usaría el valor predeterminado EPT.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-156">If the project creation information does not specify the EPT GUID, an application would use the default EPT.</span></span> <span data-ttu-id="0c5e3-157">El método **GetEptUid** se usa en el método **CreateTestProject** que se describe en el procedimiento 4.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-157">The **GetEptUid** method is used by the **CreateTestProject** method that is described in Procedure 4.</span></span> 
  
<span data-ttu-id="0c5e3-158">El método **GetEptUid** consulta el objeto de **ProjectContext** para la colección de **EnterpriseProjectTypes** donde el nombre EPT coincide con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-158">The **GetEptUid** method queries the **ProjectContext** object for the collection of **EnterpriseProjectTypes** where the EPT name equals the specified name.</span></span> <span data-ttu-id="0c5e3-159">Después de ejecutar la consulta, la variable **eptUid** se establece en el GUID del primer objeto de la colección de **eptList** **EnterpriseProjectType** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-159">After executing the query, the **eptUid** variable is set to the GUID of the first **EnterpriseProjectType** object in the **eptList** collection.</span></span> <span data-ttu-id="0c5e3-160">Debido a que los nombres de etp son únicos, hay un solo objeto **EnterpriseProjectType** que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-160">Because EPT names are unique, there is only one **EnterpriseProjectType** object that has the specified name.</span></span> 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a><span data-ttu-id="0c5e3-p119">Procedimiento 3. Para obtener el GUID de un tipo de proyecto empresarial (EPT) para un nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p119">Procedure 3. To get the GUID of an EPT for a new project</span></span>

- <span data-ttu-id="0c5e3-163">Agregue el método **GetEptUid** a la clase **Program** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-163">Add the **GetEptUid** method to the **Program** class.</span></span> 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

<span data-ttu-id="0c5e3-164">Hay varias maneras para encontrar el GUID de EPT.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-164">There are several ways to find the EPT GUID.</span></span> <span data-ttu-id="0c5e3-165">La consulta que se muestra en el método **GetEptUid** es eficaz debido a que descarga sólo en el objeto **EnterpriseProjectType** uno que coincida con el nombre EPT.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-165">The query shown in the **GetEptUid** method is efficient because it downloads only the one **EnterpriseProjectType** object that matches the EPT name.</span></span> <span data-ttu-id="0c5e3-166">La siguiente rutina alternativa es menos eficiente, porque descarga la lista completa de EPT a la aplicación cliente e itera a través de la lista.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-166">The following alternate routine is less efficient, because it downloads the complete list of EPTs to the client application and iterates through the list.</span></span> 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

<span data-ttu-id="0c5e3-167">La siguiente rutina utiliza una expresión de consulta y lambda LINQ para seleccionar el objeto etp, pero sigue descargando todos los objetos **EnterpriseProjectType** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-167">The following routine uses a LINQ query and lambda expression to select the EPT object, but still downloads all of the **EnterpriseProjectType** objects.</span></span> 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a><span data-ttu-id="0c5e3-168">Definir la información de creación y publicar el objeto</span><span class="sxs-lookup"><span data-stu-id="0c5e3-168">Setting the creation information and publishing the project</span></span>
<span data-ttu-id="0c5e3-169"><a name="pj15_GettingStartedCSOM_ProjectCreation"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-169"></span></span>

<span data-ttu-id="0c5e3-170">El método **CreateTestProject** crea un objeto **ProjectCreationInformation** y especifica la información que se requiere para crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-170">The **CreateTestProject** method creates a **ProjectCreationInformation** object and specifies the information that is required to create a project.</span></span> <span data-ttu-id="0c5e3-171">El GUID de proyecto y el nombre son necesarios; la fecha de inicio, la descripción del proyecto y el GUID de EPT son opcionales.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-171">The project GUID and name are required; the start date, project description, and EPT GUID are optional.</span></span> 
  
<span data-ttu-id="0c5e3-172">Después de establecer las propiedades del proyecto nuevo, el método **Projects.Add** agrega el proyecto a la colección de **proyectos** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-172">After setting the new project properties, the **Projects.Add** method adds the project to the **Projects** collection.</span></span> <span data-ttu-id="0c5e3-173">Para guardar y publicar el proyecto, debe llamar al método **Projects.Update** para enviar un mensaje a la cola de Project Server y crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-173">To save and publish the project, you must call the **Projects.Update** method to send a message to the Project Server queue and create the project.</span></span> 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a><span data-ttu-id="0c5e3-p123">Procedimiento 4. Para definir las nuevas propiedades del proyecto, crear el proyecto y publicarlo.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p123">Procedure 4. To set the new project properties, create the project, and publish the project</span></span>

1. <span data-ttu-id="0c5e3-176">Agregue el método **CreateTestProject** a la clase **Program** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-176">Add the **CreateTestProject** method to the **Program** class.</span></span> <span data-ttu-id="0c5e3-177">El siguiente código crea y publica un proyecto, pero no espera a que el trabajo en cola para llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-177">The following code creates and publishes a project, but does not wait for the queue job to complete.</span></span> 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. <span data-ttu-id="0c5e3-178">Reemplace el `/* Add code here to wait for the queue. */` comentario con el siguiente código que se debe esperar para el trabajo en cola.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-178">Replace the  `/* Add code here to wait for the queue. */` comment with the following code to wait for the queue job.</span></span> <span data-ttu-id="0c5e3-179">La rutina espera a que un máximo del número de segundos especificado **timeoutSeconds** o continúa si se realiza el trabajo en cola antes del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-179">The routine waits a maximum of the specified **timeoutSeconds** number of seconds, or proceeds if the queue job completes before the timeout.</span></span> <span data-ttu-id="0c5e3-180">Para los Estados de trabajo de cola posibles, consulte [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-180">For possible queue job states, see [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span></span> 
    
   <span data-ttu-id="0c5e3-181">Llamar al método **Load** y el método **ExecuteQuery** para el objeto **QueueJob** es opcional.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-181">Calling the **Load** method and the **ExecuteQuery** method for the **QueueJob** object is optional.</span></span> <span data-ttu-id="0c5e3-182">Si no se ha inicializado el objeto **QueueJob** cuando se llama al método **WaitForQueue** , Project Serverlo inicializa.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-182">If the **QueueJob** object is not initialized when you call the **WaitForQueue** method, Project Server initializes it.</span></span> 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a><span data-ttu-id="0c5e3-183">Mostrar los proyectos publicados</span><span class="sxs-lookup"><span data-stu-id="0c5e3-183">Listing the published projects</span></span>
<span data-ttu-id="0c5e3-184"><a name="pj15_GettingStartedCSOM_ListingPublished"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-184"></span></span>

<span data-ttu-id="0c5e3-185">El método **ListPublishedProjects** Obtiene la colección de todos los proyectos que se publican en Project Web App.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-185">The **ListPublishedProjects** method gets the collection of all projects that are published in Project Web App.</span></span> <span data-ttu-id="0c5e3-186">Si el trabajo en cola que crea un proyecto en el procedimiento 4 no se completa correctamente o el tiempo de espera, no se incluye el nuevo proyecto en la colección de **proyectos** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-186">If the queue job that creates a project in Procedure 4 does not complete successfully or times out, the new project is not included in the **Projects** collection.</span></span> 
  
### <a name="procedure-5-to-list-the-published-projects"></a><span data-ttu-id="0c5e3-p128">Procedimiento 5. Mostrar los proyectos publicados</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p128">Procedure 5. To list the published projects</span></span>

1. <span data-ttu-id="0c5e3-189">Agregue el método **ListPublishedProjects** a la clase **Program** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-189">Add the **ListPublishedProjects** method to the **Program** class.</span></span> 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. <span data-ttu-id="0c5e3-190">Establezca el valor correcto para la dirección URL de Project Web App, compile la aplicación **QueueCreateProject** y, a continuación, pruebe la aplicación como en el procedimiento 6.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-190">Set the correct value for your Project Web App URL, compile the **QueueCreateProject** application, and then test the application as in Procedure 6.</span></span> 
    
## <a name="testing-the-queuecreateproject-application"></a><span data-ttu-id="0c5e3-191">Probar la aplicación QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="0c5e3-191">Testing the QueueCreateProject application</span></span>
<span data-ttu-id="0c5e3-192"><a name="pj15_GettingStartedCSOM_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-192"></span></span>

<span data-ttu-id="0c5e3-193">Cuando se ejecuta en primer lugar la aplicación **QueueCreateProject** en una instancia de prueba de Project Web App, especialmente si Project Server está instalado en una máquina virtual, la aplicación puede requerir más tiempo en comparación con el tiempo de espera predeterminado de diez segundos.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-193">When you first run the **QueueCreateProject** application on a test instance of Project Web App, especially if Project Server is installed on a virtual machine, the application may require more time to run than the default queue timeout of ten seconds.</span></span> 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a><span data-ttu-id="0c5e3-p129">Procedimiento 6. Probar la aplicación QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p129">Procedure 6. To test the QueueCreateProject application</span></span>

1. <span data-ttu-id="0c5e3-196">Abra la ventana de **Propiedades de QueueCreateProject** , seleccione la ficha **Depurar** y, a continuación, agregue los argumentos de línea de comandos siguientes en la sección **Opciones de inicio** :`-n "Test proj 1" -t 20`</span><span class="sxs-lookup"><span data-stu-id="0c5e3-196">Open the **QueueCreateProject Properties** window, select the **Debug** tab, and then add the following command-line arguments in the **Start Options** section:  `-n "Test proj 1" -t 20`</span></span>
    
   <span data-ttu-id="0c5e3-197">Ejecutar la aplicación (por ejemplo, presione **F5**).</span><span class="sxs-lookup"><span data-stu-id="0c5e3-197">Run the application (for example, press **F5**).</span></span> <span data-ttu-id="0c5e3-198">Si el valor de tiempo de espera es suficiente, la aplicación muestra el siguiente resultado (si existen otros proyectos publicados en la instancia de Project Web App, también se mostrarán):</span><span class="sxs-lookup"><span data-stu-id="0c5e3-198">If the timeout value is long enough, the application shows the following output (if other published projects exist in your Project Web App instance, they will also be shown):</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. <span data-ttu-id="0c5e3-199">Ejecute otra prueba con los siguientes argumentos de línea de comandos, para usar el tiempo de espera de cola de 10 segundos de forma predeterminada:`-n "Test proj 1"`</span><span class="sxs-lookup"><span data-stu-id="0c5e3-199">Run another test with the following command-line arguments, to use the default 10-second queue timeout: `-n "Test proj 1"`</span></span>
    
   <span data-ttu-id="0c5e3-200">Dado que ya existe la prueba Test proj 1, la aplicación muestra el siguiente resultado</span><span class="sxs-lookup"><span data-stu-id="0c5e3-200">Because Test proj 1 already exists, the application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. <span data-ttu-id="0c5e3-201">Ejecute otra prueba con los siguientes argumentos de línea de comandos, para usar el tiempo de espera de cola de 10 segundos de forma predeterminada:`-n "Test proj 2"`</span><span class="sxs-lookup"><span data-stu-id="0c5e3-201">Run another test with the following command-line arguments, to use the default 10-second queue timeout:  `-n "Test proj 2"`</span></span>
    
   <span data-ttu-id="0c5e3-202">La aplicación **QueueCreateProject** crea y publica el proyecto denominado Test proj 2.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-202">The **QueueCreateProject** application creates and publishes the project named Test proj 2.</span></span> 
    
4. <span data-ttu-id="0c5e3-203">Ejecute otra prueba con los siguientes argumentos de línea de comandos y establecer el tiempo de espera sea demasiado corto para el trabajo en cola para finalizar:`-n "Test proj 3" -t 1`</span><span class="sxs-lookup"><span data-stu-id="0c5e3-203">Run another test with the following command-line arguments, and set the timeout to be too short for the queue job to finish:  `-n "Test proj 3" -t 1`</span></span>
    
   <span data-ttu-id="0c5e3-p131">Dado que el tiempo de espera en cola es demasiado corto, no se crea el proyecto. La aplicación muestra el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-p131">Because the queue timeout is too short, the project is not created. The application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. <span data-ttu-id="0c5e3-206">Modifique el código para que la aplicación no espera a que el trabajo en cola.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-206">Modify the code so that the application does not wait for the queue job.</span></span> <span data-ttu-id="0c5e3-207">Por ejemplo, quite los comentarios en el código que debe esperar para la cola, excepto para la `projCreated = true` de línea, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-207">For example, comment out the code that waits for the queue, except for the  `projCreated = true` line, as follows.</span></span> 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. <span data-ttu-id="0c5e3-208">Volver a compilar la aplicación y ejecute otra prueba con los argumentos de línea de comandos siguientes:`-n "Test proj 4"`</span><span class="sxs-lookup"><span data-stu-id="0c5e3-208">Recompile the application and run another test with the following command-line arguments:  `-n "Test proj 4"`</span></span>
    
   <span data-ttu-id="0c5e3-209">Debido a que la rutina **WaitForQueue** está convertida en comentario, la aplicación no usa el valor de tiempo de espera predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-209">Because the **WaitForQueue** routine is commented out, the application does not use the default timeout value.</span></span> <span data-ttu-id="0c5e3-210">A pesar de que la aplicación no esperar la cola, puede mostrar Test proj 4, si la acción de publicación en Project Server es lo suficientemente rápida.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-210">Even though the application does not wait for the queue, it may show Test proj 4, if the publish action in Project Server is fast enough.</span></span> 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

<span data-ttu-id="0c5e3-211">Actualizar la página Centro de proyectos en Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), para mostrar los proyectos publicados.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-211">Refresh the Project Center page in Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), to show the published projects.</span></span> <span data-ttu-id="0c5e3-212">La siguiente ilustración muestra que se publican los proyectos de prueba.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-212">The following figure shows that the test projects are published.</span></span>

<span data-ttu-id="0c5e3-213">**Comprobación de los proyectos publicados en Project Web App**</span><span class="sxs-lookup"><span data-stu-id="0c5e3-213">**Checking the published projects in Project Web App**</span></span>

<span data-ttu-id="0c5e3-214">![Comprobación de los proyectos publicados en Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Comprobación de los proyectos publicados en Project Web App")</span><span class="sxs-lookup"><span data-stu-id="0c5e3-214">![Checking the published projects in Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Checking the published projects in Project Web App")</span></span>
  
<span data-ttu-id="0c5e3-215">La aplicación de ejemplo **QueueCreateProject** muestra un ejemplo típico de cómo crear una entidad de proyecto con el CSOM mediante el uso de la clase **ProjectCreationInformation** , cómo agregar el proyecto a la colección publicada, cómo esperar un trabajo en cola por mediante el método de **WaitForQueue** y cómo enumerar la colección de proyectos publicados.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-215">The **QueueCreateProject** sample application shows a typical example of how to create a project entity with the CSOM by using the **ProjectCreationInformation** class, how to add the project to the published collection, how to wait for a queue job by using the **WaitForQueue** method, and how to enumerate the collection of published projects.</span></span> 
  
## <a name="complete-code-example"></a><span data-ttu-id="0c5e3-216">Ejemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="0c5e3-216">Complete code example</span></span>
<span data-ttu-id="0c5e3-217"><a name="pj15_GettingStartedCSOM_CompleteCode"> </a></span><span class="sxs-lookup"><span data-stu-id="0c5e3-217"></span></span>

<span data-ttu-id="0c5e3-218">El siguiente es el código completo para la aplicación de ejemplo **QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="0c5e3-218">The following is the complete code for the **QueueCreateProject** sample application.</span></span> <span data-ttu-id="0c5e3-219">La referencia de clase [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) también incluye el código de este tema.</span><span class="sxs-lookup"><span data-stu-id="0c5e3-219">The [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) class reference also includes the code in this topic.</span></span> 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0c5e3-220">Ver también</span><span class="sxs-lookup"><span data-stu-id="0c5e3-220">See also</span></span>

- [<span data-ttu-id="0c5e3-221">Actualizaciones para desarrolladores en Project 2013</span><span class="sxs-lookup"><span data-stu-id="0c5e3-221">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md) 
- [<span data-ttu-id="0c5e3-222">Modelo de objetos de cliente (COM) de Project 2013</span><span class="sxs-lookup"><span data-stu-id="0c5e3-222">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

