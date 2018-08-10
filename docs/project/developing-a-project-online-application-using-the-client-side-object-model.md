---
title: Desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: En este artículo se describe el desarrollo de aplicaciones Microsoft Project Online para aplicaciones de escritorio con .NET Framework 4.0. La aplicación que se describen en este artículo, recupera información desde el servidor de hospedaje.
ms.openlocfilehash: a0a2b4042d4db127c56c5ba873ebe25418344571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821318"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>Desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente

En este artículo se describe el desarrollo de aplicaciones Microsoft Project Online para aplicaciones de escritorio con .NET Framework 4.0. La aplicación que se describen en este artículo, recupera información desde el servidor de hospedaje. 
  
## <a name="background"></a>Fondo

Microsoft Project inicia como aplicación de escritorio de principios de los 90. En la actualidad, Project es mucho más, como sus diversas variedades confirmar:
  
- Project standard edition es una aplicación de escritorio que se ejecuta como una aplicación independiente.
    
- Professional, edición de proyecto es una aplicación de escritorio que puede interactuar y compartir datos con un servidor en una escala mayor, así como realizar la funcionalidad de edición estándar de Project.
    
- Project Online es un servicio hospedado por Microsoft que proporciona a las empresas con una solución de nivel de PMO para coordinar y administrar proyectos, programas y carteras de proyectos. Una oferta de diferente que las ediciones de escritorio, Project Online puede mantener y realizar un seguimiento de los detalles del proyecto a lo largo de la vida de un proyecto. 
    
- Project Server es un servicio hospedado de empresa en la que la empresa administra y protege el servidor que contiene información de la cartera de proyectos, programa y proyecto. Project Server, debe proteger el servidor interno, ofrece el proyecto, programa y las características de cartera de proyectos orientados a de hospedado externamente Project Online con una mayor capacidad de personalización.
    
Project Online tiene tres conjuntos de API en línea: modelo de objetos de cliente (COM), modelo de objetos de JavaScript (JSOM) y Representational State Transfer (REST). 
  
- La implementación de CSOM de .NET es la interfaz preferida al desarrollar aplicaciones de Windows que interactúan con los inquilinos de Project Online. Los entornos típicos para aplicaciones centradas en el usuario incluyen los escritorios de Windows y dispositivos de Microsoft Surface. Aplicaciones de back-end escritas con CSOM de .NET pueden conectarse a otros servidores para los orígenes de datos y lógica empresarial que son externos a Project Online. Las solicitudes de recuperación para Project Online use un sistema de consulta similar a LINQ que ofrece varias mejoras sobre las funciones de recuperación básica.
    
- La interfaz de modelo de objetos de JavaScript (JSOM) proporciona compatibilidad entre exploradores para Project Online Add-ins. Un complemento es una aplicación web que se almacena en el inquilino Project Online. Cuando un usuario desea ejecutar un complemento, el código para el complemento se descarga y se ejecuta en el explorador en el equipo del usuario. 
    
- El modelo de REST/Odata proporciona comunicación basadas en HTTP, se recomienda esta interfaz para aplicaciones en entornos que no son de Windows. Los extremos de comunicación son los objetos en el sitio de Project Web Application (PWA). Los resultados proporcionan códigos de estado HTTP normales.
    
En este artículo se centra en una aplicación que usa la interfaz de .NET CSOM.
  
## <a name="prerequisites"></a>Requisitos previos

Empezar con una base del sistema que ejecuta Windows 10 y agregue los siguientes elementos:
  
- .NET framework 4.0 o posterior--usar el marco de trabajo completo. El sitio de descarga es https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- Visual Studio 2013 o posterior--cualquier edición es aceptable. Se usó la edición de la Comunidad de 2015 de Visual Studio para desarrollar la aplicación de ejemplo. La edición de la Comunidad está disponible en https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- Componentes de cliente de SharePoint SDK--Project Online y Project Server coloca encima de SharePoint y SharePoint ensamblados. Los componentes de cliente de SharePoint se incluyen en las ediciones de Visual Studio Professional y Enterprise. Si utiliza la edición de la Comunidad de Visual Studio, la versión más reciente del SDK de herramientas para desarrolladores de Office está disponible en el siguiente sitio: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Una cuenta de Project Online--Esto proporciona acceso al sitio de hospedaje. Para obtener más información acerca de cómo obtener una cuenta de Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Proyectos en el sitio de hospedaje que se rellenan con información
    
> [!NOTE]
> El estándar de .NET Framework (4.0 o posterior) es el marco de trabajo correcto para usar. No use el perfil de cliente de .NET Framework 4. 
  
## <a name="develop-the-application"></a>Desarrollar la aplicación

En el desarrollo de una aplicación de escritorio para SharePoint, la interfaz preferida es el modelo de objetos del lado de cliente de Project (COM). 
  
Puede descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.
  
Los dos primeros temas tratan problemas básicos: creación de un proyecto de Visual Studio con ensamblados y espacios de nombres adecuados y obtener acceso al servidor de hospedaje. Los temas restantes abordar los problemas con la recuperación de información a través de CSOM, de uno y varios objetos. 
  
Recuperar información desde el host es un proceso de dos acción desde aplicaciones cliente. En primer lugar, la aplicación especifica y envía una o varias de las solicitudes de recuperación en el servidor. En segundo lugar, la aplicación emite una notificación al servidor para ejecutar las consultas enviadas. El servidor responde con el envío de los resultados de consulta al cliente.
  
### <a name="set-up-the-visual-studio-project"></a>Configurar el proyecto de Visual Studio

El programa de instalación de la aplicación consiste en crear un nuevo proyecto, vinculación los ensamblados correspondientes y declarar los espacios de nombres necesarios. Visual Studio presenta varios tipos de proyectos de desarrollo. 
  
#### <a name="select-a-visual-studio-project"></a>Seleccione un proyecto de Visual Studio

1. Inicie Visual Studio y seleccione **Iniciar un nuevo proyecto** en la página de inicio. 
    
   El cuadro de diálogo nuevo proyecto muestra plantillas de aplicación disponibles y los campos de datos para cualquier plantilla seleccionada. 
    
2. Para esta aplicación, especifique los elementos siguientes. Palabras clave que se encuentra en la pantalla tienen un atributo negrita:
    
   1. En las plantillas instaladas en el panel izquierdo, seleccione **C#** => **Windows** => **escritorio clásico**. 
    
   2. En la parte superior del panel central, seleccione **.NET Framework 4**. 
    
   3. En los tipos de aplicación en el panel central, seleccione **Aplicación de consola**. 
    
   4. En la sección inferior, especifique un nombre y una ubicación para el proyecto y un nombre de la solución. 
    
   5. También en la sección inferior, active la casilla **Crear directorio para la solución** . 
    
3. Haga clic en **Aceptar** para crear el proyecto inicial. 
    
#### <a name="add-assemblies"></a>Agregar ensamblados

La solución de VS necesita el ensamblado ProjectServerClient desde Project 2103 SDK, un par de ensamblados desde el SDK de SharePoint y el ensamblado de .NET Framework System.Security.
  
1. En el Explorador de soluciones frente a, haga clic en la entrada de referencias y seleccione **Agregar referencia** en el menú contextual. 
    
2. Comprobar la **Microsoft.ProjectServer.Client.dll**. 
    
   Si es necesario, haga clic en **Examinar...** botón en la parte inferior del cuadro de diálogo y navegue hasta el directorio de instalación de SDK de Project 2013 para buscar el ensamblado. 
    
3. Haga clic en **Aceptar**. 
    
4. Agregue el espacio de nombres de cliente de PrjoctServer al archivo. cs.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Agregue los ensamblados SDK de SharePoint 2013 mediante la consola de administrador de paquetes de NuGet. 
  
1. En el menú Herramientas de VS, haga clic en los menús siguientes: **herramientas =\> Administrador de paquetes de NuGet =\> consola de administrador de paquetes**. 
    
2. En la consola de administrador de paquetes, escriba el siguiente comando y presione \<ENTRAR\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   La **Consola de administrador de paquetes** proporciona una descripción de los resultados del comando; y, en el Explorador de soluciones de VS muestra los ensamblados de SharePoint en las referencias del proyecto. 
    
3. Agregue los espacios de nombres en el archivo .cs:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

El ensamblado System.Security forma parte de .NET Framework y se ha instalado con el marco de trabajo. La aplicación de ejemplo, necesita un espacio de nombres más que proporciona una cadena cifrada para el sistema de hospedaje para la autenticación. Una vez autenticado, la aplicación puede tener acceso a los proyectos en el sistema de hospedaje. Agregue el espacio de nombres System.Security al archivo .cs de esta manera:
  
1. En el Explorador de soluciones frente a, haga clic en la entrada de referencias y seleccione **Agregar referencia** en el menú contextual. 
    
2. Seleccione **ensamblados =\> Framework** en el panel izquierdo del cuadro de diálogo Administrador de referencias, a continuación, comprobar **System.Security**. 
    
3. Haga clic en **Aceptar**. 
    
4. Agregue el espacio de nombres System.Security al archivo .cs:
    
   ```cs
    using System.Security;
   ```

El inicio del archivo .cs debe contener los espacios de nombres siguientes:
  
- Sistema
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Conectarse al sistema de host

Project Online es una aplicación de SharePoint, por lo que usa la autenticación de SharePoint es el enfoque correcto. El siguiente fragmento de código se prepara para tener acceso a un entorno hospedado.
  
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

Preparativos para tener acceso a un entorno hospedado incluyen los siguientes elementos:
  
1. Crear un objeto de contexto para los proyectos: Esto se encuentra en el siguiente código del fragmento de código anterior. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   El contexto es heredado por otros componentes, lo que permite el sistema administrar el contexto del modelo de objetos de Project.
    
2. Identificar el sitio host: Esto se hace en el siguiente código desde el fragmento de código anterior.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Al crear una instancia del contexto de proyectos, la aplicación debe proporcionar la raíz de la colección de sitios de proyectos. La aplicación usa una subcadena de la dirección URL de la raíz de los proyectos. Una instantánea de esta ubicación se resalta con un rectángulo rojo en la siguiente ilustración. La autenticación necesita la cadena desde su inicio a través de la subcadena "pwa". En el listado de código, la aplicación utiliza la cadena "https://XXXXXXXX.sharepoint.com/sites/pwa".
        
   ![Captura de pantalla de la dirección URL de la colección de sitios de proyectos dentro de un borde rojo.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Captura de pantalla de la dirección URL de los proyectos colección dentro de un borde rojo de sitios")
  
3. Colocar la contraseña en una cadena segura: Esto se hace en el siguiente código desde el fragmento de código anterior.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   La cuenta de usuario y contraseña son las credenciales para tener acceso al sitio host. 
    
4. Agregue la cuenta de usuario y la contraseña a la parte de las credenciales del objeto context: Esto se hace en el siguiente código desde el fragmento de código anterior.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

El contexto del proyecto instancias está listo para usarse.
  
### <a name="list-all-published-projects"></a>Lista de proyectos publicados todo

Project Online y ProjectServer usan a servidores proxy para comunicarse con el servidor para crear, informe, actualizar y eliminación operaciones (CRUD). El servidor de host controla las solicitudes de una manera eficaz y tiene el cliente de realizar las siguientes acciones en la comunicación con el servidor:
  
1. Establecer un contexto para la comunicación. 
    
   El contexto se usa en la colección de proyectos, así como otros objetos y colecciones a través de herencia, incluida la colección tasks, colección de asignaciones, el objeto stage y campos personalizados. 
    
2. Use el modelo de objetos para especificar un objeto, colección o datos que desea recuperar.
    
   Este paso usa LINQ como una consulta o como un método. La especificación controla lo que reciba. A menudo, este paso se incrusta como el cuerpo del método Load (paso 3). 
    
3. Cargar la especificación de recuperación desde el paso anterior con el método Load() o LoadQuery().
    
   Para cargar objetos y colecciones, use Load(). Para las consultas con cláusulas como "where" y "grupo", use LoadQuery(). 
    
4. Ejecutar la solicitud mediante el método ExecuteQuery().
    
   El método ExecuteQuery() notifica al host que la consulta o consultas están listos para ejecutarse. Una vez que el host recibe la notificación, ejecuta las consultas y envía los resultados al cliente. 
    
Con la información en el cliente, la aplicación puede usarla. El siguiente fragmento de código recorre en iteración los proyectos publicados e imprime el identificador y el nombre para cada proyecto publicado en el host.
  
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

Salida:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Realizar una solicitud

Uso de las acciones desde el fragmento de código anterior, la aplicación recupera la lista de proyectos en la cuenta especificada en el sitio de hospedaje. 
  
1. El ProjectContext especificado para que los proyectos para obtener una lista. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Especificar el elemento que se va a recuperar. 
    
   ```cs
    projContext.Load(projects);
   ```

   Sólo que indica la colección, el servidor recupera la colección de proyectos, rellenar cada proyecto con los valores para el conjunto predeterminado de propiedades. Obtener acceso a las propiedades que forman parte del conjunto de propiedades predeterminado proporciona buenos resultados. Obtener acceso a las propiedades que no forman parte de la predeterminada establecer los resultados de una excepción "No inicializado".
    
3. Carga de la solicitud (projContext.Load).
    
   Esto es parte del paso anterior.
    
4. Ejecutar la consulta (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Recuperar información de alto nivel del proyecto

Propiedades que no son propiedades predeterminadas deben especificarse en la solicitud al servidor. El siguiente fragmento de código carga el contexto de la colección de proyectos como en el ejemplo anterior. A continuación, la especificación solicita propiedades no predeterminados adicionales para incluir en el resultado. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

La instrucción load especifica el contexto de la colección de proyectos y agrega la StartDate, fase y región para el resultado de la consulta. Las propiedades adicionales que pueden ser escalares, objetos o colecciones. Elementos escalares pueden tener acceso directamente. Objetos y colecciones requieren un procesamiento adicional, como se muestra en el siguiente fragmento de código.
  
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

Salida de los tres primeros proyectos:
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>Recuperar todas las tareas en un proyecto

Cada proyecto tiene muchas de las tareas. Por lo tanto, la inclusión de las tareas de un único proyecto consta de lo siguiente:
  
1. Establecer el contexto de la colección de proyectos.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Recuperar la información del proyecto, incluidas las propiedades de la tarea.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Tenga en cuenta que la aplicación es hacer frente a los proyectos publicados. El contexto para el proyecto publicado actual es pubProj. 
    
3. Establecer el contexto de la colección Tasks.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   El `pubProj.Tasks` (propiedad) hace referencia a las tareas del proyecto publicado actual. 
    
4. Carga de la especificación para recuperar la colección de tareas, incluidas las propiedades que no sean predeterminados adecuadas.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Ejecutar la consulta para recuperar la colección de tareas con las propiedades adecuadas.
    
   ```cs
    projContext.ExecuteQuery();
   ```

La información ahora es local. El siguiente fragmento de código procesa la colección tasks publicados mediante la escritura de la información en la consola.
  
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

Salida de tareas para un proyecto:
  
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

### <a name="access-information-at-multiple-levels"></a>Información de acceso en varios niveles

Cada tarea puede tener una o más personas (también conocido como recursos) contribuya a su finalización. Las colecciones de asignaciones y recursos que contienen esta información para cada tarea. 
  
El procesamiento consta de lo siguiente:
  
1. Obtención de un contexto para la tarea del proyecto.
    
2. Generar una solicitud y cargar la solicitud para las asignaciones de vinculadas a la tarea. 
    
3. Ejecutar la consulta para las asignaciones.
    
4. Generar una solicitud y cargar la solicitud para el recurso asociado a una asignación individual. 
    
5. Ejecutar la consulta para el recurso.
    
> [!NOTE] 
> - La colección de asignaciones se solicita explícitamente en la información desde el servidor porque no es una propiedad predeterminada de la colección Tasks. Como una colección, se realiza una consulta subsiguiente se van a extraer la colección desde el servidor. 
> - El recurso es un objeto. La consulta para una asignación incluye el nombre de recurso asociado con la asignación.
    
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

Salida para tareas 52, 75 y 76 de un proyecto:
  
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

### <a name="access-custom-enterprise-level-fields"></a>Campos personalizados de empresa-nivel de acceso

Existen campos personalizados para Project Online. Estos son los campos de nivel de empresa que se pueden asociados a un proyecto individual. En esta sección se describe cómo tener acceso a estos campos. 
  
Los campos personalizados no se incluyen en el conjunto predeterminado de propiedades asociadas con un proyecto. Por lo tanto, necesitan identificación explícita en la especificación de recuperación. La vista de alto nivel del proceso consta de los siguientes elementos:
  
1. Túnel para el campo personalizado mediante su nombre común.
    
2. Recuperar el nombre interno del campo personalizado.
    
3. Vuelva al contexto global y el sistema con el nombre interno del campo personalizado de consulta.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Túnel para el campo personalizado, recuperar su nombre interno y utiliza para consultar el sistema

Esta tarea, especifica un sistema de recuperación que utiliza una propiedad no predeterminada con un nivel de detalle se ha agregado.
  
1. Para empezar, utilizando el contexto de proyectos, tal como se describe al principio de este artículo.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Agregue dos elementos a la solicitud de recuperación de colección de proyectos además de otras propiedades que no sean predeterminados para recuperar:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   El `p => p.IncludeCustomFields` cláusula identifica la necesidad de usar un objeto de proyecto que es compatible con los campos personalizados. 
    
   El `p => p.IncludeCustomFields.CustomFields` cláusula solicita la inclusión de datos de campo personalizado en el resultado de la consulta. Esta información se utiliza después de recupera el nombre interno de campo personalizado. 
    
3. La solicitud de carga.
    
   Esto es parte del paso anterior.
    
4. Ejecutar la consulta.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Con esta información en el cliente, crear una solicitud para recuperar los campos personalizados asociados al proyecto actual.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Busque la apropiada del campo personalizado y recuperar el nombre interno del campo. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Se recupera el nombre interno del campo personalizado. Los elementos de alto nivel 1 y 2 ahora están completados.
    
7. Volver al contexto del proyecto y recuperar el valor del campo personalizado.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > Se recupera el valor del campo personalizado con el nombre interno como un índice. 
  
Salida de tres proyectos formado por identificador de proyecto, nombre del proyecto, nombre de campo personalizado, nombre interno de campo personalizado y valor de campo personalizado.
  
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

## <a name="see-also"></a>Vea también

Para obtener documentación y ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal del proyecto de desarrollo](http://dev.office.com/project.aspx).
    

