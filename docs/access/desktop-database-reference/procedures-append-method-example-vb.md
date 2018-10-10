---
title: Ejemplo de método Append de Procedures (VB)
TOCTitle: Procedures Append Method Example (VB)
ms:assetid: fa6c5e7a-6764-2208-26c8-f7fe4140dec3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250279(v=office.15)
ms:contentKeyID: 48548843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c3ad4e79bee0434e2a16d1a4b703dde83a43f11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483829"
---
# <a name="procedures-append-method-example-vb"></a><span data-ttu-id="a5e89-102">Ejemplo de método Append de Procedures (VB)</span><span class="sxs-lookup"><span data-stu-id="a5e89-102">Procedures Append Method Example (VB)</span></span>


<span data-ttu-id="a5e89-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5e89-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5e89-104">En el código siguiente, se muestra cómo usar un objeto [Command](command-object-ado.md) y el método [Append](procedures-collection-adox.md) de la colección [Procedures](append-method-adox-procedures.md) para crear un nuevo procedimiento en el origen de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="a5e89-104">The following code demonstrates how to use a [Command](command-object-ado.md) object and the [Procedures](procedures-collection-adox.md) collection [Append](append-method-adox-procedures.md) method to create a new procedure in the underlying data source.</span></span>

```vb 
 
' BeginCreateProcedureVB 
Sub Main() 
 On Error GoTo CreateProcedureError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As New ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Create the parameterized command (Microsoft Jet specific) 
 Set cmd.ActiveConnection = cnn 
 cmd.CommandText = "PARAMETERS [CustId] Text;" & _ 
 "Select * From Customers Where CustomerId = [CustId]" 
 
 ' Open the Catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Create the new Procedure 
 cat.Procedures.Append "CustomerById", cmd 
 
 'Clean 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateProcedureError: 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateProcedureVB 
```

