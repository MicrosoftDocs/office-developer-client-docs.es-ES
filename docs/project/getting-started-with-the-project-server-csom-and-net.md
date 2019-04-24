---
title: Introducción a .NET y CSOM de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Puede usar el modelo de objetos del lado cliente (CSOM) de Project Server 2013 para desarrollar soluciones locales y de Project Online con .NET Framework 4. En este artículo, se describe cómo crear una aplicación de consola en la que se usa CSOM para crear y publicar proyectos. Después de publicar un proyecto, la aplicación espera a que Project Server Queue Service termine con la acción de publicación y, después, enumera los proyectos publicados.
localization_priority: Priority
ms.openlocfilehash: b53587ca1959faefdc1b40f08c4adfda4ee11d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360581"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Introducción a .NET y CSOM de Project Server

Puede usar el modelo de objetos del lado cliente (CSOM) de Project Server 2013 para desarrollar soluciones locales y de Project Online con .NET Framework 4. En este artículo, se describe cómo crear una aplicación de consola en la que se usa CSOM para crear y publicar proyectos. Después de publicar un proyecto, la aplicación espera a que Project Server Queue Service termine con la acción de publicación y, después, enumera los proyectos publicados.
  
Para obtener una introducción general del CSOM de Project Server, vea [Actualizaciones para desarrolladores de Project 2013](updates-for-developers-in-project-2013.md). Para obtener temas de referencia en el espacio de nombres del CSOM, vea [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Creación de un proyecto de CSOM en Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Puede usar Visual Studio 2010 o Visual Studio 2012 para desarrollar soluciones en las que se use el CSOM de Project Server. En el CSOM de Project Server se incluyen tres ensamblados para el desarrollo de aplicaciones cliente, de Microsoft Silverlight y de Windows Phone 8 con .NET Framework 4. En el CSOM también se incluye un archivo de JavaScript para el desarrollo de aplicaciones web, como se describe en [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
Puede copiar el ensamblado del CSOM que necesite desde el equipo de Project Server o desde la descarga del SDK de Project 2013 a un equipo de desarrollo remoto. La aplicación de consola **QueueCreateProject** que se describe en este tema no es una aplicación de Silverlight ni de Windows Phone 8, por lo que necesita el ensamblado Microsoft.ProjectServer.Client.dll. Como el CSOM es independiente de la Interfaz de Project Server (PSI) basada en ASMX o WCF, no hay que establecer referencias de servicio para PSI ni usar el espacio de nombres **Microsoft.Office.Project.Server.Library**. 
  
La aplicación **QueueCreateProject** utiliza argumentos de la línea de comandos para crear el nombre del proyecto y para limitar el tiempo de espera de la cola. En el Procedimiento 1, se crea la aplicación de la consola básica, se agrega una rutina para analizar la línea de comandos y se añade un mensaje de uso en caso de que haya errores en la línea de comandos. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Procedimiento 1. Para crear un proyecto de CSOM en Visual Studio

1. Copie el ensamblado Microsoft.ProjectServer.Client.dll desde la carpeta `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` al equipo de desarrollo. Copie el ensamblado en una carpeta adecuada para otros ensamblados de referencia de Project Server y SharePoint que vaya a usar, como `C:\Project\Assemblies`.
    
2. Copie el ensamblado de Microsoft.SharePoint.Client.dll y el de Microsoft.SharePoint.Client.Runtime.dll de la misma carpeta de origen hasta su equipo de desarrollo. El ensamblado de Microsoft.ProjectServer.Client.dll tiene dependencias en los ensamblados de SharePoint relacionados.
    
3. En Visual Studio, cree una aplicación de consola de Windows y establezca el marco de destino en .NET Framework 4. Por ejemplo, asigne el nombre QueueCreateProject a la aplicación.
    
   > [!NOTE]
   > Si olvida definir el objetivo correcto, una vez que Visual Studio crea el proyecto, abra **QueueCreateProject Properties** en el menú **Proyecto**. En la pestaña **Aplicación**, en la lista desplegable **versión .NET Framework de destino** seleccione **.NET Framework 4**. No utilice **.NET Framework 4 Client Profile**. 
  
4. En el Explorador de soluciones, establezca referencias a los ensamblados siguientes:
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. En el archivo Program.cs edite las instrucciones `using` como se indica a continuación. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. Agregue métodos para analizar los argumentos de la línea de comandos y el número de segundos del tiempo de espera de la cola, muestre la información de uso y salga de la aplicación. Reemplace el cuerpo principal del código del archivo Program.cs con el siguiente código.
    
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

## <a name="getting-the-project-context"></a>Obtención del contexto del proyecto
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

El desarrollo de CSOM requiere que se inicialice el objeto **ProjectContext** con la dirección URL de Project Web App. En el código del Procedimiento 2 se usa la constante **pwaPath**. Si tiene previsto usar la aplicación para varias instancias de Project Web App, podría convertir **pwaPath** en una variable y agregar otro argumento de línea de comandos. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Procedimiento 2. Para obtener el contexto del proyecto

1. Agregue las constantes y variables de la clase **Program** que la aplicación **QueueCreateProject** va a usar. Además de la dirección URL de Project Web App, la aplicación usa el nombre del tipo de proyecto empresarial predeterminado (EPT), el nombre del proyecto que se va a crear y un tiempo de espera de cola máximo en segundos. En este caso, la variable **timeoutSeconds** permite probar cómo afectan a la aplicación varios valores para el tiempo de espera. El objeto **ProjectContext** es el objeto principal para acceder al CSOM. 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Reemplace el comentario `/* Add calls to methods here to get the project context and create a project. */` con el código siguiente. El objeto **Microsoft.ProjectServer.Client.ProjectContext** se inicializa con la dirección URL de Project Web App. Los métodos **CreateTestProject** y **ListPublishedProjects** se muestran en el Procedimiento 4 y el Procedimiento 5. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Obtención de un tipo de proyecto empresarial
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

La aplicación de prueba **QueueCreateProject** selecciona explícitamente el tipo de proyecto empresarial (EPT) de Enterprise Project para mostrar cómo una aplicación puede seleccionar el tipo de proyecto empresarial (EPT) para un proyecto. Si la información sobre la creación de un proyecto no especifica el GUID del tipo de proyecto empresarial (EPT), la aplicación usaría entonces el tipo de proyecto empresarial (EPT) predeterminado. El método **GetEptUid** se utiliza por el **CreateTestProject** que se describe en el Procedimiento 4. 
  
El método **GetEptUid** consulta al objeto **ProjectContext** acerca de la recopilación de **EnterpriseProjectTypes** en la que el nombre del tipo de proyecto empresarial (EPT) iguala al nombre especializado. Tras ejecutar la consulta, la variable **eptUid** se define en el GUID del primer objeto **EnterpriseProjectType** en la recopilación **eptList**. Debido a que los nombres del tipo de proyecto empresarial (EPT) son únicos, solo hay un objeto **EnterpriseProjectType** cuyo nombre está especificado. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Procedimiento 3. Para obtener el GUID de un EPT para un proyecto nuevo

- Agregue el método **GetEptUid** a la clase **Program**. 
    
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

Hay varias formas de encontrar el GUID del tipo de proyecto empresarial (EPT). La consulta mostrada en el método **GetEptUid** es eficiente ya que descarga solo el objeto **EnterpriseProjectType** que coincide con el nombre del tipo de proyecto empresarial (EPT). La rutina alternativa que sigue es menos eficiente, dado que descarga toda la lista de tipos de proyectos empresariales (EPT) en la aplicación de cliente y procesa una iteración a lo largo de la lista. 

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

En la rutina siguiente se usa una consulta LINQ y una expresión lambda para seleccionar el objeto EPT, pero se siguen descargando todos los objetos **EnterpriseProjectType**. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Configuración de la información de creación y publicación del proyecto
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

El método **CreateTestProject** crea un objeto **ProjectCreationInformation** y especifica la información necesaria para crear un proyecto. Son necesarios el GUID del proyecto y el nombre. La fecha de inicio, la descripción del proyecto y el GUID del tipo de proyecto empresarial (EPT) son opcionales. 
  
Tras definir las nuevas propiedades del proyecto, el método **Projects.Add** agrega el proyecto a la recopilación **Projects**. Para guardar y publicar el proyecto, debe llamar al método **Projects.Update**, enviar un mensaje a la cola de Project Server y crear el proyecto. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Procedimiento 4. Para establecer las propiedades del proyecto nuevo, crearlo y publicarlo

1. Agregue el método **CreateTestProject** a la clase **Program**. El siguiente código crea y publica un proyecto, pero no espera a que finalice el trabajo en cola. 
    
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

2. Reemplace el comentario `/* Add code here to wait for the queue. */` con el código siguiente para esperar al trabajo en cola. La rutina espera un máximo del número de segundos **timeoutSeconds** especificados, o bien continúa si el trabajo en cola se completa antes del tiempo de espera. Para obtener los estados posibles del trabajo en cola, vea [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx). 
    
   Las llamadas al método **Load** y al método **ExecuteQuery** para el objeto **QueueJob** son opcionales. Si el objeto **QueueJob** no se ha inicializado cuando llama al método **WaitForQueue**, Project Server lo inicializa. 
    
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

## <a name="listing-the-published-projects"></a>Enumeración de los proyectos publicados
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

El método **ListPublishedProjects** obtiene la colección de todos los proyectos publicados en Project Web App. Si el trabajo en cola que crea un proyecto en el Procedimiento 4 no finaliza correctamente o agota el tiempo de espera, el nuevo proyecto no se incluye en la colección **Projects**. 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Procedimiento 5. Para enumerar los proyectos publicados

1. Agregue el método **ListPublishedProjects** a la clase **Program**. 
    
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

2. Establezca el valor correcto para la dirección URL de Project Web App, compile la aplicación **QueueCreateProject** y, después, pruébela como se indica en el Procedimiento 6. 
    
## <a name="testing-the-queuecreateproject-application"></a>Prueba de la aplicación QueueCreateProject
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Al ejecutar por primera vez la aplicación **QueueCreateProject** en una instancia de prueba de Project Web App, sobre todo si Project Server está instalado en una máquina virtual, es posible que la aplicación requiera más tiempo de ejecución que el tiempo de espera predeterminado de diez segundos. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Procedimiento 6. Para probar la aplicación QueueCreateProject

1. Abra la ventana de **Propiedades de QueueCreateProject**, haga clic en la pestaña **Depuración** y, después, agregue los argumentos de línea de comandos siguientes en la sección **Iniciar opciones**: `-n "Test proj 1" -t 20`.
    
   Ejecute la aplicación (por ejemplo, presione **F5**). Si el valor de tiempo de espera es suficientemente largo, la aplicación muestra la salida siguiente (si existen otros proyectos publicados en la instancia de Project Web App, también se mostrarán):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Ejecute otra prueba con los argumentos de línea de comandos siguientes, para usar el tiempo de espera predeterminado de diez segundos: `-n "Test proj 1"`.
    
   Como Test proj 1 ya existe, la aplicación muestra la salida siguiente.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Ejecute otra prueba con los argumentos de línea de comandos siguientes, para usar el tiempo de espera de cola predeterminado de diez segundos: `-n "Test proj 2"`.
    
   La aplicación **QueueCreateProject** crea y publica el proyecto denominado Test proj 2. 
    
4. Ejecute otra prueba con los argumentos de línea de comandos siguientes y establezca el tiempo de espera para que sea demasiado corto como para finalizar el trabajo en cola: `-n "Test proj 3" -t 1`.
    
   Como el tiempo de espera de la cola es demasiado corto, no se crea el proyecto. La aplicación muestra la salida siguiente.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Modifique el código para que la aplicación no espere al trabajo en cola. Por ejemplo, comente el código en el que se espera a la cola, excepto la línea `projCreated = true`, como se indica a continuación. 
    
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

6. Recompile la aplicación y ejecute otra prueba con los argumentos de línea de comandos siguientes: `-n "Test proj 4"`.
    
   Dado que la rutina **WaitForQueue** ha sido excluida mediante comentario, la aplicación no utiliza el valor de tiempo de espera predeterminado. Incluso aunque la aplicación no espere la cola, es posible mostrar Test proj 4, si la acción publicar es lo suficientemente rápida en Project Server. 
    
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

Actualice la página Centro de proyectos en Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`) para mostrar los proyectos publicados. En la figura siguiente se muestra que los proyectos de prueba se han publicado.

**Comprobación de los proyectos publicados en Project Web App**

![Comprobación de los proyectos publicados en Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Checking the published projects in Project Web App")
  
En la aplicación de prueba **QueueCreateProject** se muestra un ejemplo típico de cómo crear una entidad de proyecto con el CSOM mediante la clase **ProjectCreationInformation**, cómo agregar el proyecto a la colección publicada y cómo esperar un trabajo en cola con el método **WaitForQueue**, además de cómo enumerar la colección de proyectos publicados. 
  
## <a name="complete-code-example"></a>Ejemplo de código completo
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

A continuación, se muestra el código completo para la aplicación de ejemplo **QueueCreateProject**. En la referencia de la clase [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) también se incluye el código de este tema. 
  
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
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
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

## <a name="see-also"></a>Vea también

- [Actualizaciones para desarrolladores de Project 2013](updates-for-developers-in-project-2013.md) 
- [Modelo de objetos de cliente (CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md)
    

