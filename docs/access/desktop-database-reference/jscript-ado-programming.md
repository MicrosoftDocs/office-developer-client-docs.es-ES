---
title: Programación ADO con JScript
TOCTitle: JScript ADO Programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 167033c58b163ffcef7934b6f38b79323c6b58b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484448"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="fb7ac-102">Programación ADO con JScript</span><span class="sxs-lookup"><span data-stu-id="fb7ac-102">JScript ADO Programming</span></span>


<span data-ttu-id="fb7ac-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb7ac-103">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="fb7ac-104">Crear un proyecto de ADO</span><span class="sxs-lookup"><span data-stu-id="fb7ac-104">Creating an ADO Project</span></span>

<span data-ttu-id="fb7ac-p101">Microsoft JScript no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en JScript.</span><span class="sxs-lookup"><span data-stu-id="fb7ac-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="fb7ac-108">Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con JScript:</span><span class="sxs-lookup"><span data-stu-id="fb7ac-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="fb7ac-109">Para escribir secuencias de comandos de servidor, utilice Adojavas.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\ado\\ carpeta de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fb7ac-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="fb7ac-110">Para escribir secuencias de comandos de cliente, utilice Adcjavas.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\msdac\\ carpeta de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fb7ac-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="fb7ac-111">Puede copiar y pegar las definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando secuencias de comandos de servidor, copie el archivo Adojavas.inc en una carpeta en el sitio Web y haga referencia a él desde la página ASP como esta:</span><span class="sxs-lookup"><span data-stu-id="fb7ac-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="fb7ac-112">Crear objetos de ADO en JScript</span><span class="sxs-lookup"><span data-stu-id="fb7ac-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="fb7ac-113">Deberá utilizar la llamada a la función **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="fb7ac-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="fb7ac-114">Ejemplo de JScript</span><span class="sxs-lookup"><span data-stu-id="fb7ac-114">JScript Example</span></span>

<span data-ttu-id="fb7ac-115">El código siguiente es un ejemplo genérico de programación de servidor con JScript en un archivo ASP que abre un objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="fb7ac-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

