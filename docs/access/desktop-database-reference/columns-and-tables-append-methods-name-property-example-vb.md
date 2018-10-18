---
<<<<<<< Título HEAD: columnas y tablas de métodos Append, TOCTitle de ejemplo de la propiedad de nombre (VB): columnas y tablas de métodos Append, ejemplo de propiedad de nombre (VB) === título: columnas y tablas métodos Append, nombre de la propiedad (VB) TOCTitle: Columnas y tablas métodos Append, nombre de la propiedad (VB)
>>>>>>> Master ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15) ms:contentKeyID: ms.date 48544238: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a>Ejemplo de métodos Append de Columns y Tables, propiedad Name (VB)
=======
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a>Columnas y tablas métodos Append, nombre de la propiedad (VB)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

El código siguiente muestra cómo crear una tabla nueva.

```vb 
 
' BeginCreateTableVB 
Sub Main() 
 On Error GoTo CreateTableError 
 
 Dim tbl As New Table 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Exit Sub 
 
CreateTableError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateTableVB 
```

