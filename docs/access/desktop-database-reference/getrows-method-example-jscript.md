---
title: Ejemplo del método GetRows (JScript)
TOCTitle: GetRows method example (JScript)
ms:assetid: 72d7e2d9-1e19-e993-0b0e-5310405c9b75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249466(v=office.15)
ms:contentKeyID: 48545620
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8da290cc259f9be165e069c8a62e61fa8b748b3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864119"
---
# <a name="getrows-method-example-jscript"></a>Ejemplo del método GetRows (JScript)


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo se utiliza el método [GetRows](getrows-method-ado.md) para recuperar todas las filas de la tabla *Customers* de un [conjunto de registros](recordset-object-ado.md) y rellenar una matriz con los datos resultantes. El método **GetRows** devolverá un número de filas menor que el deseado en los dos siguientes casos: si se alcanza [EOF](bof-eof-properties-ado.md) o si **GetRows** ha tratado de recuperar un registro anteriormente eliminado por otro usuario. La función devuelve **False** sólo si se produce el segundo caso. Corte y pegue el código siguiente en Bloc de notas u otro editor de texto y guárdelo como **GetRowsJS.asp**.

```javascript 
 
<!-- BeginGetRowsJS --> 
<%@ LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>ADO Recordset.GetRows example (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead { 
 background-color: #008080; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="white"> 
 
<h1>ADO Recordset.GetRows example (JScript)</h1> 
 <!-- Page text goes here --> 
<% 
 var Connect = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var mySQL = "select * from customers;"; 
 var showblank = " "; 
 var shownull = "-null-"; 
 
 var connTemp = Server.CreateObject("ADODB.Connection"); 
 
 try 
 { 
 connTemp.Open(Connect); 
 var rsTemp = Server.CreateObject("ADODB.Recordset"); 
 rsTemp.ActiveConnection = connTemp; 
 rsTemp.CursorLocation = adUseClient; 
 rsTemp.CursorType = adOpenKeyset; 
 rsTemp.LockType = adLockOptimistic; 
 rsTemp.Open(mySQL); 
 
 rsTemp.MoveFirst(); 
 
 if (rsTemp.RecordCount == 0) 
 { 
 Response.Write("No records matched "); 
 Response.Write (mySQL & "So cannot make table..."); 
 connTemp.Close(); 
 Response.End(); 
 } else 
 { 
 Response.Write('<table width="100%" border="2">'); 
 Response.Write('<tr class="thead2">'); 
 
 // Headings On The Table for each Field Name 
 for (var i=0; i<rsTemp.Fields.Count; i++) 
 { 
 fieldObject = rsTemp.fields(i); 
 Response.Write('<td width="' + Math.floor(100 / rsTemp.Fields.Count) + '%">' + fieldObject.name + "</td>"); 
 } 
 
 Response.Write("</tr>"); 
 
 // JScript doesn't support multi-dimensional arrays 
 // so we'll convert the returned array to a single 
 // dimensional JScript array and then display the data. 
 tempArray = rsTemp.GetRows(); 
 recArray = tempArray.toArray(); 
 
 var col = 1; 
 var maxCols = rsTemp.Fields.Count; 
 
 for (var thisField=0; thisField<recArray.length; thisField++) 
 { 
 if (col == 1) 
 Response.Write('<tr class="tbody">'); 
 if (recArray[thisField] == null) 
 recArray[thisField] = shownull; 
 if (recArray[thisField] == "") 
 recArray[thisField] = showblank; 
 Response.Write("<td>" + recArray[thisField] + "</td>"); 
 col++ 
 if (col > maxCols) 
 { 
 Response.Write("</tr>"); 
 col = 1; 
 } 
 } 
 Response.Write("</table>"); 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsTemp.State == adStateOpen) 
 rsTemp.Close; 
 if (connTemp.State == adStateOpen) 
 connTemp.Close; 
 rsTemp = null; 
 connTemp = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndGetRowsJS --> 
 
```

