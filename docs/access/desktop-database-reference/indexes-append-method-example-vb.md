---
title: Ejemplo del método Append de Indexes (VB)
TOCTitle: Indexes Append method example (VB)
ms:assetid: 71b18a5b-d000-5184-afac-c5d26b7f17e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249454(v=office.15)
ms:contentKeyID: 48545591
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b004f5e952f471ef6c39e4fa40dc9ae6a5a2fce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291681"
---
# <a name="indexes-append-method-example-vb"></a>Ejemplo del método Append de Indexes (VB)


**Se aplica a:** Access 2013, Office 2013

El código siguiente muestra cómo crear un índice nuevo. El índice es para dos columnas de la tabla.

```vb 
 
' BeginCreateIndexVB 
Sub Main() 
 On Error GoTo CreateIndexError 
 
 Dim tbl As New Table 
 Dim idx As New ADOX.Index 
 Dim cat As New ADOX.Catalog 
 
 'Open the catalog. 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the table and append it to the catalog 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 ' Define a multi-column index 
 idx.Name = "multicolidx" 
 idx.Columns.Append "Column1" 
 idx.Columns.Append "Column2" 
 
 ' Append the index to the table 
 tbl.Indexes.Append idx 
 Debug.Print "The index is appended to table 'MyTable'." 
 
 'Delete the table as this is a demonstration 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set idx = Nothing 
 Exit Sub 
 
CreateIndexError: 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set idx = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateIndexVB 
```

