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
- ejemplos de código, project server,Project Server, programación,PSI, compilación de ejemplos de código,PSI, programación
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Obtenga información para ayudarle a crear proyectos en Visual Studio usando los ejemplos de código basados en ASMX que se incluyen en los temas de referencia de Project Server Interface (PSI).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357095"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Requisitos previos para los ejemplos de código basados en ASMX en Project

Obtenga información para ayudarle a crear proyectos en Visual Studio usando los ejemplos de código basados en ASMX que se incluyen en los temas de referencia de Project Server Interface (PSI).
  
Muchos de los ejemplos de código incluidos en la biblioteca de clases y la referencia del servicio web de [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) se crearon originalmente para el SDK de Office Project 2007 y usan un formato estándar para los servicios web ASMX. Los ejemplos siguen funcionando en Project Server 2013 y están diseñados para copiarse en una aplicación de consola y ejecutarse como una unidad completa. Las excepciones están señaladas en la muestra. 
  
Los nuevos ejemplos de PSI en el SDK de Project 2013 se ajustan a un formato que usa los servicios de Windows Communication Foundation (WCF). Las muestras basadas en ASMX también pueden adaptarse para usar servicios de WCF. Este artículo muestra cómo usar las muestras con servicios web de ASMX. Para obtener información acerca del uso de los ejemplos con servicios WCF, vea [Requisitos previos para](prerequisites-for-wcf-based-code-samples-in-project.md)ejemplos de código basados en WCF en Project .
  
> [!NOTE]
> La interfaz de servicios web ASMX de la PSI está en desuso en Project Server 2013, pero aún es compatible. Si el modelo de objeto de cliente (CSOM) incluye los métodos que su aplicación necesita, deberían desarrollarse nuevas aplicaciones con el CSOM. El CSOM permite a las aplicaciones trabajar con Project Online o una instalación local de Project Server 2013. De lo contrario, si su aplicación usa la PSI, debería usar la interfaz de WCF, que es la tecnología que recomendamos para las comunicaciones de red. Las aplicaciones que usan la interfaz ASMX o wcf solo pueden funcionar para instalaciones locales de Project Server 2013. Para obtener más información acerca del CSOM, vea La arquitectura de [Project Server 2013](project-server-2013-architecture.md) y el modelo de objetos del lado cliente [(CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de usar las muestras de código, asegúrese de configurar el entorno de desarrollo, configurar la aplicación y modificar los valores de constantes genéricas para que coincidan con su entorno.
  
## <a name="setting-up-the-development-environment"></a>Configurar el entorno de desarrollo
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Configurar un sistema de Project Server de prueba**.
    
   Use un sistema de Project Server de prueba siempre que haga un desarrollo o una prueba. Incluso cuando su código funcione perfectamente, las dependencias entre proyectos, los informes u otros factores de entorno pueden generar consecuencias no esperadas. 
    
   > [!NOTE]
   > Asegúrese de ser un usuario válido en el servidor y compruebe que posee los permisos suficientes para las llamadas de la PSI que use su aplicación. El tema de la referencia de desarrollador para cada método de PSI incluye una tabla de permisos de Project Server. Por ejemplo, el [método Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requiere el permiso global **NewProject** y **el permiso SaveProjectTemplate.** 
  
   En algunos casos, quizás deba hacer una depuración remota en el servidor. También puede que tenga que configurar un controlador de eventos instalando un ensamblado de controlador de eventos en cada equipo de Project Server en la granja de servidores de SharePoint y, a continuación, configurando el controlador de eventos para la instancia de Project Web App mediante la página Configuración de Project Server en la Configuración de aplicación general de Administración central de SharePoint.
    
2. **Configurar un PC de desarrollo.**
    
   Generalmente obtiene acceso a la PSI a través de una red. Las muestras de código están diseñadas para usarse en un cliente independiente del servidor, excepto cuando se indique lo contrario.
    
   1. **Instale la versión correcta de Visual Studio.** Excepto cuando se lo especifique, las muestras de código se escriben en Visual C#. Se pueden usar con Visual Studio 2010 o Visual Studio 2012. Asegúrese de tener instalado el Service Pack más reciente. 
        
   2. **Copie los DLL de Project Server en el PC de desarrollo.** Copie los ensamblados siguientes del equipo de  `[Program Files]\Microsoft Office Servers\15.0\Bin` Project Server en el equipo de desarrollo: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Para obtener información sobre cómo compilar y usar el ensamblado de proxy ProjectServerServices.dll para los servicios web de ASMX en la PSI, vea [Usar un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Instalar los archivos de IntelliSense.**
    
    Para usar descripciones de IntelliSense para clases y miembros en ensamblados de Project Server, copie los archivos XML de IntelliSense actualizados de la descarga del SDK de Project 2013 en el mismo directorio donde se encuentran los ensamblados de Project Server. Por ejemplo, copie el archivo Microsoft.Office.Project.Server.Library.xml al directorio donde su aplicación establecerá una referencia al ensamblado Microsoft.Office.Project.Server.Library.dll.
    
    IntelliSense descripciones para los servicios web de psi requieren que cree un ensamblado de proxy de PSI mediante el script CompileASMXProxyAssembly.cmd en el subdirectorio de la descarga del SDK de  `Documentation\IntelliSense\WSDL` Project 2013. El script crea el ensamblado de proxy ProjectServerServices.dll basado en ASMX. Para más información, vea el archivo [ReadMe_IntelliSense] en la descarga de SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Crear la aplicación y agregar una referencia de servicio web
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Crear una aplicación de consola**.
    
   Cuando crea una aplicación de consola, en la lista desplegable del cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4**. Puede copiar el código de ejemplo de PSI en la nueva aplicación.
    
2. **Agregar la referencia necesaria para ASMX.**
    
   En el Explorador de soluciones, agregue una referencia a **System.Web.Services** (vea la Figura 1). 
    
   **Figura 1. Adición de una referencia en Visual Studio**

   ![Agregar una referencia en Visual Studio]agregar una referencia en(media/pj15_PrerequisitesASMX_AddReference.gif "Visual Studio")
  
3. **Copiar el código**.
    
   Copie el ejemplo de código completo en el archivo Program.cs de la aplicación de consola.
    
4. **Establecer el espacio de nombres para la aplicación de muestra**.
    
   Puede cambiar el espacio de nombres que aparece en la parte superior de la muestra por el espacio de nombres predeterminado de la aplicación o bien cambiar el espacio de nombres de la aplicación predeterminado para que coincida con la muestra. Puede cambiar el espacio de nombres de la aplicación predeterminado modificando las propiedades de la aplicación.
    
   Por ejemplo, el ejemplo de código [de QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) tiene el espacio de nombres **Microsoft.SDK.Project.Samples.RenameProject**. Si el nombre del proyecto de Visual Studio es **RenameProject**, copie el espacio de nombres desde el archivo Program.cs y, después, abra el panel **Propiedades** del proyecto (en el menú **Proyecto**, elija **Propiedades de RenameProject**). En la pestaña **Aplicación**, copie el espacio de nombres en el cuadro de texto **Espacio de nombre predeterminado**. 
    
5. **Establecer las referencias web**.
    
   Muchos ejemplos necesitan una referencia a uno o más de los servicios web de la PSI. Estos aparecen en la muestra misma o en comentarios que preceden a la muestra. Para obtener el espacio de nombres correcto de las referencias web, asegúrese de establecer primero el espacio de nombres de la aplicación predeterminado.
    
   Existen tres maneras de agregar una referencia de servicio web de ASMX para la PSI:
    
   - Cree un ensamblado de proxy de PSI llamado ProjectServerServices.dll y, después, establezca una referencia al ensamblado. Para obtener IntelliSense, esta es la manera recomendada de agregar una referencia de PSI. Vea [Usar un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Agregue un archivo de proxy desde la salida wsdl.exe a la solución de Visual Studio. Vea [Agregar un archivo de proxy de PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Agregue una referencia de servicio web usando Virtual Studio. Vea [Agregar una referencia de servicio web](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Usar un ensamblado de proxy de PSI y descripciones de IntelliSense

Puede crear y usar el ensamblado de proxy ProjectServerServices.dll para todos los servicios web basados en ASMX en psi, mediante el script CompileASMXProxyAssembly.cmd en la carpeta de la descarga del SDK de  `Documentation\IntelliSense\WSDL` Project 2013. Para obtener un vínculo a la descarga, vea la documentación para desarrolladores de [Project 2013.](project-2013-developer-documentation.md)
  
> [!NOTE]
> Al extraer los archivos de origen proxy del archivo Source.zip, los archivos de la carpeta están actualizados a partir de la fecha de publicación de la descarga del SDK de  `Documentation\IntelliSense\WSDL\Source` Project 2013. Para generar archivos de origen de proxy de PSI actualizados, use el script GenASMXProxyAssembly.cmd en el PC de Project Server. Los scripts de la  `Documentation\IntelliSense\WCF` carpeta no funcionan para aplicaciones basadas en ASMX. El script GenWCFProxyAssembly.cmd llama a SvcUtil.exe, que genera archivos de código de origen para los servicios de WCF. Los archivos de proxy de WCF incluyen diferentes atributos, la interfaz de canal, y una clase de cliente para cada servicio de PSI. Por ejemplo, el servicio Recurso basado en WCF incluye la interfaz de **ResourceChannel**, la interfaz de **Resource**, y la clase **ResourceClient**. La web de Recurso basado en ASMX incluye la clase **Resource** con algunas propiedades diferentes. 
  
A continuación se muestra el script GenASMXProxyAssembly.cmd que genera archivos de salida de WSDL para los servicios web de PSI, y después compila el ensamblado.
  
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

El script usa el archivo ClassList_asmx.txt, que contiene la lista de servicios web que están disponibles para otros desarrolladores.
  
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

Los scripts crean un ensamblado con el nombre ProjectServerServices.dll. No lo confunda con ProjectServerServices.dll para el ensamblado basado en WCF. Los nombres de ensamblado son los mismos, para permitir el uso de cualquiera de los ensamblados con el archivo ProjectServerServices.xml de IntelliSense.
  
El espacio de nombres arbitrario creado por los scripts tanto para los servicios web de ASMX como para los servicios de WCF es el mismo, de manera que el archivo ProjectServerServices.xml de IntelliSense funciona con ambos ensamblados. Por ejemplo, el espacio de nombres del servicio Recurso en el ensamblado de proxy basado en WCF y en el ensamblado de proxy basado en ASMX es **SvcResource**. Por supuesto, puede modificar los nombres de los espacios de nombres, si se asegura de que coinciden en el ensamblado de proxy y en el archivo ProjectServerServices.xml de IntelliSense.
  
Si una muestra de código usa un nombre diferente para un espacio de nombres de servicio web de PSI, por ejemplo **ProjectWebSvc**, para que funcione IntelliSense asegúrese de cambiar la muestra para que use **SvcProject** de manera que el espacio de nombres coincida con el ensamblado de proxy. 
  
Una ventaja de usar el ensamblado de proxy basado en ASMX es que incluye todos los nombres de espacio de servicio web de PSI; no tiene que crear varias referencias web. Otra ventaja es que, si agrega el archivo ProjectServerServices.xml al mismo directorio donde estableció una referencia al ensamblado de proxy ProjectServerServices.dll, puede obtener descripciones de IntelliSense para los miembros y las clases de PSI. La Figura 2 muestra el texto de IntelliSense para el método **Project.QueueCreateProject**. Para obtener más información, vea el archivo [ReadMe_IntelliSense] en la carpeta IntelliSense de la descarga del SDK de Project 2013. 
  
**Figura 2. Uso de IntelliSense para un método en el servicio web de Recurso**

![Uso de IntelliSense para un método en un servicio de PSI]mediante(media/pj15_PrerequisitesASMX_Intellisense.gif "IntelliSense para un método en un servicio de PSI")
  
Las desventajas de usar el ensamblado de proxy son que la solución es mayor y usted necesita distribuir e instalar el ensamblado de proxy con la solución. También necesita usar los mismos espacios de nombres que se encuentran en el ensamblado de proxy y los archivos de IntelliSense, a menos que cambie el script y el archivo ProjectServerServices.xml de IntelliSense para usar distintos espacios de nombres.
  
### <a name="adding-a-psi-proxy-file"></a>Agregar un archivo de proxy de PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

La descarga del SDK de Project 2013 incluye los archivos de origen generados por el comando Wsdl.exe para el ensamblado de proxy. Los archivos de origen están Source.zip en el  `Documentation\IntelliSense\ASMX` subdirectorio. En lugar de establecer una referencia al ensamblado de proxy, puede agregar uno o más archivos de origen a una solución de Visual Studio. Por ejemplo, después de usar el script GenASMXProxyAssembly.cmd, agregue el archivo wsdl.Project.cs file a la solución. En vez de usar el script, puede usar los siguientes comandos para generar un solo archivo de origen, por ejemplo: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Para definir un objeto de **Project** como variable de clase con el nombre **project**, use el siguiente código. El método **AddContextInfo** agrega la información contextual al objeto de **project** para autenticación de Windows y autenticación basada en formularios. 
  
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
> Si usa un ensamblado de proxy de PSI o agrega un archivo de proxy para una referencia de servicio de Project llamada **SvcProject**, usaría el mismo código para crear un objeto de **project**. 
  
### <a name="adding-a-web-service-reference"></a>Agregar una referencia de servicio web
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Si no usa el ensamblado de proxy basado en ASMX o agrega un archivo de salida de WSDL, puede establecer una o más referencias web individuales. Los siguientes pasos muestran cómo establecer una referencia web mediante Visual Studio 2012.
  
1. En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** y después seleccione **Agregar referencia de servicio**. 
    
2. En el cuadro de diálogo **Agregar referencia de servicio**, elija **Avanzada**.
    
3. En el cuadro de diálogo **Configuración de referencia de servicio**, elija **Agregar referencia web**.
    
4. En el cuadro de texto dirección **URL,** escriba y, a continuación, `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` presione **ENTRAR** o elija el **icono** Ir. Si tiene instalada la Capa de sockets seguros (SSL), asegúrese de usar el protocolo HTTPS en lugar del protocolo HTTP. 

   Por ejemplo, use la siguiente dirección URL para el servicio project en el  `https://MyServer/pwa` sitio de Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   O bien, abra el explorador web y vaya a `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` . Guarde el archivo en un directorio local, como `C:\Project\WebServices\ServiceName.wsdl` . En el cuadro de diálogo **Agregar referencia web**, para **Dirección URL**, escriba el protocolo de archivo y la ruta de acceso al archivo. Por ejemplo, escriba `file://C:\Project\WebServices\Project.wsdl`. 
    
5. Una vez que se resuelve la referencia, escriba el nombre de la referencia en el cuadro de texto **Nombre de referencia web**. Los ejemplos de código de la documentación para desarrolladores de Project 2013 usan el nombre de referencia estándar arbitrario **Svc _ServiceName_**. Por ejemplo, el servicio web de Proyecto tiene el nombre **SvcProject** (vea la Figura 3). 
    
   **Figura 3. Adición de una referencia de servicio web de ASMX**

   ![Adición de una referencia de servicio web ASMX](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Agregar una referencia de servicio web ASMX")
  
Para los componentes de aplicación que deben usarse en el PC de Project Server, use suplantación, o tenga permisos elevados, use una referencia de servicio de WCF en lugar de una referencia web de ASMX. Para obtener más información, vea [Requisitos previos para ejemplos de código basados en WCF en Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Estableciendo otras referencias
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Las aplicaciones de Project Server suelen usar otros servicios, como los servicios web de SharePoint Server 2013. Si se necesitan otros servicios, se lo señala en el ejemplo.
  
Las referencias locales para la muestra de código aparecen en las instrucciones de **using** en la parte superior de la muestra: 
  
1. En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** y después seleccione **Agregar referencia**.
    
2. Seleccione **Examinar** y después diríjase a la ubicación donde ha almacenado los DLL de Project Server que copió previamente. Elija los DLL que necesite y luego seleccione **Aceptar**.
    
> [!NOTE]
> Asegúrese de que las versiones de ensamblado en su PC de desarrollo coincidan exactamente con aquellas del PC de Project Server de destino. 
  
## <a name="using-multiple-authentication"></a>Usar autenticación múltiple
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

La autenticación de usuarios locales de Project Server, ya sea mediante autenticación de Windows o autenticación de formularios, se realiza mediante el procesamiento de notificaciones en SharePoint Server 2013. La autenticación múltiple significa que la aplicación web en la que se aprovisiona Project Web App admite la autenticación de Windows y la autenticación basada en formularios. Si ese es el caso, cualquier llamada a un servicio web de ASMX que use la autenticación de Windows fallará con el siguiente error, porque el proceso de notificaciones no puede determinar qué tipo de usuario autenticar:
  
`The server was unable to process the request due to an internal error. . . .`

Para solucionar el problema para ASMX, todas las llamadas a los métodos de PSI deberían hacerse a una clase derivada que se define para cada servicio web de PSI. La clase derivada también debe usar la clase **SvcLoginWindows.LoginWindows** para obtener una cookie para la clase de servicio de PSI derivada. En el siguiente ejemplo, la clase **ProjectDerived** deriva de la clase **SvcProject.Project**. La clase derivada agrega la propiedad **EnforceWindowsAuth** y sobrescribe el encabezado de solicitud web para todas las llamadas a un método en la clase **Project**. Si la propiedad **EnforceWindowsAuth** es **true**, el método **GetWebRequest** agrega un encabezado que deshabilita la autenticación de formularios. Si **EnforceWindowsAuth** es **false**, se puede continuar con la autenticación de formularios.
  
Para usar la siguiente muestra **ASMXLogon_MultiAuth**, cree una aplicación de consola, siga los pasos en [Crear la aplicación y agregar una referencia de servicio web](#pj15_PrerequisitesASMX_Configure), y después agregue el archivo de proxy wsdl.LoginWindows.cs y el archivo de proxy wsdl.Project.cs. El método **Main** crea la instancia **project** de la clase **ProjectDerived**. La muestra debe usar la clase derivada **LoginWindowsDerived** para obtener un objeto **CookieContainer** para la propiedad **project.CookieContainer**, que distingue la autenticación de formularios y la autenticación de Windows. El objeto **project** puede usarse después para hacer llamadas a cualquier método en la clase **SvcProject.Project**. 
  
> [!NOTE]
> El servicio **LoginWindows** es necesario solo para aplicaciones de ASMX en un entorno de autenticación múltiple. En la muestra **ASMXLogon_MultiAuth**, el método **GetLogonCookie** obtiene una cookie para el objeto **loginWindows**. La propiedad **project.CookieContainer** se establece en el valor **loginWindows.CookieContainer**. 
  
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

Las aplicaciones que se inician en un entorno de autenticación múltiple necesitan el uso de la clase derivada **LoginWindows** y la realización de llamadas de PSI con un encabezado de solicitud web que deshabilita la autenticación de formularios. Si Project Server usa solo autenticación de notificaciones, no es necesario derivar un clase que agrega un encabezado de solicitud web. El ejemplo anterior se usa en ambos entornos. 
  
La solución de una aplicación basada en WCF es diferente. Para obtener más información, vea la sección Uso  *de varias*  autenticaciones en [Requisitos previos](prerequisites-for-wcf-based-code-samples-in-project.md)para ejemplos de código basados en WCF en Project .
  
## <a name="changing-the-values-of-generic-constants"></a>Modificar los valores de constantes genéricas
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

La mayoría de las muestras tienen una o más variables que necesita actualizar para que la muestra funcione adecuadamente en el entorno. En el siguiente ejemplo, si tiene SSL instalado, use el protocolo HTTPS en lugar del protocolo HTTP. Reemplace  _ServerName_ por el nombre del servidor que está usando. Reemplace  _ProjectServerName_ por el nombre del directorio virtual del sitio de Project Server, como PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Cualquier otra variable que deba cambiar o cualquier otro requisito previo se indica en la parte superior del ejemplo de código.
  
## <a name="verifying-the-results"></a>Comprobar los resultados
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Obtener e interpretar los resultados de una muestra de código no es siempre sencillo. Por ejemplo, si crea un proyecto, debe publicarlo antes de que aparezca en la página Centro de proyectos de Project Web App.
  
Puede verificar los resultados de muestra de código de varias formas, por ejemplo:
  
- Use el cliente de Project Professional 2013 para abrir el proyecto desde el equipo de Project Server y ver los elementos que desee.
    
- Ver proyectos publicados en la página Centro de proyectos de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Ver el registro de cola en Project Web App. Abra la página Configuración  del servidor (elija el icono Configuración  en la esquina superior derecha) y, a continuación, elija Mis trabajos en cola en la sección **Configuración personal** ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). En la lista desplegable **Vista**, puede ordenar por el estado de trabajo. El estado predeterminado **Trabajos fallidos y en progreso en la última semana**. 
    
- Use la página Configuración del servidor en Project Web App ( ) para administrar todos los trabajos en cola y eliminar o forzar la `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` comprobación de objetos de empresa. Asegúrese de tener los permisos administrativos para obtener acceso a aquellos enlaces de la página Configuración del servidor.
    
- Use **Microsoft SQL Server Management Studio** para usar una consulta en una tabla de una base de datos de Project. Por ejemplo, use la siguiente consulta para seleccionar las 200 filas superiores de la tabla pub.MSP_WORKFLOW_STAGE_PDPS para mostrar información sobre las páginas de detalles de proyectos (PDP) en etapas de flujo de trabajo. 
    
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

## <a name="cleaning-up"></a>Limpieza
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

Después de probar algunas muestras de código, existen configuraciones y objetos de empresa que deberían eliminarse o restablecerse. Puede usar la página Configuración del servidor en Project Web App para administrar datos empresariales ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Los vínculos en la página Configuración de servidor le permiten eliminar elementos viejos, forzar la protección de proyectos, administrar la cola de trabajo para todos los usuarios y hacer otras tareas administrativas.
  
A continuación aparecen algunos de los vínculos de la página Configuración de servidor que puede usar para actividades típicas de limpieza después de usar muestras de código:
  
- **Campos personalizados de empresa y tablas de búsqueda**
    
- **Administrar trabajos en cola**
    
- **Eliminación de objetos de empresa**
    
- **Forzar protección de objetos de la empresa**
    
- **Tipos de proyecto empresarial**
    
- **Fases de flujo de trabajo**
    
- **Etapas de flujo de trabajo**
    
- **Páginas de detalles del proyecto**
    
- **Períodos de presentación de informes de horas**
    
- **Configuración y valores predeterminados del parte de horas**
    
- **Clasificaciones de línea**
    
SharePoint Server 2013 administra la configuración adicional para cada instancia de Project Web App, en lugar de hacerlo mediante una página específica de configuración del servidor de Project Web App. En la aplicación Administración central de SharePoint, elija Configuración de aplicación **general,** elija Administrar en Configuración de **Project Server** y, a continuación, elija la instancia de Project Web App en la lista desplegable de la página Configuración del servidor.  Por ejemplo, elija **Controladores de** eventos del lado servidor para agregar o eliminar controladores de eventos para la instancia de Project Web App seleccionada. 
  
## <a name="see-also"></a>Consulte también
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Requisitos previos de muestras de código basadas en WCF en Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Usar la suplantación con WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Descripción general de referencia de PSI de Project](project-psi-reference-overview.md)
- [Centro para desarrolladores de SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

