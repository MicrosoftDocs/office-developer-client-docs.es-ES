---
<span data-ttu-id="cbe5e-101"><<<<<<< Título HEAD: AbsolutePosition y CursorLocation (JScript) del ejemplo se propiedades TOCTitle: ejemplo AbsolutePosition y CursorLocation propiedades (JScript) ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: ms.date 48548142: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="cbe5e-101"><<<<<<< HEAD title: AbsolutePosition and CursorLocation Properties Example (JScript) TOCTitle: AbsolutePosition and CursorLocation Properties Example (JScript) ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: 48548142 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a><span data-ttu-id="cbe5e-102">Ejemplo de las propiedades AbsolutePosition y CursorLocation (JScript)</span><span class="sxs-lookup"><span data-stu-id="cbe5e-102">AbsolutePosition and CursorLocation Properties Example (JScript)</span></span>

<span data-ttu-id="cbe5e-103">=== título: ejemplo de las propiedades AbsolutePosition y CursorLocation (JScript) TOCTitle: ms:assetid de ejemplo (JScript) de las propiedades AbsolutePosition y CursorLocation: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: ms.date 48548142: 17/10/2018 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="cbe5e-103">======= title: AbsolutePosition and CursorLocation properties example (JScript) TOCTitle: AbsolutePosition and CursorLocation properties example (JScript) ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15) ms:contentKeyID: 48548142 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a><span data-ttu-id="cbe5e-104">Ejemplo de las propiedades AbsolutePosition y CursorLocation (JScript)</span><span class="sxs-lookup"><span data-stu-id="cbe5e-104">AbsolutePosition and CursorLocation properties example (JScript)</span></span>
>>>>>>> <span data-ttu-id="cbe5e-105">master</span><span class="sxs-lookup"><span data-stu-id="cbe5e-105">master</span></span>

<span data-ttu-id="cbe5e-106">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbe5e-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cbe5e-p101">En este ejemplo se muestra cómo la propiedad [AbsolutePosition](absoluteposition-property-ado.md) puede realizar un seguimiento del progreso de un bucle que enumera todos los registros de un objeto [Recordset](recordset-object-ado.md). Usa la propiedad [CursorLocation](cursorlocation-property-ado.md) para habilitar la propiedad **AbsolutePosition** estableciendo el cursor en un cursor de cliente. Corte y pegue el código siguiente en el Bloc de notas u otro editor de texto y guárdelo como **AbsolutePositionJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-p101">This example demonstrates how the [AbsolutePosition](absoluteposition-property-ado.md) property can track the progress of a loop that enumerates all the records of a [Recordset](recordset-object-ado.md). It uses the [CursorLocation](cursorlocation-property-ado.md) property to enable the **AbsolutePosition** property by setting the cursor to a client cursor. Cut and paste the following code to Notepad or another text editor, and save it as **AbsolutePositionJS.asp**.</span></span>

```javascript
<!-- BeginAbsolutePositionJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<<<<<<< HEAD
<title>AbsolutePosition and CursorLocation Properties Example (JScript)</title> 
=======
<title>AbsolutePosition and CursorLocation properties example (JScript)</title> 
>>>>>>> master
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
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
 
<body> 
<<<<<<< HEAD
<h1>AbsolutePosition and CursorLocation Properties Example (JScript)</h1> 
=======
<h1>AbsolutePosition and CursorLocation properties example (JScript)</h1> 
>>>>>>> master
<% 
 // connection and recordset variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 // display string 
 var strMessage; 
 
 try 
 { 
 // Open a recordset on the Employee table using 
 // a client-side cursor to enable AbsolutePosition property. 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("employees", strCnxn, adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Write beginning of table to the document. 
 Response.Write('<table border="0" align="center">'); 
 Response.Write('<tr class="thead2">'); 
 Response.Write("<th>AbsolutePosition</th><th>Name</th><th>Hire Date</th></tr>"); 
 
 while (!rsEmployee.EOF) 
 { 
 strMessage = ""; 
 
 // Start a new table row. 
 strMessage = '<tr class="tbody">'; 
 
 // First column in row contains AbsolutePosition value. 
 strMessage += "<td>" + rsEmployee.AbsolutePosition + " of " + rsEmployee.RecordCount + "</td>" 
 
 // First and last name are in first column. 
 strMessage += "<td>" + rsEmployee.Fields("FirstName") + " "; 
 strMessage += rsEmployee.Fields("LastName") + " " + "</td>"; 
 
 // Hire date in second column. 
 strMessage += "<td>" + rsEmployee.Fields("HireDate") + "</td>"; 
 
 // End the row. 
 strMessage += "</tr>"; 
 
 // Write line to document. 
 Response.Write(strMessage); 
 
 // Get next record. 
 rsEmployee.MoveNext; 
 } 
 
 // Finish writing document. 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 rsEmployee = null; 
 } 
%> 
 
</html> 
<!-- EndAbsolutePositionJS --> 
```

