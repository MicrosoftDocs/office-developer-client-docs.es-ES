---
title: Ejemplo del método Find (JScript)
TOCTitle: Find Method Example (JScript)
ms:assetid: 87db96d6-4ed4-0807-8bff-62d978d4a008
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249589(v=office.15)
ms:contentKeyID: 48546116
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 171ffa27f5ac3da669f8c8b55c769632fc2b0452
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485820"
---
# <a name="find-method-example-jscript"></a><span data-ttu-id="7aa1e-102">Ejemplo del método Find (JScript)</span><span class="sxs-lookup"><span data-stu-id="7aa1e-102">Find Method Example (JScript)</span></span>


<span data-ttu-id="7aa1e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aa1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7aa1e-104">En este ejemplo se usa el método de [Find](find-method-ado.md) del objeto [Recordset](recordset-object-ado.md) para localizar y mostrar las compañías de la base de datos ***Northwind*** cuyo nombre comienza con la letra G. corte y pegue el código siguiente en el Bloc de notas u otro editor de texto y guárdelo como \*\* FindJS.asp\*\*.</span><span class="sxs-lookup"><span data-stu-id="7aa1e-104">This example uses the [Recordset](recordset-object-ado.md) object's [Find](find-method-ado.md) method to locate and display the companies in the ***Northwind*** database whose name begins with the letter G. Cut and paste the following code to Notepad or another text editor, and save it as **FindJS.asp**.</span></span>

```javascript 
 
<!-- BeginFindJS --> 
<%@ Language=JavaScript %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>ADO Recordset.Find Example</title> 
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
 
<h1>ADO Recordset.Find Example</h1> 
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection"); 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsCustomers = Server.CreateObject("ADODB.Recordset"); 
 // display string 
 var strMessage; 
 var strFind; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 //create recordset using object refs 
 SQLCustomers = "select * from Customers;"; 
 
 rsCustomers.ActiveConnection = Cnxn; 
 rsCustomers.CursorLocation = adUseClient; 
 rsCustomers.CursorType = adOpenKeyset; 
 rsCustomers.LockType = adLockOptimistic; 
 rsCustomers.Source = SQLCustomers; 
 
 rsCustomers.Open(); 
 rsCustomers.MoveFirst(); 
 
 //find criteria 
 strFind = "CompanyName like 'g%'" 
 rsCustomers.Find(strFind); 
 
 if (rsCustomers.EOF) { 
 Response.Write("No records matched "); 
 Response.Write(SQLCustomers & "So cannot make table..."); 
 Cnxn.Close(); 
 Response.End(); 
 } 
 else { 
 Response.Write('<table width="100%" border="2">'); 
 Response.Write('<tr class="thead2">'); 
 // Put Headings On The Table for each Field Name 
 for (thisField = 0; thisField < rsCustomers.Fields.Count; thisField++) { 
 fieldObject = rsCustomers.Fields(thisField); 
 Response.Write('<th width="' + Math.floor(100 / rsCustomers.Fields.Count) + '%">' + fieldObject.Name + "</th>"); 
 } 
 Response.Write("</tr>"); 
 
 while (!rsCustomers.EOF) { 
 Response.Write('<tr class="tbody">'); 
 for(thisField=0; thisField<rsCustomers.Fields.Count; thisField++) { 
 fieldObject = rsCustomers.Fields(thisField); 
 strField = fieldObject.Value; 
 if (strField == null) 
 strField = "-Null-"; 
 if (strField == "") 
 strField = ""; 
 Response.Write("<td>" + strField + "</td>"); 
 } 
 rsCustomers.Find(strFind, 1, adSearchForward) 
 Response.Write("</tr>"); 
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
 if (rsCustomers.State == adStateOpen) 
 rsCustomers.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsCustomers = null; 
 Cnxn = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndFindJS --> 
 
```
