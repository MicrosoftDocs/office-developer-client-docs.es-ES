---
title: Ejemplo de propiedad Clustered (VB)
TOCTitle: Clustered Property Example (VB)
ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15)
ms:contentKeyID: 48543293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4cf09b0e8393eca74b1ed8fbaca8591a99103b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485679"
---
# <a name="clustered-property-example-vb"></a><span data-ttu-id="dbfa8-102">Ejemplo de propiedad Clustered (VB)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-102">Clustered Property Example (VB)</span></span>


<span data-ttu-id="dbfa8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbfa8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dbfa8-104">En este ejemplo, se muestra la propiedad [Clustered](clustered-property-adox.md) de un [índice](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="dbfa8-104">This example demonstrates the [Clustered](clustered-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="dbfa8-105">Tenga en cuenta que las bases de datos Microsoft Jet no admiten índices agrupados, por lo que en este ejemplo se devolverá **False** para la propiedad **Clustered** de todos los índices de la base de datos *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="dbfa8-105">Note that Microsoft Jet databases do not support clustered indexes, so this example will return **False** for the **Clustered** property of all indexes in the *Northwind* database.</span></span>

```vb 
 
' BeginClusteredVB 
Sub Main() 
 On Error GoTo ClusteredXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblLoop As ADOX.Table 
 Dim idxLoop As ADOX.Index 
 Dim strCnn As String 
 
 strCnn = "Provider='SQLOLEDB';Data Source='MySqlServer';Initial Catalog='pubs';" & _ 
 "Integrated Security='SSPI';" 
 ' Connect the catalog. 
 cnn.Open strCnn 
 cat.ActiveConnection = cnn 
 
 ' Enumerate Tables 
 For Each tblLoop In cat.Tables 
 'Enumerate Indexes 
 For Each idxLoop In tblLoop.Indexes 
 Debug.Print tblLoop.Name & " " & _ 
 idxLoop.Name & " " & idxLoop.Clustered 
 Next idxLoop 
 Next tblLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ClusteredXError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndClusteredVB 
```

