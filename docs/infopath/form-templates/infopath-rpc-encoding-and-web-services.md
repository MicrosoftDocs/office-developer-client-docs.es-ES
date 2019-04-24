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
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, codificación RPC y servicios web

Los servicios web pueden exponer uno de dos estilos para enlazar con sus métodos web en el contrato WSDL (Lenguaje de descripción de servicios web) que los describe: Documento o RPC. Asimismo, cada uno de estos dos estilos de enlace pueden especificarse como literal o codificado. Las implementaciones más comunes de cada tipo son: documento/literal y RPC/codificado. Sin embargo, Microsoft InfoPath solo admite la conexión a los servicios web que usen el estilo documento/literal.
  
La mayoría de las herramientas de desarrollo de servicios web proporcionan un modificador para especificar el tipo de servicio web que se desea crear. Si está desarrollando un servicio web al que se conectará desde InfoPath, debe especificar documento/literal como codificación y estilo del servicio web.
  
Sin embargo, si no controla el servicio web con el que desea trabajar y tiene que conectarse a un servicio web que usa el estilo RPC/codificado, use un servicio proxy de .NET para conectar con un servicio web RPC/codificado.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Uso de un servicio proxy de .NET para conectar con un servicio web

Si no controla el servicio web RPC/codificado con el que desea trabajar, puede crear un servicio proxy documento/literal de Microsoft .NET que proporcione funciones de contenedor para cada uno de los métodos web que desea invocar desde el servicio web RPC/codificado. Entonces podrá trabajar con el servicio web de proxy documento/literal desde InfoPath.
  
El código de .NET Framework funciona con cualquier tipo de servicio web (tanto RPC/codificado como documento/literal) y todos los servicios web de .NET usan la codificación y el estilo documento/literal. Como .NET Framework puede comunicarse con cualquier tipo de servicio web, puede crear un servicio web .NET que tenga métodos que hagan llamadas al servicio web RPC/codificado. El servicio web .NET actuará como el traductor que permite a InfoPath hacer llamadas en estilo documento/literal al servicio web .NET que, a su vez, puede hacer llamadas RPC/codificadas al servicio web original.
  
Los requisitos previos para crear un servicio web de proxy de Microsoft .NET son un equipo con Microsoft Windows o Microsoft Windows Server en el que se ejecute Internet Information Services (IIS) con ASP.NET instalado para implementar el servicio web de proxy. Cuando cree una solución de InfoPath, señalará al servicio web de proxy en lugar de al servicio web RPC/codificado. El servicio web de proxy hará llamadas al servicio RPC/codificado.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Crear un servicio web de proxy con Visual Studio

1. Crear un nuevo proyecto de **Aplicación de servicio web de ASP.NET**. 
    
2. En el **Explorador de soluciones**, haga clic con el botón secundario en la carpeta **Referencias** del nuevo proyecto y, a continuación, haga clic en **Agregar referencia web**. 
    
3. En el cuadro de diálogo **Agregar referencia web**, escriba la dirección URL del servicio web RPC/codificado con el que desea trabajar y haga clic en **Ir**.
    
4. Haga clic en **Agregar referencia**. 
    
5. Abra el archivo .asmx del servicio web y agregue un método de servicio web que llame a cada método de servicio web desde el servicio web RPC/codificado al que se hace referencia.
    
6. Para ver una lista de los métodos del servidor web RPC/codificado de referencia, muestre la ventana **Vista de clases**. Por cada método de servicio web, verá tres métodos. Por ejemplo, si el método de servicio web se denomina  `doSearch`, verá tres métodos denominados  `doSearch`,  `BegindoSearch` y  `EnddoSearch`. Sólo tiene que crear un método contenedor de servicio web para el método  `doSearch`. Asegúrese de que la firma del método y el tipo devuelto coinciden exactamente. 
    
7. Dentro de cada método contenedor, tiene que escribir código que haga una llamada al servicio web RPC/codificado al que se hace referencia, como se muestra en el ejemplo siguiente. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Si el servicio web RPC/codificado requiere autenticación, codifique las credenciales necesarias para conectar con el servicio web RPC/codificado en el código fuente del servicio web de proxy .NET o use código como el que se muestra a continuación. 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Para obtener más información, consulte el artículo de Microsoft Knowledge Base sobre cómo pasar las credenciales existentes a un servicio web de ASP.NET, en https://support.microsoft.com/.
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Crear un servicio web de proxy sin Visual Studio .NET

También puede crear un servicio web de proxy con las herramientas que se proporcionan en el kit de desarrollo de software de .NET Framework, que se puede descargar de MSDN.
  
Use la herramienta Wsdl.exe (Lenguaje de descripción de servicios web) para crear el archivo de código para el servicio web de proxy. Este archivo de código puede compilarse con el compilador de la línea de comandos de C# (csc.exe) o el compilador de la línea de comandos de Visual Basic .NET (vbc.exe), que también están incluidos en el SDK de .NET Framework. Una vez que la herramienta Lenguaje de descripción de servicios web genere al archivo de código, cambie la extensión del nombre de archivo por .asmx y abra el archivo en cualquier editor de texto. En la primera línea del documento, agregue la siguiente directiva de página:
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Vaya al final del archivo de código y cree una llamada a cada método de servicio web del servicio web RPC/codificado. En el código de ejemplo siguiente se muestra el código de un servicio web de .NET Web que conecta con el servicio web de Google, que usa el estilo de desarrollo RPC/codificado. Hay un marcador de posición donde debería ir el código generado por la herramienta wsdl.exe.
  
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


