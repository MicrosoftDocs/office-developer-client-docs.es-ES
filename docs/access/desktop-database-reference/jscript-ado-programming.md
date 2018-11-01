---
title: Programación ADO con JScript
TOCTitle: JScript ADO Programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd470482c8e4a2e9228247c5eea4512367ca6483
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867240"
---
# <a name="jscript-ado-programming"></a>Programación ADO con JScript


**Se aplica a**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Crear un proyecto de ADO

Microsoft JScript no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en JScript.

Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con JScript:

- Para escribir secuencias de comandos de servidor, utilice Adojavas.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\ado\\ carpeta de forma predeterminada.

- Para escribir secuencias de comandos de cliente, utilice Adcjavas.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\msdac\\ carpeta de forma predeterminada.

Puede copiar y pegar las definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando secuencias de comandos de servidor, copie el archivo Adojavas.inc en una carpeta en el sitio Web y haga referencia a él desde la página ASP como esta:

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

