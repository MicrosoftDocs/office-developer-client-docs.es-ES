---
title: Requisitos previos para ejemplos de código basados en WCF en Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Obtenga información para ayudarle a crear proyectos en Visual Studio mediante el uso de los ejemplos de código basados en WCF que se incluyen en los temas de referencia de Project Server Interface (PSI).
ms.openlocfilehash: 43700a9db4445dacf366c7ca2efe1bfb10914372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821440"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Requisitos previos para ejemplos de código basados en WCF en Project

Obtenga información para ayudarle a crear proyectos en Visual Studio mediante el uso de los ejemplos de código basados en WCF que se incluyen en los temas de referencia de Project Server Interface (PSI).
   
Muchos de los ejemplos de código basados en WCF incluidos en la [referencia de servicio de web y biblioteca de clase de Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) se crearon originalmente para la documentación para desarrolladores de Project 2010 y utilizan un formato estándar para los servicios web de WCF. Los ejemplos de aún funcionan en Project Server 2013 y están diseñados para ser copiado en una aplicación de consola y se ejecute como una unidad completa. En el ejemplo se indican excepciones. 
  
Ejemplos de código en la documentación para desarrolladores de Project 2013 que se han modificado en los ejemplos de desarrollado para Office Project Server 2007 usan servicios Web de ASMX. Los ejemplos basados en ASMX también puede adaptarse a usar los servicios de WCF. En este artículo se muestra cómo usar los ejemplos con los servicios de WCF. Para obtener información acerca de cómo usar los ejemplos con servicios web de ASMX, vea [requisitos previos para ejemplos de código basados en ASMX en Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Si el modelo de objetos de cliente (COM) incluye los métodos que requiere la aplicación, se deben desarrollar nuevas aplicaciones con el CSOM. El CSOM permite a las aplicaciones trabajar con Project Online o una instalación local de Project Server 2013. De lo contrario, si la aplicación utiliza la interfaz PSI, que debe usar la interfaz WCF, que es la tecnología que se recomienda para las comunicaciones de red. Las aplicaciones que usan la interfaz ASMX o la interfaz WCF pueden trabajar solo para instalaciones locales de Project Server 2013. 
>
> Para obtener más información sobre el CSOM, consulte [arquitectura de Project Server 2013](project-server-2013-architecture.md) y [modelo de objetos de cliente (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de ejecutar las muestras de código, debe configurar el entorno de desarrollo, configurar la aplicación y agregar un archivo de configuración de servicio (o configurar los servicios de WCF de forma programada) y cambiar valores constantes genéricos para que coincidan con su entorno.
  
## <a name="setting-up-the-development-environment"></a>Configurar el entorno de desarrollo
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configurar un sistema de Project Server de prueba.**
    
    Use un sistema de Project Server de prueba siempre que haga un desarrollo o una prueba. Incluso cuando su código funcione perfectamente, las dependencias entre proyectos, los informes u otros factores de entorno pueden generar consecuencias no esperadas. 
    
    > [!NOTE]
    > Asegúrese de que es un usuario válido en el servidor y compruebe que tiene permisos suficientes para las llamadas PSI que usa la aplicación. El tema de la documentación para desarrolladores para cada método PSI incluye una tabla de permisos de Project Server. Por ejemplo, el método [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requiere el permiso **NewProject** global y el permiso **SaveProjectTemplate** . 
  
    En algunos casos, debe realizar la depuración remota en el servidor. También es posible que deba configurar un controlador de eventos mediante la instalación de un ensamblado del controlador de eventos en cada equipo de Project Server en la granja de servidores de SharePoint y, a continuación, configurar el controlador de eventos para la instancia de Project Web App mediante la página Configuración de Project Server en General Configuración de la aplicación de Administración Central de SharePoint.
    
2. **Configurar un PC de desarrollo.**
    
    Generalmente obtiene acceso a la PSI a través de una red. Las muestras de código están diseñadas para usarse en un cliente independiente del servidor, excepto cuando se indique lo contrario.
    
    1. **Instale la versión correcta de Visual Studio.** Excepto donde se indique, los ejemplos de código se escriben en Visual C#. Se pueden usar con Visual Studio 2010 o Visual Studio 2012. Asegúrese de que tiene instalado el service pack más reciente. 
    
    2. **Copie la DLL de Project Server en el equipo de desarrollo.** Copie los siguientes ensamblados de `[Program Files]\Microsoft Office Servers\15.0\Bin` en el equipo de Project Server en el equipo de desarrollo: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Para obtener información sobre cómo compilar y utilizar el ensamblado de proxy ProjectServerServices.dll para los servicios de WCF en la PSI, consulte [Uso de un ensamblado de proxy de PSI y descripciones de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Instalar los archivos de IntelliSense.**
    
    Para usar descripciones de IntelliSense para las clases y miembros en ensamblados de Project Server, copia los archivos XML de IntelliSense actualizados desde el SDK de Project 2013 descargarán en el mismo directorio donde se encuentran los ensamblados de Project Server. Por ejemplo, copie el archivo Microsoft.Office.Project.Server.Library.xml al directorio donde la aplicación establecerá una referencia al ensamblado Microsoft.Office.Project.Server.Library.dll.
    
    Descripciones de IntelliSense para los servicios PSI requieren la creación de un ensamblado de proxy PSI mediante el uso de la secuencia de comandos CompileWCFProxyAssembly.cmd en el `Documentation\IntelliSense\WCF` subdirectorio en la descarga del SDK de Project 2013. El script crea el ensamblado de proxy ProjectServerServices.dll basados en WCF. Para obtener más información, vea el archivo .mht [ReadMe_IntelliSense] en la descarga del SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Crear la aplicación y agregar una referencia de servicio
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Crear una aplicación de consola.**
    
    Cuando crea una aplicación de consola, en la lista desplegable del cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4**. Puede copiar el código de ejemplo de PSI en la nueva aplicación.
    
2. **Agregar referencias requeridas para WCF.**
    
    En el Explorador de soluciones, agregue una referencia a **System.ServiceModel** (vea la figura 1). Una aplicación web usaría **System.ServiceModel.Web**.
    
    También agregue una referencia a **System.Runtime.Serialization**.
    
    **Figura 1. Agregar las referencias en Visual Studio para una aplicación basada en WCF**

    ![Adición de referencias para WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Adición de referencias para WCF")
  
3. **Copiar el código**.
    
    Copie el ejemplo de código completo en el archivo Program.cs de la aplicación de consola.
    
4. **Establecer el espacio de nombres para la aplicación de ejemplo.**
    
    Puede cambiar el espacio de nombres que aparece en la parte superior de la muestra por el espacio de nombres predeterminado de la aplicación o bien cambiar el espacio de nombres de la aplicación predeterminado para que coincida con la muestra. Puede cambiar el espacio de nombres de la aplicación predeterminado modificando las propiedades de la aplicación. 
    
    Por ejemplo, el código de ejemplo para [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) tiene el espacio de nombres **Microsoft.SDK.Project.Samples.CreateResourceTest**. Si el nombre del proyecto de Visual Studio es **ResourceTest**, copie el archivo Program.cs en el espacio de nombres y, a continuación, abra el panel de **Propiedades** del proyecto (en el menú **proyecto** , elija **Propiedades ResourceTest**). En la ficha **aplicación** , copie el espacio de nombres en el cuadro de texto de **espacio de nombres predeterminado** . 
    
5. **Establecer las referencias de servicio.**
    
    Muchos ejemplos requieren una referencia a uno o más de los servicios de la PSI. Estos aparecen en la muestra misma o en comentarios que preceden a la muestra. Para obtener el espacio de nombre correcto de las referencias de servicio, asegúrese de establecer primero el espacio de nombre de la aplicación predeterminado.
    
    Existen tres maneras de agregar una referencia de servicio de WCF:
    
    - Cree un ensamblado de proxy de PSI llamado ProjectServerServices.dll y, a continuación, establezca una referencia al ensamblado. Consulte [Uso de un ensamblado de proxy de PSI y de descripciones de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Agregue un archivo de proxy desde la salida svcutil.exe a la solución de Visual Studio. Consulte [Agregar un archivo de proxy de PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Agregue una referencia de servicio utilizando Virtual Studio. Consulte [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference)
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Usar un ensamblado de proxy de PSI y descripciones de IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Puede usar un ensamblado de proxy para todos los servicios WCF públicos de la PSI. Compilar el ensamblado de proxy ProjectServerServices.dll mediante el uso de la `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` secuencia de comandos en la descarga del SDK de Project 2013 y, a continuación, copie el ensamblado de proxy en el equipo de desarrollo. Copie el archivo ProjectServerServices.xml para IntelliSense en la misma ubicación. En Visual Studio, establezca una referencia al ensamblado de proxy ProjectServerServices.dll. 
  
Para Project Server service packs y actualizaciones, puede actualizar los archivos de origen de proxy y crear un ensamblado de proxy de nuevo mediante el uso de la secuencia de comandos GenWCFProxyAssembly.cmd en la misma carpeta de descarga SDK. Para un vínculo a la descarga del SDK, vea la [documentación para desarrolladores de Project 2013](project-2013-developer-documentation.md). Para obtener más información, vea la sección [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> Al extraer los archivos de origen del proxy de la Source.zip, los archivos de la `Documentation\IntelliSense\WCF\Source` carpeta son actuales a partir de la fecha de publicación de la descarga del SDK de Project 2013. Para generar actualiza los archivos de origen de proxy PSI, ejecute el script GenASMXProxyAssembly.cmd en el equipo de Project Server. Para obtener más información, vea [Agregar una referencia de servicio](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Las secuencias de comandos en el `Documentation\IntelliSense\ASMX` carpeta no funcionan para las aplicaciones basadas en WCF. El script GenASMXProxyAssembly.cmd llama a Wsdl.exe, que genera archivos de código fuente para los servicios ASMX. Los archivos de proxy ASMX incluyen las propiedades y las distintas clases. Por ejemplo, el servicio web de recursos basados en ASMX incluye la clase de **recurso** , mientras que el servicio de recursos basados en WCF incluye la interfaz de **recursos** , la interfaz de **ResourceChannel** y la clase **ResourceClient** . 
  
Los espacios de nombre arbitrarios creados tanto para los servicios web de ASMX como para los servicios de WCF son los mismos, de manera que el archivo ProjectServerServices.xml para IntelliSense funciona con ambos ensamblados. Por ejemplo, el espacio de nombre del servicio Recurso en el ensamblado de proxy basado en WCF y en el ensamblado de proxy basado en ASMX es **SvcResource**. Por supuesto, puede modificar los nombres de los espacios de nombre, si se asegura de que coinciden en el ensamblado de proxy y en el archivo ProjectServerServices.xml de IntelliSense.
  
Si una muestra de código utiliza un nombre diferente para un espacio de nombre de servicio de PSI, por ejemplo **ProjectWebSvc**, para que funcione IntelliSense debe cambiar la muestra para que utilice **SvcProject** de manera que el espacio de nombre coincida con el ensamblado de proxy. 
  
Algunas ventajas del uso del ensamblado de proxy basado en WCF son las siguientes:
  
- Puede desarrollar la mayoría de las soluciones con el ensamblado de proxy en un equipo distinto del equipo de Project Server. Establecer una referencia de servicio individual requiere desarrollo en el equipo de Project Server.
    
- El ensamblado de proxy incluye todos los espacios de nombre de servicio de PSI, entonces no tiene que agregar varios archivos de proxy.
    
- Si se agrega el archivo ProjectServerServices.xml en el mismo directorio donde se establece una referencia al ensamblado de proxy ProjectServerServices.dll, puede obtener descripciones de IntelliSense para las clases PSI y miembros. Para obtener más información, consulte el archivo [ReadMe_IntelliSense] en la `Documentation\IntelliSense` carpeta de la descarga del SDK de Project 2013. 
    
**Figura 2. Uso de IntelliSense para acceder a un método en el servicio de Recurso**

![Uso de Intellisense para el método ReadResource] (media/pj15_PrerequisitesWCF_Intellisense.gif "Uso de Intellisense para el método ReadResource")
  
Las desventajas de utilizar el ensamblado de proxy son que la solución es mayor y debe distribuir e instalar el ensamblado de proxy con la solución. También debe utilizar los mismos espacios de nombre que se encuentran en el ensamblado de proxy y los archivos de IntelliSense, a menos que cambie la secuencia de comandos para crear un ensamblado de proxy y cambie el archivo ProjectServerServices.xml de IntelliSense para utilizar distintos espacios de nombre.
  
### <a name="adding-a-psi-proxy-file"></a>Agregar un archivo de proxy de PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

La descarga del SDK de Project 2013 incluye los archivos de origen que se generan mediante el comando SvcUtil.exe para el ensamblado de proxy. Los archivos de origen se encuentran en el archivo Source.zip en el `Documentation\IntelliSense\WCF` subdirectorio. En lugar de establecer una referencia al ensamblado de proxy, puede agregar uno o varios de los archivos de origen a una solución de Visual Studio. Por ejemplo, para usar el servicio de proyecto y el servicio de recursos, agregue el wcf. Project.cs y wcf. Archivos de Resource.cs a la solución. 
  
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

Si no usa el ensamblado de proxy basados en WCF o agregar un archivo de proxy para un servicio de la PSI, puede establecer una o más referencias de servicio individuales directamente en Visual Studio. También puede usar el paso 1 del siguiente procedimiento para crear archivos de proxy actualizada, para preparar el `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` es decir de secuencias de comandos incluidos en la descarga del SDK de Project 2013. 
  
> [!NOTE]
> Para establecer una referencia de servicio, debe utilizar Visual Studio en el equipo de Project Server. Recomendamos que utilice el ensamblado de proxy ProjectServerServices.dll o agregue archivos de origen de proxy, en lugar de agregar directamente referencias de servicio en Visual Studio. 
  
Los pasos siguientes muestran cómo establecer una referencia de servicio mediante el uso de Visual Studio 2012 en un equipo que ejecuta una instalación de prueba de Project Server:
  
1. Para obtener acceso a los servicios de WCF back-end, ejecute Visual Studio en el equipo de Project Server.
    
2. En **Solution Explorer**, haga clic con el botón secundario en la carpeta **Referencias** y, a continuación, seleccione **Agregar referencia de servicio**. 
    
3. En el cuadro de diálogo **Agregar referencia de servicio** , en el cuadro de texto **dirección** , escriba http://localhost:32843/ _GUID_/psi/ _ServiceName_svc y, a continuación, presione **ENTRAR**. Reemplazar el _GUID_ con el nombre del directorio virtual de la aplicación de servicio de Project Server, como 534c37eb00d74ccfadcecf9827e95239. Reemplace _ServiceName_ con el nombre del servicio, como recurso (vea la figura 3). 
    
   Puede obtener el nombre del directorio virtual del servicio de Project Server de una de las siguientes maneras:
    
   - Abra la aplicación de Administración Central de SharePoint 2013 en el explorador. Elija **Administrar aplicaciones de servicio**y, a continuación, elija la aplicación de servicio de PSI de Project Server que desee. Por ejemplo, elija **ProjectServerService**. La dirección URL de la página Administrar sitios de Project Web App contiene el nombre del directorio virtual. Por ejemplo, en `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, el nombre del directorio virtual es `534c37eb00d74ccfadcecf9827e95239` (el nombre del directorio no contiene guiones). 
    
   - Abra el cuadro de diálogo **Administrador de Servicios de información de internet (IIS)** en el equipo de Project Server. Expanda el nodo **Servicios web de SharePoint** en el panel **Conexiones** y, a continuación, expanda los directorios virtuales de servicio debajo de eso, hasta que encuentra el directorio que incluye una carpeta de PSI. Seleccione el directorio, elija **Configuración avanzada** en el panel **Acciones** y, a continuación, copie el nombre del directorio en el campo **Ruta virtual**. 
    
      > [!NOTE]
      > Puede haber más de un directorio virtual de servicio de Project Server. Asegúrese de elegir el directorio virtual que contiene la instancia de Project Web App que desee. 
  
   - Use el cmdlet **get-SPServiceApplication** en Windows PowerShell que se instala con SharePoint 2013. En el menú **Inicio de** barra de tareas, elija **Todos los programas**, elija **Productos de Microsoft SharePoint 2013**y, a continuación, elija **Consola de administración de SharePoint 2013**. Siguiente es el comando y los resultados en la ventana de la **Consola de administración de SharePoint 2013get -** para las aplicaciones de servicio definido (su GUID será diferente). Copie el GUID de la aplicación de servicio de Project Server. 
    
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
  
   Las direcciones URL como `http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` son estándar para los servicios de Project Server. 
    
4. Una vez que se resuelve la referencia de servicio, escriba el nombre de referencia en el cuadro de texto de **Namespace** . Ejemplos de código en la documentación para desarrolladores de Project 2013 usan el nombre de espacio de nombres arbitrario **Svc _ServiceName_**. Por ejemplo, el servicio de recursos en los ejemplos de código se denomina **SvcResource**.
    
    **Figura 3. Agregar la referencia de servicio de Recurso basada en WCF**

    ![Adición de la referencia de servicio de recursos basados en WCF] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Adición de la referencia de servicio de recursos basados en WCF")
  
5. Reemplace el archivo web.config temporal en el directorio de servicio de Project Server con el original (cambiar el nombre al archivo web.config) y, a continuación, vuelva a ejecutar `iisreset`.
    
## <a name="setting-other-references"></a>Estableciendo otras referencias
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Aplicaciones de Project Server suelen usan otros servicios, como los servicios web de SharePoint 2013. Si se requieren otros servicios o referencias, se indican en el ejemplo de código.
  
Las referencias locales para el ejemplo de código se enumeran en instrucciones **using** en la parte superior de la muestra. 
  
1. En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** y después seleccione **Agregar referencia**.
    
2. Seleccione **Examinar** y, a continuación, diríjase a la ubicación donde ha almacenado los DLL de Project Server que copió previamente. Elija los DLL que desee y luego seleccione **Aceptar**.
    
> [!NOTE]
> Asegúrese de que las versiones de ensamblado en su equipo de desarrollo coinciden exactamente con aquellas del equipo de Project Server de destino. 
  
## <a name="adding-a-service-configuration-file"></a>Agregar un archivo de configuración de servicio
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Si una aplicación configura de forma programada los servicios de WCF, no utiliza un archivo de configuración de servicio. De lo contrario, una aplicación de consola o una aplicación de Windows utiliza el elemento **system.serviceModel** en un archivo app.config; una aplicación web incluye **system.serviceModel** en web.config. Para obtener más información sobre el uso de un archivo app.config o la configuración preprogramada de los servicios de WCF, consulte [Tutorial: desarrollo de aplicaciones de PSI mediante WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Cuando genera un archivo de código fuente del proxy de servicio, el comando SvcUtil.exe también crea un archivo output.config que es la base para el elemento de **system.serviceModel** de forma predeterminada en un archivo app.config o el archivo web.config. La descarga del SDK de Project 2013 incluye un ejemplo de archivo output.config en `Documentation\IntelliSense\WCF\Source.zip`. Por ejemplo, el archivo output.config predeterminado que crea SvcUtil.exe para el servicio de recursos incluye dos enlaces, denominados **BasicHttpBinding_Resource** y **BasicHttpBinding_Resource1**. El elemento de **cliente** incluye dos extremos predeterminados. Es uno de los extremos para el acceso seguro a la dirección HTTP en el puerto 32843 y la otra es para el acceso normal en el puerto 32843, como se indica a continuación: 
  
```XML
<client>
    <endpoint address="http://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="http://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

La configuración de servicio de PSI no utiliza los extremos y enlazados predeterminados. Project Server requiere que las aplicaciones accedan a los servicios de PSI a través de ProjectServer.svc front-end, que actúa como un enrutador para llamadas a los servicios back-end. Para crear el archivo app.config, realice los siguientes pasos:
  
1. Si establece una referencia al ensamblado de proxy ProjectServerServices.dll, o agregar el archivo de origen de proxy para un servicio, la aplicación no contiene un archivo app.config. Agregar un nuevo elemento al proyecto de Visual Studio. En el cuadro de diálogo **Agregar nuevo elemento** , elija la plantilla de **Archivo de configuración de aplicación** , asígnele el nombre app.config y, a continuación, elija **Agregar**.
    
2. Elimine todo el texto en el archivo app.config y, a continuación, copie el código siguiente en el archivo. Puede usar el mismo enlace, por ejemplo `basicHttpConf`, para cada extremo de servicio. Si desea usar más de un enlace, por ejemplo, para enlazar los protocolos HTTP y HTTPS, debe crear un enlace para cada protocolo.
    
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
                                <transport clientCredentialType="Ntlm" realm="http://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="http://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Reemplace `ServerName/ProjectServerName` en la dirección de extremo de cliente con el nombre de su servidor y la instancia de Project Web App. 
    
4. Reemplace `ServiceName` con el nombre de un servicio PSI, como recurso. Asegúrese de que reemplace todas las instancias de tres el nombre del servicio, por ejemplo:
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
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
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Puede editar un archivo app.config mediante el **Editor de configuración del servicio de WCF** en Visual Studio (en el menú **Herramientas** ). La figura 4 muestra cómo se establece el elemento de **contrato** en el cuadro de diálogo **Editor de configuración del servicio de Microsoft** . Si la solución es usar el ensamblado de proxy PSI, abra ProjectServerServices.dll en el `bin\debug` directorio de la solución de Visual Studio. El cuadro de diálogo **Explorador de tipos de contrato** muestra todos los contratos de servicios WCF (vea la figura 5). 
  
**Figura 4. Uso del Editor de configuración de servicio de WCF**

![Uso del Editor de configuración del servicio WCF] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Uso del Editor de configuración del servicio WCF")
  
Si la solución es usar un archivo de proxy de servicio, como wcfResource.cs, compile la aplicación y, a continuación, abra el archivo ejecutable en el `bin\debug` Active directory. Para obtener más información acerca de cómo modificar el archivo app.config, vea [Tutorial: aplicaciones de desarrollo de PSI mediante WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figura 5. Uso del Explorador de tipo de contrato en el Editor de configuración de servicio de WCF**

![Uso del explorador de tipo de contrato] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Uso del explorador de tipo de contrato")
  
## <a name="using-multiple-authentication"></a>Usar autenticación múltiple
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Autenticación de usuarios de Project Server local, ya sea mediante la autenticación de Windows o autenticación de formularios, se realiza a través de notificaciones de procesamiento en SharePoint. Autenticación múltiple significa que la aplicación web en el que se ha aprovisionado Project Web App admite la autenticación de Windows y autenticación basada en formularios. Si ese es el caso, se producirá un error en cualquier llamada a un servicio WCF que usa la autenticación de Windows con el siguiente error, debido a que el proceso de notificaciones no puede determinar qué tipo de usuario para autenticar:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Para solucionar el problema para WCF, todas las llamadas a los métodos de PSI deberían estar dentro de un **OperationContextScope** que se define para cada servicio de PSI. No anide ámbitos para varios servicios; por ejemplo, al usar llamadas a los servicios de Project y Recurso, cada conjunto de llamadas debería estar dentro de su propio ámbito. 
  
En el ejemplo siguiente, el método **DisableFormsAuth** se puede llamar desde cada sección **OperationContextScope** en una aplicación. El método quita cualquier valor de encabezado que se deshabilitó anteriormente autenticación mediante formularios, por lo que la autenticación de formularios puede continuar si el parámetro _isWindowsAuth_ es **false**. Si _isWindowsAuth_ es **true**, el método **DisableFormsAuth** deshabilita la autenticación de formularios. 
  
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
> La corrección para una aplicación basada en ASMX es diferente. Para obtener más información, vea la sección *uso de la autenticación de varios* de [los requisitos previos para ejemplos de código basados en ASMX en Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Modificar valores de constantes genéricas
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Mayoría de los ejemplos tiene una o más variables que se debe actualizar para que el ejemplo funcione correctamente en su entorno. En el siguiente ejemplo, si tiene instalado de SSL, use el protocolo HTTPS en lugar del protocolo HTTP. Reemplace _ServerName_ con el nombre del servidor que va a usar. Reemplace _ProjectServerName_ con el nombre del directorio virtual de su sitio de project server, por ejemplo, PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Cualquier otra variable que deba cambiar se señala en la parte superior del ejemplo de código.
  
## <a name="verifying-the-results"></a>Comprobación de los resultados:
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Introducción e interpretar los resultados de un ejemplo de código no siempre son un proceso sencillo. Por ejemplo, si se crea un proyecto, debe publicar el proyecto antes de que aparezca en la página Centro de proyectos en Project Web App.
  
Puede verificar los resultados de muestra de código de varias formas, por ejemplo:
  
- Use el cliente de Project Professional 2013 para abrir el proyecto desde el equipo de Project Server y ver los elementos que desee.
    
- Ver los proyectos publicados en la página Centro de proyectos de Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Ver el registro de cola en Project Web App. Abra la página Configuración del servidor (en la esquina superior derecha, elija el icono **configuración** ) y, a continuación, elija **Mis trabajos en cola** en la sección **Configuración Personal** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). En la lista desplegable **vista** , puede ordenar por el estado del trabajo. El estado predeterminado es **en curso y los trabajos con errores en la semana pasada**. 
    
- Use la página Configuración del servidor de Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) para administrar todos los trabajos en cola y eliminar o forzar la protección de empresa de objetos. Debe tener permisos administrativos para tener acceso a los vínculos en la página Configuración del servidor.
    
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

## <a name="cleaning-up"></a>Limpiar
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Después de probar algunos ejemplos de código, son objetos de empresa y la configuración que se debe eliminar o restablecer. Puede usar la página Configuración del servidor en Project Web App para administrar datos de la empresa ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Vínculos en la página Configuración del servidor permiten eliminar elementos antiguos, forzar la protección de proyectos, administrar la cola de trabajo para todos los usuarios y realizar otras tareas administrativas.
  
A continuación aparecen algunos de los enlaces de la página Configuración de servidor para utilizar para actividades típicas de limpieza después de ejecutar muestras de código:
  
- **Campos personalizados de empresa y tablas de búsqueda**
    
- **Administrar trabajos en cola**
    
- **Eliminar objetos de empresa**
    
- **Forzar protección de objetos de la empresa**
    
- **Tipos de proyecto empresarial**
    
- **Fases de flujo de trabajo**
    
- **Etapas de flujo de trabajo**
    
- **Páginas de detalles del proyecto**
    
- **Períodos de presentación de informes de horas**
    
- **Configuración y valores predeterminados del parte de horas**
    
- **Clasificaciones de línea**
    
Configuración adicional se administra mediante SharePoint Server 2013 para cada instancia de Project Web App, en lugar de una página específica de la configuración del servidor de Project Web App. En la aplicación de Administración Central de SharePoint, elija **Configuración de aplicación General**, elija **Administrar** bajo **Configuración de Project Server**y, a continuación, elija la instancia de Project Web App en la lista desplegable en la página Configuración del servidor . Por ejemplo, elija **Controladores de eventos del servidor** para agregar o eliminar controladores de eventos para la instancia de Project Web App seleccionada. 
  
## <a name="see-also"></a>Vea también

- [Requisitos previos para ejemplos de código basados en ASMX en Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Tutorial: Desarrollar aplicaciones de PSI mediante WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Usar suplantación con WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Información general de referencia PSI de Project](project-psi-reference-overview.md) 
- [Centro para desarrolladores de SharePoint](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

