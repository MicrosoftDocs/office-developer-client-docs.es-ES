---
title: Ejemplo de la propiedad IndexNulls (VB)
TOCTitle: IndexNulls property example (VB)
ms:assetid: 69b5661c-931e-3a1c-d60e-96a0f93b9494
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249414(v=office.15)
ms:contentKeyID: 48545417
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e37f53218a7dabfa6248ea1da7630f82818a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291472"
---
# <a name="indexnulls-property-example-vb"></a>Ejemplo de la propiedad IndexNulls (VB)

**Se aplica a:** Access 2013, Office 2013

En este ejemplo, se muestra la propiedad [IndexNulls](indexnulls-property-adox.md) de un [índice](index-object-adox.md). El código crea un nuevo índice y establece el valor de **IndexNulls** en función de valores especificados por el usuario (de un cuadro de lista denominado List1). A continuación, **el índice** se anexa a la **tabla Empleados** [](table-object-adox.md) del *Catálogo northwind* [.](catalog-object-adox.md) El nuevo **índice** se aplica a un [conjunto de registros](recordset-object-ado.md) basándose en la tabla **Employees** y el **conjunto de registros** se abre. Se añade un nuevo registro a la tabla **Employees**, con valor **Nulo** en el campo indizado. Que el nuevo registro se muestre o no depende de la configuración de la propiedad **IndexNulls**.

```vb
    ' IndexNullsVB 
    Sub Main() 
     On Error GoTo IndexNullsXError 
     
     Dim cnn As New ADODB.Connection 
     Dim catNorthwind As New ADOX.Catalog 
     Dim idxNew As New ADOX.Index 
     Dim rstEmployees As New ADODB.Recordset 
     Dim varBookmark As Variant 
     
     ' Connect the catalog. 
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\" & _ 
     "Microsoft Office\Office\Samples\Northwind.mdb';" 
     
     Set catNorthwind.ActiveConnection = cnn 
     
     ' Append Country column to new index 
     idxNew.Columns.Append "Country" 
     idxNew.Name = "NewIndex" 
     
     Dim Response 
     Response = MsgBox("Allow 'Null' index? Otherwise ignore 'Null' index.", vbYesNo) 
     '"Allow 'Null' index? Otherwise ignore 'Null' index." 
     ', vbYesNo + vbCritical + vbDefaultButton2,,,, 
     If Response = vbYes Then ' User chose Yes. 
     idxNew.IndexNulls = adIndexNullsAllow 
     Else ' User chose No. 
     idxNew.IndexNulls = adIndexNullsIgnore 
     End If 
     
     'Append new index to Employees table 
     catNorthwind.Tables("Employees").Indexes.Append idxNew 
     
     rstEmployees.Index = idxNew.Name 
     rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
     adLockOptimistic, adCmdTableDirect 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Bookmark the newly added record 
     varBookmark = .Bookmark 
     
     ' Use the new index to set the order of the records. 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IndexNulls = " & idxNew.IndexNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IndexNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = varBookmark 
     .Delete 
     
     .Close 
     End With 
     
     'Clean up 
     Set rstEmployees = Nothing 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     cnn.Close 
     Set cnn = Nothing 
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     Exit Sub 
     
    IndexNullsXError: 
     
     If Not rstEmployees Is Nothing Then 
     If rstEmployees.State = adStateOpen Then rstEmployees.Close 
     End If 
     Set rstEmployees = Nothing 
     
     ' Delete new Index because this is a demonstration. 
     If Not catNorthwind Is Nothing Then 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     End If 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
     
    End Sub 
    ' EndIndexNullsVB
```
