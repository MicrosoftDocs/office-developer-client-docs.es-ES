---
title: Ejemplo del método Clone (VBScript)
TOCTitle: Clone method example (VBScript)
ms:assetid: b9d49eb9-8da8-dfd2-1c59-35ac70969850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249893(v=office.15)
ms:contentKeyID: 48547357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1fc3341f4ec662c17e2a7c274b1cc3af215c877c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296335"
---
# <a name="clone-method-example-vbscript"></a>Ejemplo del método Clone (VBScript)


**Se aplica a:** Access 2013, Office 2013

En este ejemplo se usa el método [Clone](clone-method-ado.md) para crear copias de un [conjunto de registros](recordset-object-ado.md) y, después, se deja que el usuario coloque el puntero de registros de cada copia de manera independiente.

Use el ejemplo siguiente en una página Active Server (ASP). En este ejemplo se utiliza la base de datos Northwind distribuida con Microsoft Access. Corte y pegue el código siguiente en el Bloc de notas u otro editor de texto y guárdelo como **CloneVBS.asp**. Podrá ver el resultado en cualquier explorador de cliente.

Para realizar el ejemplo, cambie la línea RsCustomerList.Source = "Customers" a RsCustomerList.Source = "Products" para contar una tabla más grande.

```vb 
 
<!-- BeginCloneVBS --> 
<% Language = VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Clone Method</TITLE> 
</HEAD> 
 
<BODY> 
 
<H1 align="center">ADO Clone Method</H1> 
<HR> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim rsFirst, rsLast, rsCount 
    Dim rsClone 
    Dim CloneFirst, CloneLast, CloneCount 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open strCnxn 
         
    ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    rsCustomers.MoveFirst 
    rsCount = rsCustomers.RecordCount 
    rsFirst = rsCustomers("CompanyName") 
    rsCustomers.MoveLast 
    rsLast = rsCustomers("CompanyName") 
 
    ' create clone 
    Set rsClone = rsCustomers.Clone 
    rsClone.MoveFirst 
    CloneCount = rsClone.RecordCount 
    CloneFirst = rsClone("CompanyName") 
    rsClone.MoveLast 
    CloneLast = rsClone("CompanyName") 
%> 
 
<!-- Display Results --> 
<H3>There Are <%=rsCount%> Records in the original recordset</H3> 
<H3>The first record is <%=rsFirst%> and the last record is <%=rsLast%></H3> 
<BR><HR> 
<H3>There Are <%=CloneCount%> Records in the original recordset</H3> 
<H3>The first record is <%=CloneFirst%> and the last record is <%=CloneLast%></H3> 
<BR><HR> 
<H4>Location of OLEDB Database</H4> 
 
<% 
    ' Show location of DSN data source 
    Response.Write(Cnxn) 
 
    ' Clean up 
    If rsCustomers.State = adStateOpen then 
       rsCustomers.Close 
    End If 
    If rsClone.State = adStateOpen then 
       rsClone.Close 
    End If 
    If Cnxn.State = adStateOpen then 
       Cnxn.Close 
    End If 
    Set rsCustomers = Nothing 
    Set rsClone = Nothing 
    Set Cnxn = Nothing 
%> 
</BODY> 
</HTML> 
<!-- EndCloneVBS --> 
 
```

