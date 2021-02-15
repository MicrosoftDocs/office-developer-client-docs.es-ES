---
title: Programación de ADO con JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290894"
---
# <a name="jscript-ado-programming"></a>Programación de ADO con JScript


**Se aplica a:** Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Crear un proyecto de ADO

Microsoft JScript no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en JScript.

Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con JScript:

- Para scripting del lado servidor, use Adojavas.inc, que está instalado en la carpeta c: Archivos de programa common \\ \\ Files System \\ \\ ado de forma \\ predeterminada.

- Para scripting del lado cliente, use Adcjavas.inc, que está instalado en la carpeta \\ \\ \\ \\ msdac del sistema de archivos comunes de archivos de programa c: \\ de forma predeterminada.

Puede copiar y pegar definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando scripting del lado servidor, copie el archivo Adojavas.inc en una carpeta de su sitio web y haga referencia a él desde la página ASP de la siguiente forma:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Crear objetos de ADO en JScript

Deberá utilizar la llamada a la función **CreateObject**:

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Ejemplo de JScript

El código siguiente es un ejemplo genérico de programación de servidor con JScript en un archivo ASP que abre un objeto **Recordset**:

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

