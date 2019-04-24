---
title: InfoPath, codificación RPC y servicios web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Los servicios web pueden exponer uno de dos estilos para enlazar con sus métodos web en el contrato WSDL (Lenguaje de descripción de servicios web) que los describe: Documento o RPC.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303531"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="1b659-103">InfoPath, codificación RPC y servicios web</span><span class="sxs-lookup"><span data-stu-id="1b659-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="1b659-p101">Los servicios web pueden exponer uno de dos estilos para enlazar con sus métodos web en el contrato WSDL (Lenguaje de descripción de servicios web) que los describe: Documento o RPC. Asimismo, cada uno de estos dos estilos de enlace pueden especificarse como literal o codificado. Las implementaciones más comunes de cada tipo son: documento/literal y RPC/codificado. Sin embargo, Microsoft InfoPath solo admite la conexión a los servicios web que usen el estilo documento/literal.</span><span class="sxs-lookup"><span data-stu-id="1b659-p101">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC. Additionally, each of these two styles of binding can be specified as either literal or encoded. The most common implementations for each type are: document/literal and RPC/encoded. However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="1b659-p102">La mayoría de las herramientas de desarrollo de servicios web proporcionan un modificador para especificar el tipo de servicio web que se desea crear. Si está desarrollando un servicio web al que se conectará desde InfoPath, debe especificar documento/literal como codificación y estilo del servicio web.</span><span class="sxs-lookup"><span data-stu-id="1b659-p102">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create. If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="1b659-110">Sin embargo, si no controla el servicio web con el que desea trabajar y tiene que conectarse a un servicio web que usa el estilo RPC/codificado, use un servicio proxy de .NET para conectar con un servicio web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="1b659-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="1b659-111">Uso de un servicio proxy de .NET para conectar con un servicio web</span><span class="sxs-lookup"><span data-stu-id="1b659-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="1b659-p103">Si no controla el servicio web RPC/codificado con el que desea trabajar, puede crear un servicio proxy documento/literal de Microsoft .NET que proporcione funciones de contenedor para cada uno de los métodos web que desea invocar desde el servicio web RPC/codificado. Entonces podrá trabajar con el servicio web de proxy documento/literal desde InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1b659-p103">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service. You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="1b659-p104">El código de .NET Framework funciona con cualquier tipo de servicio web (tanto RPC/codificado como documento/literal) y todos los servicios web de .NET usan la codificación y el estilo documento/literal. Como .NET Framework puede comunicarse con cualquier tipo de servicio web, puede crear un servicio web .NET que tenga métodos que hagan llamadas al servicio web RPC/codificado. El servicio web .NET actuará como el traductor que permite a InfoPath hacer llamadas en estilo documento/literal al servicio web .NET que, a su vez, puede hacer llamadas RPC/codificadas al servicio web original.</span><span class="sxs-lookup"><span data-stu-id="1b659-p104">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding. Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service. The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="1b659-p105">Los requisitos previos para crear un servicio web de proxy de Microsoft .NET son un equipo con Microsoft Windows o Microsoft Windows Server en el que se ejecute Internet Information Services (IIS) con ASP.NET instalado para implementar el servicio web de proxy. Cuando cree una solución de InfoPath, señalará al servicio web de proxy en lugar de al servicio web RPC/codificado. El servicio web de proxy hará llamadas al servicio RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="1b659-p105">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service. When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service. The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="1b659-120">Crear un servicio web de proxy con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b659-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="1b659-121">Crear un nuevo proyecto de **Aplicación de servicio web de ASP.NET**.</span><span class="sxs-lookup"><span data-stu-id="1b659-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="1b659-122">En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** del nuevo proyecto y, a continuación, haga clic en **Agregar referencia web**.</span><span class="sxs-lookup"><span data-stu-id="1b659-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="1b659-123">En el cuadro de diálogo **Agregar referencia web**, escriba la dirección URL del servicio web RPC/codificado con el que desea trabajar y haga clic en **Ir**.</span><span class="sxs-lookup"><span data-stu-id="1b659-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="1b659-124">Haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="1b659-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="1b659-125">Abra el archivo .asmx del servicio web y agregue un método de servicio web que llame a cada método de servicio web desde el servicio web RPC/codificado al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="1b659-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="1b659-p106">Para ver una lista de los métodos del servidor web RPC/codificado de referencia, muestre la ventana **Vista de clases**. Por cada método de servicio web, verá tres métodos. Por ejemplo, si el método de servicio web se denomina  `doSearch`, verá tres métodos denominados  `doSearch`,  `BegindoSearch` y  `EnddoSearch`. Sólo tiene que crear un método contenedor de servicio web para el método  `doSearch`. Asegúrese de que la firma del método y el tipo devuelto coinciden exactamente.</span><span class="sxs-lookup"><span data-stu-id="1b659-p106">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window. For each Web Service method, you will see three methods. For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`. You only have to create a wrapper Web Service method for the  `doSearch` method. Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="1b659-131">Dentro de cada método contenedor, tiene que escribir código que haga una llamada al servicio web RPC/codificado al que se hace referencia, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b659-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="1b659-132">Si el servicio web RPC/codificado requiere autenticación, codifique las credenciales necesarias para conectar con el servicio web RPC/codificado en el código fuente del servicio web de proxy .NET o use código como el que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="1b659-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="1b659-133">Para obtener más información, consulte el artículo de Microsoft Knowledge Base sobre cómo pasar las credenciales existentes a un servicio web de ASP.NET, en https://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="1b659-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="1b659-134">Crear un servicio web de proxy sin Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="1b659-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="1b659-135">También puede crear un servicio web de proxy con las herramientas que se proporcionan en el kit de desarrollo de software de .NET Framework, que se puede descargar de MSDN.</span><span class="sxs-lookup"><span data-stu-id="1b659-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="1b659-p107">Use la herramienta Wsdl.exe (Lenguaje de descripción de servicios web) para crear el archivo de código para el servicio web de proxy. Este archivo de código puede compilarse con el compilador de la línea de comandos de C# (csc.exe) o el compilador de la línea de comandos de Visual Basic .NET (vbc.exe), que también están incluidos en el SDK de .NET Framework. Una vez que la herramienta Lenguaje de descripción de servicios web genere al archivo de código, cambie la extensión del nombre de archivo por .asmx y abra el archivo en cualquier editor de texto. En la primera línea del documento, agregue la siguiente directiva de página:</span><span class="sxs-lookup"><span data-stu-id="1b659-p107">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service. This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK. After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor. On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="1b659-p108">Vaya al final del archivo de código y cree una llamada a cada método de servicio web del servicio web RPC/codificado. En el código de ejemplo siguiente se muestra el código de un servicio web de .NET Web que conecta con el servicio web de Google, que usa el estilo de desarrollo RPC/codificado. Hay un marcador de posición donde debería ir el código generado por la herramienta wsdl.exe.</span><span class="sxs-lookup"><span data-stu-id="1b659-p108">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service. The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development. There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


