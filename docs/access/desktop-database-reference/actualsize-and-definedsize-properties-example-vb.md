---
<<<<<<< Título HEAD: ActualSize y ejemplo de propiedades de DefinedSize (VB) TOCTitle: ms:assetid ActualSize y ejemplo de propiedades de DefinedSize (VB): fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID: ms.date 48548884: 18/09/2015 mtps_version: Office.15
---

# <a name="actualsize-and-definedsize-properties-example-vb"></a>Ejemplo de las propiedades ActualSize y DefinedSize (VB)
=== título: ejemplo de las propiedades ActualSize y DefinedSize (VB) TOCTitle: ms:assetid de ejemplo (VB) de las propiedades ActualSize y DefinedSize: fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID: ms.date 48548884: 16/10/2018 mtps _version: Office.15
---

# <a name="actualsize-and-definedsize-properties-example-vb"></a>Ejemplo de las propiedades ActualSize y DefinedSize (VB)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

En este ejemplo se utilizan las propiedades [ActualSize](actualsize-property-ado.md) y [DefinedSize](definedsize-property-ado.md) para mostrar el tamaño definido y el tamaño real de un campo.

```vb 
 
'BeginActualSizeVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstStores As ADODB.Recordset 
 Dim SQLStores As String 
 Dim strCnxn As String 
 'record variables 
 Dim strMessage As String 
 
 ' Open a recordset for the Stores table 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Set rstStores = New ADODB.Recordset 
 
 SQLStores = "Suppliers" 
 rstStores.Open SQLStores, strCnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines of code are identical as the default values for 
 'CursorType and LockType arguments match those indicated 
 
 ' Loop through the recordset displaying the contents 
 ' of the store_name field, the field's defined size, 
 ' and its actual size. 
 rstStores.MoveFirst 
 
 Do Until rstStores.EOF 
 strMessage = "Company name: " & rstStores!CompanyName & _ 
 vbCrLf & "Defined size: " & _ 
 rstStores!CompanyName.DefinedSize & _ 
 vbCrLf & "Actual size: " & _ 
 rstStores!CompanyName.ActualSize & vbCrLf 
 
 MsgBox strMessage, vbOKCancel, "ADO ActualSize Property (Visual Basic)" 
 rstStores.MoveNext 
 Loop 
 
 ' clean up 
 rstStores.Close 
 Set rstStores = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstStores Is Nothing Then 
 If rstStores.State = adStateOpen Then rstStores.Close 
 End If 
 Set rstStores = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActualSizeVB 
```

