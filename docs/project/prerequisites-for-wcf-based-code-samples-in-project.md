---
title: Requisitos previos de muestras de código basadas en WCF en Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Obtenga información para ayudarle a crear proyectos en Visual Studio usando los ejemplos de código basados en WCF que se incluyen en los temas de referencia de Project Server Interface (PSI).
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357179"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Requisitos previos de muestras de código basadas en WCF en Project

Obtenga información para ayudarle a crear proyectos en Visual Studio usando los ejemplos de código basados en WCF que se incluyen en los temas de referencia de Project Server Interface (PSI).
   
Muchos de los ejemplos de código basados en WCF incluidos en la biblioteca de clases y la referencia del servicio web de [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) se crearon originalmente para la documentación para desarrolladores de Project 2010 y usan un formato estándar para los servicios web WCF. Los ejemplos siguen funcionando en Project Server 2013 y están diseñados para copiarse en una aplicación de consola y ejecutarse como una unidad completa. Las excepciones están señaladas en la muestra. 
  
Los ejemplos de código de la documentación para desarrolladores de Project 2013 que no han cambiado con respecto a los ejemplos desarrollados para Office Project Server 2007 usan servicios web ASMX. Las muestras basadas en ASMX también pueden adaptarse para utilizar servicios de WCF. Este artículo muestra cómo utilizar las muestras con servicios de WCF. Para obtener información sobre cómo usar los ejemplos con servicios web ASMX, vea Requisitos previos para ejemplos de código basados en [ASMX en Project.](prerequisites-for-asmx-based-code-samples-in-project.md)
  
> [!NOTE]
> Si el modelo de objeto de cliente (CSOM) incluye los métodos que su aplicación necesita, deberían desarrollarse nuevas aplicaciones con el CSOM. El CSOM permite a las aplicaciones trabajar con Project Online o una instalación local de Project Server 2013. De lo contrario, si su aplicación usa la PSI, debería usar la interfaz de WCF, que es la tecnología que recomendamos para las comunicaciones de red. Las aplicaciones que usan la interfaz ASMX o wcf solo pueden funcionar para instalaciones locales de Project Server 2013. 
>
> Para obtener más información acerca del CSOM, vea La arquitectura de [Project Server 2013](project-server-2013-architecture.md) y el modelo de objetos del lado cliente [(CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de ejecutar las muestras de código, debe configurar el entorno de desarrollo, configurar la aplicación y agregar un archivo de configuración de servicio (o configurar los servicios de WCF de forma programada) y cambiar valores constantes genéricos para que coincidan con su entorno.
  
## <a name="setting-up-the-development-environment"></a>Configuración del entorno de desarrollo
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configurar un sistema de Project Server de prueba.**
    
    Use un sistema de Project Server de prueba siempre que haga un desarrollo o una prueba. Incluso cuando su código funcione perfectamente, las dependencias entre proyectos, los informes u otros factores de entorno pueden generar consecuencias no esperadas. 
    
    > [!NOTE]
    > Asegure que es un usuario válido en el servidor y compruebe que posee los permisos suficientes para las llamadas de la PSI que utilice su aplicación. El tema de la documentación de desarrollador para cada método de PSI incluye una tabla de permisos de Project Server. Por ejemplo, el [método Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requiere el permiso global **NewProject** y **el permiso SaveProjectTemplate.** 
  
    En algunos casos, quizás deba hacer una depuración remota en el servidor. También puede que tenga que configurar un controlador de eventos instalando un ensamblado de controlador de eventos en cada equipo de Project Server en la granja de servidores de SharePoint y, a continuación, configurando el controlador de eventos para la instancia de Project Web App mediante la página Configuración de Project Server en la Configuración de aplicación general de Administración central de SharePoint.
    
2. **Configurar un PC de desarrollo.**
    
    Generalmente obtiene acceso a la PSI a través de una red. Las muestras de código están diseñadas para usarse en un cliente independiente del servidor, excepto cuando se indique lo contrario.
    
    1. **Instale la versión correcta de Visual Studio.** Excepto cuando se lo especifique, las muestras de código se escriben en Visual C#. Se pueden usar con Visual Studio 2010 o Visual Studio 2012. Asegúrese de tener instalado el Service Pack más reciente. 
    
    2. **Copie los DLL de Project Server en el PC de desarrollo.** Copie los ensamblados siguientes del equipo de  `[Program Files]\Microsoft Office Servers\15.0\Bin` Project Server en el equipo de desarrollo: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Para obtener información sobre cómo compilar y utilizar el ensamblado de proxy ProjectServerServices.dll para los servicios de WCF en la PSI, consulte [Uso de un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Instalar los archivos de IntelliSense.**
    
    Para usar descripciones de IntelliSense para clases y miembros en ensamblados de Project Server, copie los archivos XML de IntelliSense actualizados de la descarga del SDK de Project 2013 en el mismo directorio donde se encuentran los ensamblados de Project Server. Por ejemplo, copie el archivo Microsoft.Office.Project.Server.Library.xml al directorio donde su aplicación establecerá una referencia al ensamblado Microsoft.Office.Project.Server.Library.dll.
    
    IntelliSense descripciones para los servicios de PSI requieren que cree un ensamblado de proxy de PSI mediante el script CompileWCFProxyAssembly.cmd en el subdirectorio de la descarga del SDK de  `Documentation\IntelliSense\WCF` Project 2013. La secuencia de comandos crea el ensamblado de proxy ProjectServerServices.dll basado en WCF. Para obtener más información, consulte el archivo [ReadMe_IntelliSense].mht en la descarga de SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Crear la aplicación y agregar una referencia de servicio
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Crear una aplicación de consola.**
    
    Cuando crea una aplicación de consola, en la lista desplegable del cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4**. Puede copiar el código de ejemplo de PSI en la nueva aplicación.
    
2. **Agregar referencias requeridas para WCF.**
    
    En Solution Explorer, agregue una referencia a **System.ServiceModel** (consulte Figura 1). Una aplicación web utilizaría **System.ServiceModel.Web**.
    
    También agregue una referencia a **System.Runtime.Serialization**.
    
    **Figura 1. Agregar las referencias en Visual Studio para una aplicación basada en WCF**

    ![Adición de referencias para WCF]agregar referencias para(media/pj15_PrerequisitesWCF_AddReference.gif "WCF")
  
3. **Copiar el código**.
    
    Copie el ejemplo de código completo en el archivo Program.cs de la aplicación de consola.
    
4. **Establecer el espacio de nombre para la aplicación de muestra.**
    
    Puede cambiar el espacio de nombres que aparece en la parte superior de la muestra por el espacio de nombres predeterminado de la aplicación o bien cambiar el espacio de nombres de la aplicación predeterminado para que coincida con la muestra. Puede cambiar el espacio de nombres de la aplicación predeterminado modificando las propiedades de la aplicación. 
    
    Por ejemplo, el ejemplo de código [de ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) tiene el espacio de nombres **Microsoft.SDK.Project.Samples.CreateResourceTest**. Si el nombre del proyecto de Visual Studio es **ResourceTest**, copie el espacio de nombre desde el archivo Program.cs y, a continuación, abra el panel **Propiedades** del proyecto (en el menú **Proyecto**, elija **Propiedades de ResourceTest**). En la ficha **Aplicación**, copie el espacio de nombre en el cuadro de texto **Espacio de nombre predeterminado**. 
    
5. **Establecer las referencias de servicio.**
    
    Muchos ejemplos requieren una referencia a uno o más de los servicios de la PSI. Estos aparecen en la muestra misma o en comentarios que preceden a la muestra. Para obtener el espacio de nombre correcto de las referencias de servicio, asegúrese de establecer primero el espacio de nombre de la aplicación predeterminado.
    
    Existen tres maneras de agregar una referencia de servicio de WCF:
    
    - Cree un ensamblado de proxy de PSI llamado ProjectServerServices.dll y, a continuación, establezca una referencia al ensamblado. Consulte [Uso de un ensamblado de proxy de PSI y de descripciones de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Agregue un archivo de proxy desde la salida svcutil.exe a la solución de Visual Studio. Consulte [Agregar un archivo de proxy de PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Agregue una referencia de servicio utilizando Virtual Studio. Consulte [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference)
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Uso de un ensamblado de proxy de PSI y de descripciones de IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Puede utilizar un ensamblado de proxy para todos los servicios de WCF en la PSI. Compile el ProjectServerServices.dll proxy mediante el script de la descarga del SDK de Project 2013 y, a continuación, copie el ensamblado  `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` de proxy en el equipo de desarrollo. Copie el archivo ProjectServerServices.xml para IntelliSense en la misma ubicación. En Visual Studio, establezca una referencia al ensamblado de proxy ProjectServerServices.dll. 
  
Para las actualizaciones y los Service Packs de Project Server, puede actualizar los archivos de origen de proxy y crear un nuevo ensamblado de proxy utilizando la secuencia de comando GenWCFProxyAssembly.cmd en la misma carpeta de descarga de SDK. Para obtener un vínculo a la descarga del SDK, vea la documentación para desarrolladores de [Project 2013.](project-2013-developer-documentation.md) Para obtener más información, consulte la sección [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference). 
  
> [!NOTE]
> Al extraer los archivos de origen proxy del archivo Source.zip, los archivos de la carpeta están actualizados a partir de la fecha de publicación de la descarga del SDK de  `Documentation\IntelliSense\WCF\Source` Project 2013. Para generar archivos de origen de proxy de PSI actualizados, ejecute la secuencia de comando GenASMXProxyAssembly.cmd en el equipo de Project Server. Para obtener más información, consulte [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Los scripts de la  `Documentation\IntelliSense\ASMX` carpeta no funcionan con aplicaciones basadas en WCF. La secuencia de comandos The GenASMXProxyAssembly.cmd llama a Wsdl.exe, lo cual genera archivos de código de origen para los servicios ASMX. Los archivos de proxy de ASMX incluyen diferentes clases y propiedades. Por ejemplo, el servicio web de Recurso basado en ASMX incluye la clase de **Resource**, mientras que el servicio de Recurso basado en WCF incluye la interfaz de **Resource**, la interfaz de **ResourceChannel** y la clase de **ResourceClient**. 
  
Los espacios de nombre arbitrarios creados tanto para los servicios web de ASMX como para los servicios de WCF son los mismos, de manera que el archivo ProjectServerServices.xml para IntelliSense funciona con ambos ensamblados. Por ejemplo, el espacio de nombre del servicio Recurso en el ensamblado de proxy basado en WCF y en el ensamblado de proxy basado en ASMX es **SvcResource**. Por supuesto, puede modificar los nombres de los espacios de nombre, si se asegura de que coinciden en el ensamblado de proxy y en el archivo ProjectServerServices.xml de IntelliSense.
  
Si una muestra de código utiliza un nombre diferente para un espacio de nombre de servicio de PSI, por ejemplo **ProjectWebSvc**, para que funcione IntelliSense debe cambiar la muestra para que utilice **SvcProject** de manera que el espacio de nombre coincida con el ensamblado de proxy. 
  
Algunas ventajas del uso del ensamblado de proxy basado en WCF son las siguientes:
  
- Puede desarrollar la mayoría de las soluciones con el ensamblado de proxy en un equipo distinto del equipo de Project Server. Establecer una referencia de servicio individual requiere desarrollo en el equipo de Project Server.
    
- El ensamblado de proxy incluye todos los espacios de nombre de servicio de PSI, entonces no tiene que agregar varios archivos de proxy.
    
- Si agrega el archivo ProjectServerServices.xml al mismo directorio donde estableció una referencia al ensamblado de proxy ProjectServerServices.dll, puede obtener descripciones de IntelliSense para los miembros y las clases de PSI. Para obtener más información, vea el archivo [ReadMe_IntelliSense] en la carpeta de la descarga del SDK de  `Documentation\IntelliSense` Project 2013. 
    
**Figura 2. Uso de IntelliSense para acceder a un método en el servicio de Recurso**

![Uso de IntelliSense para el método ReadResource Mediante](media/pj15_PrerequisitesWCF_Intellisense.gif "IntelliSense para el método ReadResource")
  
Las desventajas de utilizar el ensamblado de proxy son que la solución es mayor y debe distribuir e instalar el ensamblado de proxy con la solución. También debe utilizar los mismos espacios de nombre que se encuentran en el ensamblado de proxy y los archivos de IntelliSense, a menos que cambie la secuencia de comandos para crear un ensamblado de proxy y cambie el archivo ProjectServerServices.xml de IntelliSense para utilizar distintos espacios de nombre.
  
### <a name="adding-a-psi-proxy-file"></a>Agregar un archivo de proxy de PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

La descarga del SDK de Project 2013 incluye los archivos de origen generados por el comando SvcUtil.exe para el ensamblado de proxy. Los archivos de origen se encuentran en Source.zip archivo en el  `Documentation\IntelliSense\WCF` subdirectorio. En lugar de establecer una referencia al ensamblado de proxy, puede agregar uno o más archivos de origen a una solución de Visual Studio. Por ejemplo, para utilizar el servicio de Project y el servicio de Recurso, agregue los archivos wcf.Project.cs y wcf.Resource.cs a la solución. 
  
En WCF, la clase primaria en cada servicio de PSI se define por una interfaz y se implementa en una clase de cliente para acceder a los miembros. Por ejemplo, la interfaz de **SvcProject.Resource** se implementa en la clase de **SvcProject.ResourceClient**. Para definir un objeto de **ResourceClient** como una variable de clase llamada **resourceClient**, por ejemplo, utilice el siguiente código. En el ejemplo, el método **SetClientEndpoints** crea un objeto de **resourceClient** que utiliza el extremo **basicHttp_Project**, que se define en el archivo app.config. Para obtener más información sobre el archivo app.config, consulte la sección [Agregar un archivo de configuración de servicio](#pj15_PrerequisitesWCF_AddConfig). 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> Si utiliza un ensamblado de proxy de PSI o agrega un archivo de proxy para una referencia de servicio de Project llamada **SvcResource**, utilizaría el mismo código para crear y descartar un objeto de **resourceClient**. 
  
### <a name="adding-a-service-reference"></a>Adición de una referencia de servicio
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Si no utiliza el ensamblado de proxy basado en WCF o agrega un archivo de proxy para un servicio de PSI, puede establecer una o más referencias de servicio individual directamente en Visual Studio. También puede usar el paso 1 del siguiente procedimiento para crear archivos proxy actualizados, para prepararse para el script que se incluye en la descarga del SDK de  `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` Project 2013. 
  
> [!NOTE]
> Para establecer una referencia de servicio, debe utilizar Visual Studio en el equipo de Project Server. Recomendamos que utilice el ensamblado de proxy ProjectServerServices.dll o agregue archivos de origen de proxy, en lugar de agregar directamente referencias de servicio en Visual Studio. 
  
Los pasos siguientes muestran cómo establecer una referencia de servicio mediante Visual Studio 2012 en un equipo que ejecuta una instalación de prueba de Project Server:
  
1. Para obtener acceso a los servicios de WCF back-end, ejecute Visual Studio en el equipo de Project Server.
    
2. En **Solution Explorer**, haga clic con el botón secundario en la carpeta **Referencias** y, a continuación, seleccione **Agregar referencia de servicio**. 
    
3. En el **cuadro de diálogo**  Agregar referencia de servicio, en el cuadro de texto Dirección, escriba https://localhost:32843/ _GUID_/psi/ _ServiceName_.svc y, a continuación, presione **Entrar**. Reemplace  _EL GUID_ por el nombre del directorio virtual de la aplicación de servicio de Project Server, como 534c37eb00d74ccfadcecf9827e95239. Reemplace  _ServiceName_ por el nombre del servicio, como Recurso (vea la figura 3). 
    
   Puede obtener el nombre del directorio virtual del servicio de Project Server de una de las siguientes maneras:
    
   - Abra la aplicación de Administración central de SharePoint 2013 en el explorador. Elija **Administrar aplicaciones de servicio** y luego elija la aplicación de servicio de PSI de Project Server que desee. Por ejemplo, elija **ProjectServerService**. La dirección URL de la página Administrar sitios de Project Web App contiene el nombre del directorio virtual. Por ejemplo, en  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239` , el nombre del directorio virtual es (el nombre del directorio no contiene  `534c37eb00d74ccfadcecf9827e95239` guiones). 
    
   - Abra el cuadro de diálogo **Administrador de Servicios de información de internet (IIS)** en el equipo de Project Server. Expanda el nodo **Servicios web de SharePoint** en el panel **Conexiones** y, a continuación, expanda los directorios virtuales de servicio debajo de eso, hasta que encuentra el directorio que incluye una carpeta de PSI. Seleccione el directorio, elija **Configuración avanzada** en el panel **Acciones** y, a continuación, copie el nombre del directorio en el campo **Ruta virtual**. 
    
      > [!NOTE]
      > Puede haber más de un directorio virtual de servicio de Project Server. Asegúrese de elegir el directorio virtual que contiene la instancia de Project Web App que desee. 
  
   - Use el cmdlet **get-SPServiceApplication** en Windows PowerShell que está instalado con SharePoint 2013. En la barra de tareas del menú **Inicio**, elija **Todos los programas**, seleccione **Productos de Microsoft SharePoint 2013** y, a continuación, elija **SharePoint 2013 Management Shell**. A continuación verá el comando y los resultados en la ventana de **SharePoint 2013get- Management Shell** para las aplicaciones de servicio definidas (sus GUID serán diferentes). Copie el GUID para la aplicación de servicio de Project Server. 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Si conoce el nombre completo de la aplicación de servicio de Project Server, puede utilizarlo para obtener el valor de GUID, por ejemplo:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Elimine los guiones del GUID para obtener el nombre del directorio virtual. 
  
   Las direcciones URL como son  `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` estándar para los servicios de Project Server. 
    
4. Una vez que se resuelve la referencia de servicio, escriba el nombre de la referencia en el cuadro de texto **Espacio de nombre**. Los ejemplos de código de la documentación para desarrolladores de Project 2013 usan el nombre de espacio de nombres arbitrario **Svc _ServiceName_**. Por ejemplo, el servicio Recurso en los ejemplos de código se llama **SvcResource**.
    
    **Figura 3. Agregar la referencia de servicio de Recurso basada en WCF**

    ![Adición de la referencia de servicio de recursos basada en WCF]agregando la referencia de servicio de recursos basada en(media/pj15_PrerequisitesWCF_AddSvcReference.gif "WCF")
  
5. Reemplace el archivo de web.config temporal en el directorio del servicio de project por el original (cuyo nombre se ha cambiado a web.config) y, a continuación, vuelva a ejecutar  `iisreset` .
    
## <a name="setting-other-references"></a>Estableciendo otras referencias
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Las aplicaciones de Project Server suelen usar otros servicios, como los servicios web de SharePoint 2013. Si se requieren otros servicios u otras referencias, se lo señala en el ejemplo de código.
  
Las referencias locales para la muestra de código aparecen en las declaraciones de **using** en la parte superior de la muestra. 
  
1. En **Solution Explorer**, haga clic con el botón secundario en la carpeta **Referencias** y, a continuación, seleccione **Agregar referencia**.
    
2. Seleccione **Examinar** y, a continuación, diríjase a la ubicación donde ha almacenado los DLL de Project Server que copió previamente. Elija los DLL que desee y luego seleccione **Aceptar**.
    
> [!NOTE]
> Asegúrese de que las versiones de ensamblado en su equipo de desarrollo coinciden exactamente con aquellas del equipo de Project Server de destino. 
  
## <a name="adding-a-service-configuration-file"></a>Agregar un archivo de configuración de servicio
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Si una aplicación configura de forma programada los servicios de WCF, no utiliza un archivo de configuración de servicio. De lo contrario, una aplicación de Windows o una aplicación de consola usa el **elemento system.serviceModel** en un app.config archivo; una aplicación web incluye **system.serviceModel** en web.config. Para obtener más información acerca de cómo usar un archivo app.config o configurar mediante programación los servicios WCF, vea [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Cuando genera un archivo de origen de proxy de servicio, el comando SvcUtil.exe también crea un archivo output.config que es la base para el elemento **system.serviceModel** predeterminado en un archivo app.config o un archivo web.config. La descarga del SDK de Project 2013 incluye un ejemplo output.config archivo en  `Documentation\IntelliSense\WCF\Source.zip` . Por ejemplo, el archivo output.config predeterminado que crea SvcUtil.exe para el servicio de Recurso incluye dos enlazados, llamados **BasicHttpBinding_Resource** y **BasicHttpBinding_Resource1**. El elemento **client** incluye dos extremos predeterminados. Un extremo es para el acceso seguro a la dirección HTTP en el puerto 32843 y el otro es para el acceso normal en el puerto 32843, de la manera siguiente: 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

La configuración de servicio de PSI no utiliza los extremos y enlazados predeterminados. Project Server requiere que las aplicaciones accedan a los servicios de PSI a través de ProjectServer.svc front-end, que actúa como un enrutador para llamadas a los servicios back-end. Para crear el archivo app.config, realice los siguientes pasos:
  
1. Si establece una referencia al ensamblado de proxy de ProjectServerServices.dll o agrega el archivo de origen de proxy para un servicio, la aplicación no contiene un archivo app.config. Agregue un nuevo elemento al proyecto de Visual Studio. En el **cuadro de diálogo**  Agregar nuevo elemento, elija la plantilla Archivo de configuración de aplicación, así mismo app.config y, a continuación, **elija Agregar**.
    
2. Elimine todo el texto del archivo app.config y luego copie el siguiente código en el archivo. Puede usar el mismo enlace, por  `basicHttpConf` ejemplo, para cada extremo de servicio. Si desea utilizar más de un enlazado, por ejemplo, para enlazar los protocolos tanto HTTP como HTTPS, debe crear un enlazado para cada protocolo.
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Reemplace  `ServerName/ProjectServerName` la dirección del extremo del cliente por el nombre del servidor y la instancia de Project Web App. 
    
4. Reemplace  `ServiceName` por el nombre del servicio de PSI, como Resource. Asegúrese de reemplazar las tres instancias del nombre de servicio, por ejemplo:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Para utilizar más de un servicio de PSI, cree un elemento **endpoint** para cada servicio y para cada elemento **binding** que utiliza el servicio. Por ejemplo, los siguientes extremos configuran el cliente que utilizará el enlazado HTTP básico para el servicio de Project y el servicio de QueueSystem. 
    
    > [!NOTE]
    > Si ejecuta una aplicación y obtiene un error de que el servidor está demasiado ocupado o de que la solicitud de HTTP no está autorizada, asegúrese de que las direcciones de extremo sean correctas en el archivo app.config. 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Puede editar un archivo app.config utilizando el **Editor de configuración de servicio de WCF** en Visual Studio (en el menú **Herramientas**). La Figura 4 muestra cómo establecer el elemento **contract** en el cuadro de diálogo **Editor de configuración de servicio de Microsoft**. Si la solución usa el ensamblado de proxy de PSI, abra ProjectServerServices.dll en el  `bin\debug` directorio de la solución Visual Studio cliente. El cuadro de diálogo **Explorador de tipo de contrato** muestra todos los contratos de servicio de WCF (vea la Figura 5). 
  
**Figura 4. Uso del Editor de configuración de servicio de WCF**

![Uso del Editor de configuración del servicio WCF]mediante el Editor de configuración del servicio(media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "WCF")
  
Si la solución usa un archivo proxy de servicio, como wcfResource.cs, compile la aplicación y, a continuación, abra el archivo ejecutable en el  `bin\debug` directorio. Para obtener más información sobre la edición del archivo app.config, consulte [Tutorial: Desarrollo de aplicaciones de PSI utilizando WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figura 5. Uso del Explorador de tipo de contrato en el Editor de configuración de servicio de WCF**

![Uso del explorador de tipo de contrato]mediante el explorador de tipo de(media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "contrato")
  
## <a name="using-multiple-authentication"></a>Usar autenticación múltiple
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

La autenticación de usuarios de Project Server locales, ya sea por autenticación de Windows o por autenticación de formas, ser realiza a través de reclamos que se procesan en SharePoint. La autenticación múltiple significa que la aplicación web en la que se aprovisiona Project Web App admite la autenticación de Windows y la autenticación basada en formularios. Si ese es el caso, cualquier llamada a un servicio de WCF que utilice la autenticación de Windows fallará con el siguiente error, porque el proceso de reclamos no puede determinar qué tipo de usuario autenticar:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Para solucionar el problema para WCF, todas las llamadas a los métodos de PSI deberían estar dentro de un **OperationContextScope** que se define para cada servicio de PSI. No anide ámbitos para varios servicios; por ejemplo, al usar llamadas a los servicios de Project y Recurso, cada conjunto de llamadas debería estar dentro de su propio ámbito. 
  
En el siguiente ejemplo, el método **DisableFormsAuth** puede llamarse desde cada sección de **OperationContextScope** en una aplicación. El método quita cualquier valor de encabezado que anteriormente deshabilitó la autenticación de formularios, de modo que la autenticación de formularios pueda continuar si el parámetro  _isWindowsAuth_ es **false**. Si  _isWindowsAuth es_ **true**, el **método DisableFormsAuth** deshabilita la autenticación de formularios. 
  
En el método **WcfSample**, el objeto **projectClient** es una instancia de la clase **SvcProject.ProjectClient** de PSI. 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> La realización de llamadas de PSI dentro de un **OperationContextScope** es necesario solo para aplicaciones que se ejecutan en un entorno de varias autenticaciones. Si Project Server utiliza solamente la autenticación de Windows, no es necesario establecer un ámbito y agregar un encabezado de solicitud web que deshabilite la autenticación de formas. 
> 
> La solución de una aplicación basada en ASMX es diferente. Para obtener más información, vea la sección Uso *de autenticación* múltiple en Requisitos previos para ejemplos de código basados en [ASMX en Project.](prerequisites-for-asmx-based-code-samples-in-project.md) 
  
## <a name="changing-values-of-generic-constants"></a>Modificar valores de constantes genéricas
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

La mayoría de las muestras tienen una o más variables que necesita actualizar para que la muestra funcione adecuadamente en el entorno. En el siguiente ejemplo, si tiene SSL instalado, use el protocolo HTTPS en lugar del protocolo HTTP. Reemplace  _ServerName_ por el nombre del servidor que está usando. Reemplace  _ProjectServerName_ por el nombre del directorio virtual del sitio del servidor de proyectos, como PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Cualquier otra variable que deba cambiar se señala en la parte superior del ejemplo de código.
  
## <a name="verifying-the-results"></a>Comprobación de los resultados:
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Obtener e interpretar los resultados de una muestra de código no es siempre sencillo. Por ejemplo, si crea un proyecto, debe publicarlo para que pueda aparecer en la página Centro de proyectos de Project Web App.
  
Puede verificar los resultados de muestra de código de varias formas, por ejemplo:
  
- Use el cliente de Project Professional 2013 para abrir el proyecto desde el equipo de Project Server y ver los elementos que desee.
    
- Ver proyectos publicados en la página Centro de proyectos de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Ver el registro de cola en Project Web App. Abra la página Configuración  del servidor (elija el icono Configuración  en la esquina superior derecha) y, a continuación, elija Mis trabajos en cola en la sección **Configuración personal** ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). En la lista desplegable **Vista**, puede ordenar por el estado de trabajo. El estado predeterminado **Trabajos fallidos y en progreso en la última semana**. 
    
- Use la página Configuración del servidor en Project Web App ( ) para administrar todos los trabajos en cola y eliminar o forzar la `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` comprobación de objetos de empresa. Debe tener los permisos administrativos para acceder a aquellos enlaces de la página de Configuración del servidor.
    
- Utilice **Microsoft SQL Server Management Studio** para ejecutar una consulta en una tabla de una base de datos de Project Server. Por ejemplo, utilice la siguiente consulta para seleccionar las 200 filas superiores de la tabla MSP_WORKFLOW_STAGE_PDPS para mostrar información sobre las páginas de detalles de proyectos (PDP) en etapas de flujo de trabajo. 
    
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
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Después de probar algunas muestras de código, existen configuraciones y objetos de empresa que deberían eliminarse o restablecerse. Puede usar la página Configuración del servidor en Project Web App para administrar datos empresariales ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Los enlaces en la página de Configuración de servidor le permiten eliminar elementos viejos, forzar la protección de proyectos, administrar la cola de trabajo para todos los usuarios y realizar otras tareas administrativas.
  
A continuación aparecen algunos de los enlaces de la página Configuración de servidor para utilizar para actividades típicas de limpieza después de ejecutar muestras de código:
  
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

- [Requisitos previos para los ejemplos de código basados en ASMX en Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Tutorial: desarrollo de aplicaciones de PSI mediante WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Usar la suplantación con WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Descripción general de referencia de PSI de Project](project-psi-reference-overview.md) 
- [Centro para desarrolladores de SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

