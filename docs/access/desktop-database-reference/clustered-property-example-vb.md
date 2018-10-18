---
<<<<<<< Título HEAD: ejemplo de propiedad Clustered (VB) TOCTitle: ejemplo de propiedad Clustered (VB) === título: ejemplo de propiedad Clustered (VB) TOCTitle: ejemplo de propiedad Clustered (VB)
>>>>>>> Master ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15) ms:contentKeyID: ms.date 48543293: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="clustered-property-example-vb"></a>Ejemplo de propiedad Clustered (VB)
=======
# <a name="clustered-property-example-vb"></a>Ejemplo de propiedad Clustered (VB)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo, se muestra la propiedad [Clustered](clustered-property-adox.md) de un [índice](index-object-adox.md). Tenga en cuenta que las bases de datos Microsoft Jet no admiten índices agrupados, por lo que en este ejemplo se devolverá **False** para la propiedad **Clustered** de todos los índices de la base de datos *Northwind* .

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

