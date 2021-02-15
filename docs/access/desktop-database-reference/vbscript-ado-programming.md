---
title: Programación ADO en VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4aff2c8b3394321367851ad82e4e7efe98badff8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306030"
---
# <a name="vbscript-ado-programming"></a>Programación de ADO con VBScript


**Se aplica a:** Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Crear un proyecto de ADO

Microsoft Visual Basic Scripting Edition no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en VBScript.

Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con VBScript:

  - Para scripting del lado servidor, use Adovbs.inc, que está instalado en la carpeta c: Archivos de programa common \\ \\ Files System \\ \\ ado de forma \\ predeterminada.

  - Para scripting del lado cliente, use Adcvbs.inc, que está instalado en la carpeta \\ \\ \\ \\ msdac del sistema de archivos comunes de archivos de programa c: \\ de forma predeterminada.

Puede copiar y pegar definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando scripting del lado servidor, copie el archivo Adovbs.inc en una carpeta del sitio web y haciendo referencia a él desde la página ASP de esta forma:

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

- No se puede `on error goto <label>` usar en VBScript.

- VBScript admite algunas de las funciones incorporadas de Visual Basic, tales como **Msgbox**, **Date** y **IsNumeric**. Sin embargo, puesto que VBScript es un subconjunto de Visual Basic, no todas las funciones integradas están admitidas. Por ejemplo, VBScript no admite la función **Format** ni las funciones de E/S de archivo.

