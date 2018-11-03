---
title: Programación ADO en VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 694580005a3d016448ea9e5e715fea236a1d93f5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944868"
---
# <a name="vbscript-ado-programming"></a>Programación ADO de VBScript


**Se aplica a**: Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Crear un proyecto de ADO

Microsoft Visual Basic Scripting Edition no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en VBScript.

Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con VBScript:

  - Para escribir secuencias de comandos de servidor, utilice Adovbs.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\ado\\ carpeta de forma predeterminada.

  - Para escribir secuencias de comandos de cliente, utilice Adcvbs.inc, el cual se instala en la unidad c:\\archivos de programa\\archivos comunes\\System\\msdac\\ carpeta de forma predeterminada.

Puede copiar y pegar las definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando secuencias de comandos de servidor, copiar archivo Adovbs.inc en una carpeta en su sitio Web y hacer referencia a él desde la página ASP como esta:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Crear objetos de ADO en VBScript

No es posible utilizar la instrucción **Dim** para asignar objetos a un tipo específico en VBScript. Además, VBScript no admite la sintaxis **New** utilizada con la instrucción **Dim** en Visual Basic para Aplicaciones (VBA). Deberá utilizar la llamada a la función **CreateObject**:

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Ejemplos de VBScript

El código siguiente es un ejemplo genérico de programación de servidor con VBScript en un archivo ASP:

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

En la documentación de ADO, se incluyen ejemplos más específicos de VBScript. Para obtener más información, vea [ejemplos de código de ADO en Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Diferencias entre VBScript y Visual Basic

El uso de ADO con VBScript es similar al uso con Visual Basic, incluido el uso de la sintaxis. Sin embargo, existen algunas diferencias significativas:

- VBScript sólo admite el tipo de datos Variant, el cual puede contener diferentes tipos de datos. Es posible almacenar los datos que se necesitan en un tipo de datos Variant, y aquéllos funcionarán correctamente debido a la conversión realizada por VBScript. Éste reconoce el tipo requerido por ADO y convierte el valor correspondiente del Variant en consecuencia.

- No puede usar `on error goto <label>` dentro de VBScript.

- VBScript admite algunas de las funciones incorporadas de Visual Basic, tales como **Msgbox**, **Date** y **IsNumeric**. Sin embargo, puesto que VBScript es un subconjunto de Visual Basic, no todas las funciones integradas están admitidas. Por ejemplo, VBScript no admite la función **Format** ni las funciones de E/S de archivo.

